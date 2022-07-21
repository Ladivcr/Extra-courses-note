# Infraestructura como código 

# Cómo desplegar infraestructura en Cloud

Cuando se habla de infraestructura en Cloud es necesario tener en cuenta diferentes cosas: 
1. Vamos a tener diferentes herramientas para desplegrar infraestructura en Cloud
2. Vamos a tener diferentes Cloud providers en los que podemos desplegar una infraestructura

Cuando trabajamos en proyectos de despliegue de infraestructura de forma automatizada y de aplicaciones.
**Una de las ventajas que tenemos es el versionamiento.** Ya que podedmos tener nuestra infraestructura versionada.

**Ejemplo:**

- Si tienes una app corriendo en un servidor y ahora le vas a añadir una BD.
La versión 1 puede tener el servidor y la versión 2 puede tenr la base de datos. 

Otras ventajas: 

- **Trazabilidad:** Se puede tener control y trazabilidad sobre cada despligue (como los commits en git)
- **Eficiencia:** Tienes una plantilla de código que se va a usar para desplegar la infraesctructura. Por lo que 
se puede usar dicha plantilla para diferentes ambientes. De tal forma que mejoras el tiempo de despliegue. 
- **Re-utilizable**: Tienes un template en el que tienes múltiples recursos, si cambias de proyecto, puedes
reutilizar el template sin problema.
- **Infraestructura inmutable:** La infraestructura no puede cambiar. 
- - **Ejemplo:** Tenemos un servidor corriendo con Mysql, apache web server y php. Y de repente surge un kernel panic. Podemos entrar al 
servidor y pasar tiempo tratando de solucionar el error. La otra opción es hacer uso del template que ya tenemos y volver a desplegarlo
desde cero. Esa es la escencia de la infraestructura inmutable. 

# Herramientas para desplegar infraestructura como código

1. **Terra:** Despliegues multi cloud, posee una version open source y otra enterprise
2. **Pulumi:** Despligues multi cloud, podes sacar ventajas tus conocimientos en un lenguaje
3. **Serverless Framework:** Para el despliegue de Lambdas, DynamoDB, api gateway, s3, kinesis
4. **SDK:** provista diferentes lenguajes, para python se llama boto3
5. **CDK (Cloud Development Kit):** Diferencia con el sdk, es que no va usar librerias particulares, sino que dentro del mismo codigo python
 vamos a llamar a los recursos y crearlos. Por detras cdk va a generar un template de CFN.
6. **AWS SAM (Serverless Aplication Model):** Para el despliegue de Lambdas, DynamoDB, api gateway, kinesis. Cambia la definición del recurso,
 para desplegar una lambda en CFN se declara como “AWS::Lambda::Function” y en SAM “AWS::Serverless::Function”

### What is CloudFormation?
> AWS CloudFormation is an AWS service that uses template files to automate the setup of AWS resources.

# Introducción y ventajas de usar Cloudformation

- **Flujo de despliegue:** Código, se verifica y hay una fase de despliegue. **Se pueden crear templates en formato YAML o JSON**.
- **Servicios:** Stacks, stack sets, integración full con todos los componentes de AWS.
- **Beneficios:** AWS brinda soporte sobre tu código de cloudformation en caso de que no despliegue tu integración, es decir brinda soporte sobre
 tu código si tienes el plan bussiness contratado.
- Integración nativa con todos los servicios de AWS.
- **Designer:** Te permite crear infraestructura de forma visual y si ya lo tienes creado, cargas tu plantilla y veras como luce.
- **Multicuenta:** Desplegar en 3 cuentas diferentes la misma infraestructura.
- **Flexibilidad:** Creación de recursos dinámicamente con custom resources.
- **Cloudformation:** Gratis, se te cobra por los recursos que este despliegue.
- **Escalabilidad:** Puede crecer desde el recurso mas simple hasta una arquitectura más compleja.
- **Seguridad:** Todos los despliegues están completamente asegurados, cifrado de llaves, etc.
- **Estabilidad:** Al ser administrado por AWS tiene un alto nivel de SLA.
- **Transaccional:** Espera a que todos los recursos estén creados para desplegar la aplicación, sino hará un rollback.

> Empresa que usan Cloud Formation: Barcelona FC, Expedia, Coinbase, nextdoor.

# Anatomía de un template en CloudFormation
- `AWSTemplateFormatVersion: '2021-09-09'`: [Opcional] Define las capacidades de la plantilla, si no es 
especificado. Amazon lo va a especificar con una versión por default (2010-09-09). 
- `Description: String`: [Opcional] Es un texto para describir la plantilla
- `Metadata: String`: [Opcional] Información adicional del template
- - AWS::CloudFormation::Init
- - AWS::CloudFormation::Interface
- - AWS::CloudFormation::Designer
- `Parameters: set of parameters`: [Opcional] Valores que se le pasan a la plantilla cuando se crea o actualiza
un stack. Pueden ser referenciados desde Resources u Outputs. 
- -  Ejemplos: 
```yml
Parameters:
    myKeyPair:
        Description: "Amazon EC2 key pair"
        Type: "AWS::EC2::KeyPair::KeyName"
    mySubnetIDs:
        Description: "Subnet IDs"
        Type: "List<AWS::EC2::Subnet::Id>"
```
```yml
Parameters:
    DbSubnetIpBlocks:
        Description: "Comma-delimeted list of three CIDR blocks"
        Type: CommaDelimetedList
        Default: "10.0.46.0/24, 10.0.112.0/24, 10.0.176.0/24"
```
```yml
Parameters:
    DbPort:
        Default: 3306
        Description: "TCP/IP port for the database"
        Type: Number
        MinValue: 1150 // Rango permitido
        MaxValue: 65535 // Rango permitido
    DbPwd:
        NoEcho: true // Valor Seguro (****)
        Description: "The database admin account password"
        Type: String
        MinLength: 1
        MaxLength: 41
        AllowedPattern: ^[a-zA-Z0-9]*$ //Cumplir expresión
```
- `Mappings: set of mappings`: [Opcional] Llave valor asociados que se usan para parámetros condicionales.
Similar a una tabla de búsqueda. Utiliza la función **Fn::FindInMap**
- - Ejemplo: Nosotros tenemos un servidor, ese servidor lo vamos a desplegar en tres regiones: Fráncfort, Sao Paulo y Virginia. El mapping lo que va a evaluar es la región donde se encuenttra y con ayuda del mapping
usa ese AMI evaluando el id de la imagen.
```yml
Mappings:
  RegionMap: 
    us-east-1: 
      "HVM64": "ami-0ff8a91507f77f867"
    us-west-1:
      "HVM64": "ami-0bdb828fd58c52235"
    eu-west-1:
      "HVM64": "ami-047bb4163c506cd98"
    ap-southeast-1:
      "HVM64": "ami-08569b978cc4dfa10"
    ap-northeast-1:
      "HVM64": "ami-05cd52961ce9f0d85"
```

### ¿Cómo quedaria nuestra función lambda usando parámetros? 
```yml
AWSTemplateFormatVersion: '2021-09-09'
Description: Mi primer lambda en Platzi

Parameters:
    NombreLambda:
      Description: Nombre de la funciónn lambda
        Type: String
       
    RuntimeLambda: 
      Description: Ingresa el runtime de la función lambda
      Type: String
      Default: python3.7
      AllowedValues: 
        - python3.7
        - python2.7
        - ruby2.5
        - nodejs8.10
        - java8
        - dotnetcore2.1
```

# Clase práctica creación de un template

[Formato yml para DynamoDB](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)

```yml
AWSTemplateFormatVersion: '2021-09-09'
Description: Mi primer lambda en Platzi

Parameters:
  DynamoAtributo: 
    Type: String
  NombreDynamo: 
    Type: String

Resources:
  DynamodesdeCero: 
    Type: AWS::DynamoDB::Table
    Properties: 
      AttributeDefinitions: 
        - AttributeName: !Ref DynamoAtributo
          AttributeType: S
      KeySchema: 
        - AttributeName: !Ref DynamoAtributo
          KeyType: HASH
      BillingMode: PAY_PER_REQUEST //On demand
      SSESpecification: 
        SSEEnabled: true
      TableName: !Ref NombreDynamo
      
Outputs: 
  NombreDynamo: 
    Value: !Ref DynamodesdeCero
    Export: 
      Name: NombreDynamo
```