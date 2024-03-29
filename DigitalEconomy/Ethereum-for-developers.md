# ¿Qué es Ethereum? 
Ethereum es la plataforma descentralizada que se basa en la tecnología blockchain que trajo consigo Bitcoin. Es una plataforma para ejecutar contratos inteligentes
(smart contracts) a través de una computadora virtual (EVM) y utiliza una criptomoneda llamada Ether (ETH) para medir y restringir los costos de ejecución.

La red Ethereum comparte muchas cosas con la red de Bitcoin, siendo una de ellas que ambas son redes open blockchain.
Esto significa que cualquier persona puede participar en la creación e interacción dentro de ellas, mientras tenga un dispositivo adecuado con acceso a internet,
por lo que se considera que son resilientes a la censura.

## ¿Para qué sirve Ethereum? 
El propósito de su creación, según sus propios autores, es ser una herramienta para poder brindar un ambiente de trabajo determinado y seguro donde se puedan programar
aplicaciones descentralizadas. Esto sin necesidad de construir la infraestructura base de algoritmos de consenso y redes de persona a persona para cada nueva aplicación.
Básicamente, facilitar el desarrollo de proyectos que aprovechen la tecnología blockchain.

La implementación de los smart contracts es su característica más popular (fue la primera red en concebirlos) y la idea principal para hacer de esta red algo más
interesante que la propuesta original de Bitcoin, al permitir el desarrollo técnico de aplicaciones con su propio lenguaje de programación
“orientado a contratos”: Solidity. Técnicamente, **esto se le conoce como “turing completo”**, algo de lo que la red de Bitcoin carece.

### Ethereum vs. Bitcoin 
- Ethereum -> Turing Completo: La moneda cumple una función para un objetivo más amplio
- Bitcoin -> Turing incompleto: Limitado a ser un sistema monetario superseguro

## Su historia desde el comienzo 
- Publicación del White Paper por Vitalik Buterin (2013)
- Publicación del Yellow Paper por el Dr. Gavin Wood, co-fundador y CTO de Ethereum (2014)
- Presale de la ICO de Ethereum (Julio 2014)
- Frontier, el despliegue de la primera etapa de cuatro fases de desarrollo programadas (30 de julio de 2014)

Desde su planificación, los creadores decidieron que Ethereum tendría una ruta de desarrollo progresiva hasta una transición final, donde se cambiaría a
un consenso distinto al de Bitcoin. Las versiones principales antes de su versión final fueron las siguientes:
- Frontier (2014)
- Homestead (2016)
- Metropolis (2017)
- Serenity (Ethereum 2.0)

## Ethereum 2.0 
- Transición de PoW a PoS
- Beacon Chain (dic 2020)
- PoS validators
- Shard Chains

Se espera mucho de esta innovadora propuesta, y a pesar de los obstáculos, se cree que será una de las redes que, junto con Bitcoin,
cambiarán la forma en la que interactuamos y hacemos transacciones de todo tipo dentro de Internet.

> Contribución creada con los aportes de: Luis E. Herrera

# Componentes de Ethereum 

1. **Red P2P:** Es la red que permite la comunicación y envío de datos entre un usuario y otro sin necesidad de un intermediario.
 Aunque en realidad es más complejo que eso, se puede entender que los canales dentro de una red P2P son compartidos y anónimos, es decir, los usuarios no tienen
 que conocerse entre ellos para poder hacer uso de estos canales, y no hay un control respecto a qué datos son tomados como prioridad o con algún privilegio (o censura).

2. **Algoritmo de consenso (consenso de Nakamoto):** Fue el mismo de Bitcoin hasta la aparición de Ethereum 2.0, y no es más que la forma en la que se acordó cómo
 se actualizaría la información dentro de la red, de manera que se evitara la inserción de datos de manera arbitraria y creando un sistema protegido contra los intentos
 de corrupción.
 
3. **Ether:** Es la criptomoneda nativa del proyecto. Sirve para muchas cosas, además de tener un valor como lo tiene Bitcoin. En ella se basan todas las
  operaciones que tienen lugar dentro de la red, basadas en transacciones que se realizan con ayuda de otros instrumentos.
  
  > Es importante diferenciar entre Ether y Ethereum. Ether es la moneda y Ethereum es la red.
  
4. **Ethereum Virtual Machine (EVM):**  Es el software creado para servir como una computadora que se aloja en la nube, con el propósito de procesar los
   programas que funcionan en la propia red.

5. **Algoritmo criptográfico de seguridad (Ethash):** Es la herramienta creada a partir de una aplicación matemática que brinda una protección a todo el sistema, 
sin la cual, la seguridad de una red incorruptible no existiría.

6. **Clientes (Gethm Parity):** Son los paquetes de conexión que permiten funcionar como un nodo que aloje la información de la red, así como interactuar con ella.

## Conceptos relevantes de Ethereum

- **Clientes/Nodos:**  Los clientes son los encargados de empaquetar el sistema sobre el cual se puede ejecutar un nodo en la red BlockChain.
 Cuando instalas en tu computador este cliente, automáticamente te conviertes en un nodo participante en la red de Ethereum.

- **Walletes:** Las wallets o billeteras son aplicaciones que nos permiten administrar nuestras cuentas de Ethereum o de cualquier otra red, para poder
 interactuar con otras personas que también sean parte de esta red. Además de controlar nuestros fondos y activos.

- **Smart Contracs:** Son los programas que nos permiten comunicarnos con la blockchain a partir de ciertas condiciones especificadas dentro del contrato inteligente.
 Estos contratos se ejecutan dentro de la EVM para ser analizados y posteriormente implementados en la blockchain

- **Web3:** Es una nueva web descentralizada sobre la cual no necesariamente va a existir un ente central, sino que al ser una red descentralizada o P2P los usuarios
 son los encargados tomar decisiones autónomas sin necesidad de recurrir o de pedir información a un ente central.

## La base de Ethereum 

Para poder entender cómo es que se interactúa con esta blockchain, primero hay que saber que todo se maneja a través de transacciones.
Aquí es donde entra el Ether, así como los componentes que regulan su administración y el uso de la red para una correcta distribución de los datos,
evitando la congestión del tráfico en las transacciones. Para ello, es necesario conocer el concepto de “gas”.

> Contribución creada con los aportes de: Luis E. Herrera y Johan Muñoz

# La moneda ETH y el Gas

Ether, también conocida como ETH, es la moneda nativa de la red de Ethereum. Sirve para hacer transferencias de valor,
pagar a los mineros, correr programas y como mecanismo de seguridad contra potenciales errores en la máquina virtual
EVM (Ethereum Virtual Machine) a través del GAS.

## El gas en Ethereum 

La unidad de medición principal para el Ether se llama “Gwei” en honor a un ingeniero informático chino, Wei Dai,
quien contribuyó con aportes en el área de la criptografía dedicada a las criptomonedas. Esta unidad se divide a
su vez en “wei”, la unidad mínima, de la cual se necesitan 10^18 para completar un Ether.

Entonces, otro concepto a conocer bien es el de “gas”, que se refiere a una cantidad de Ether en dichas unidades
para poder interactuar con la red de Ethereum, y que como su nombre alude, sirva como gasolina para alimentar a la EVM. 
En otras palabras, se debe pagar por cada transacción que se conecte a la blockchain, una pequeña tarifa para hacer
uso de esta máquina virtual.

Esto es necesario, ya que la EVM, al tratarse de una computadora en términos prácticos, es susceptible a los percances
que podría ocasionar el código, como bucles infinitos y bugs que afecten su correcto funcionamiento.
Así, con el gas se puede asegurar un proceso delimitado por su duración, y de esta forma evitar que este tipo
de fallas perdure sin control alguno.

> Contribución creada con los aportes de: Luis E. Herrera.


# Etapas de desarrollo y actualizaciones programadas

## 4 Etapas de desarrollo de Ethereum

Estas son las 4 actualizaciones programadas de Ethereum: 

- Frontier
- Homestead
- Metropolis
- Serenity -> Ethereum 2.0

Estas actualizaciones están subdivididas en distintas actualizaciones que 
responden a problemas que van surgiendo en el momento. Algunas de ellas se hacen a 
través de consenso de toda la red y muchas se tienen deben ejecutar a través de un 
fork.

## Los forks en Ethereum

La ruta de desarrollo de estas nuevas versiones consiste en diversas bifurcaciones 
del código mismo (forks), que se refiere a que se crean ramas independientes, en 
donde la versión anterior y la nueva se separan para tomar cada una su propio 
camino. De esta manera, es posible seguir desarrollando cada una sin afectar a la 
otra, claramente con el fin de poder seguir mejorando a la nueva versión.

En el 2016, sucedió un ataque a la red de Ethereum, por lo que tuvo que realizarse 
un fork para reestablecer la seguridad de la blockchain. Desde entonces, permanece 
esa versión vieja bautizada como “Ethereum Classic”, que todavía mantiene pocos 
adeptos, a pesar de que la gran mayoría de los que participan en este proyecto 
hacen uso de la que simplemente se conoce como la red Ethereum.

> Contribución creada con los aportes de: Luis E. Herrera


# ¿Qué es la criptografía asimétrica?

La criptografía es la práctica y el estudio de métodos para proteger información a 
través de codificar mensajes. Por su parte, la criptografía asimétrica es 
posiblemente el aspecto más importante de cualquier blockchain, ya que a 
diferencia del pasado, no se requiere una llave única que deban compartir el 
emisor y receptor para generar un canal de comunicación segura.

Este tipo de criptografía consiste en la creación computada de una serie de 
caracteres al azar, que servirán como “llaves”. La generación de esta serie de 
letras y números depende de un algoritmo basado en principios matemáticos, los 
cuales otorgan seguridad a los sistemas como la blockchain.

## ¿Cómo funciona la criptografía asimétrica?

Básicamente, se trata de la creación de una serie de caracteres a partir de una 
llave privada (una serie elegida al azar), las cuales estarán mutuamente 
correlacionadas, y que para los procesos de verificación, solo podrán ser 
comparadas correctamente entre ellas.

Por ejemplo: si se quisiera encriptar un mensaje secreto para enviarlo sin temor a 
que pudiera ser interceptado, lo que se haría con ayuda de la criptografía 
asimétrica, sería cifrar el mensaje con la llave generada por la llave privada del 
destinatario, es decir, la llave pública. Esta llave es, por cierto, la que se 
puede compartir con este fin.

Después de llegar a su destino, el remitente tendría que descifrar el mensaje con 
su llave privada (que solo debe conocer el remitente), con la que se creó la llave 
pública que encriptó dicho mensaje. Solo esta llave puede “desbloquear” el 
contenido, y es virtualmente imposible, con el poder de cómputo actual, tratar de 
romper la seguridad de este cifrado. Es lo que hace a la criptografía de este tipo 
tan poderosa y útil.

## Qué es la función HASH

Técnicamente, existen funciones informáticas para este tipo de cifrado llamadas 
funciones hash, las cuales se encargan de encriptar los datos que se pasen a la 
computadora y convertirlos en un solo código de un tamaño determinado, sin 
importar la extensión del contenido original. Sirven para proteger las cuentas y 
los balances de los usuarios de blockchain.

Con este concepto primordial abordado, ahora es más fácil entender el poder de las 
matemáticas aplicadas a la privacidad de nuestros datos, y reconocer el papel tan 
crucial para el funcionamiento de las redes blockchain.

> Contribución creada con los aportes de: Luis E. Herrera.

# ¿Qué son las Wallets?

Las wallets son un software o dispositivo encargado de administrar las llaves de 
un usuario. Estas no alojan los activos, solo son un puente para que su dueño 
pueda interactuar con su cuenta de Ethereum en la red blockchain, y así permitirle 
hacer uso de las distintas aplicaciones en la red con sus activos de forma segura.

En Ethereum se manejan los activos a través de la autenticación con las llaves 
(sin importar la identidad real del usuario), por lo que es fundamental cuidar 
ambas llaves, en especial de la privada, ya que al exponer o extraviar ambas se 
corre el riesgo de no poder recuperar los activos en dicha cuenta.

Ninguna wallet o empresa podrá hacer algo al respecto (aquí entra la ya famosa 
frase: “Your keys, your coins. Not your keys, not your coins”).

## Conceptos importantes de las wallets

- **Accounts:** Son los registros dentro de Ethereum que poseen un balance en ETH, 
y que son administradas por las entidades (ya sea personas o programas) que poseen 
sus respectivas llaves para poder hacer transacciones.
- **Transacciones:** Una instrucción controlada por una cuenta que cambia el
estado del sistema.
- **Firmas digitales:** Es una cadena de carácteres producida a partir de un texto 
con el hash de una llave privada.
- **Tokens:** Es un tipo de moneda o activo con una utilidad o distinción que 
puede ser rastreado y transferido, y cuyo valor (que puede ser nulo) depende de su 
proyecto padre y el ether.

Recuerda, la función de las wallets solo es administrar las llaves vinculadas a 
una cuenta y dar acceso a la blockchain, no el de salvaguardarlas. Por lo que la 
responsabilidad de esto recae cien por ciento en el representante de la cuenta.

> Contribución creada con los aportes de: Luis E. Herrera.


# ¿Qué son los Smart Contracts?

El término smart contracts se le ocurrió a un desarrollador llamado Nick Szabo, 
que contribuyó precisamente con la idea de programas especiales que se ejecuten 
redes descentralizadas con criptografía.

Más en detalle, un smart contract es un programa o protocolo que se ejecuta de 
forma automática y descentralizada dentro de una blockchain, y sirve para 
controlar una acción o documentar un evento de acuerdo a los parámetros del código 
que lo componen.

## ¿Qué usos tiene un smart contract?

El objetivo de los smart contracts es evitar la necesidad de confiar en un tercero 
para evitar la intermediación en los procesos, y así:
- Abaratar costos
- Reducir tiempos de operación
- Minimizar fraudes

Dicho de otra forma, son herramientas informáticas que ayudan a cumplir 
efectivamente tareas en las que el humano podría intervenir con malas intenciones 
o simplemente, sin el debido cuidado.

La utilidad de estos programas se pueden imaginar en distintas ramas de la 
actividad humana, pero es más notorio su efecto y los beneficios dentro del mundo 
de las finanzas (DeFi).

> Contribución creada con los aportes de: Luis E. Herrera.

# Qué es DeFi o finanzas descentralizadas

**DeFi significa finanzas descentralizadas.** Es muy probable que las finanzas 
tradicionales se vean muy afectadas por el uso de los smart contracts y las 
plataformas que están siendo construidas en blockchain. Esto porque en teoría, 
según varias escuelas del pensamiento económico, los sistemas monetarios funcionan 
mejor al no estar controlados por un ente central. Así se desarrolla un mercado 
más libre y más fructífero.

## Los actores dentro de DeFi

Hay diferentes elementos y áreas en el ecosistema DeFi, como por ejemplo:
- Decentralized Exchanges (DEX)
- Stable coins
- Préstamos
- Seguros
- Derivados (contratos)
- Margin trade
- Oráculos

## Ejemplo de uso de DeFi

La idea es aplicar la filosofía de “cero intermediarios” para poder usar servicios 
financieros diversos. No solo esto, sino también poder desarrollar mecanismos 
internos que aceleren la gestión de sistemas que incrementen los beneficios, algo 
que en las finanzas tradicionales tardaría mucho más tiempo en hacerse posibles.

Algunos de esos elementos, como los stable coins, ayudan a proveer una estabilidad 
al mercado aun volátil de las criptodivisas. Otros son propuestas que facilitan el 
intercambio de estos activos como lo sería en el sistema fíat tradicional, tanto 
de forma controlada (DEX) como de forma arriesgada a cambio de ganancias 
inmediatas (trading).

Hablando de oráculos, estos son sistemas de distinta complejidad que proveen 
información del mundo real a las blockchain con el fin de darles una utilidad que 
sea relevante. Con esto, los smart contracts pueden generar cambios reales en 
algún contexto cotidiano, por ejemplo.

> Contribución creada con los aportes de: Luis E. Herrera.

# Qué es un NFT. Non-Fungible Token

Actualmente, un *NFT* (Non Fungible Token) tiene la reputación de ser algo que puede ser vendido por mucho dinero si se logra convencer al
mercado de su “valor”.

Sin embargo, el propósito va mucho más allá. Si bien, un NFT puede representar algo tan simple y subjetivo como un activo sin valor útil (obras de arte), 
también puede representar algo único que sí sea de utilidad en el mundo real.

## Qué es un NFT

“Fungible” implica que es algo que puede ser replicado una indeterminada cantidad de veces, y puede seguir valiendo lo mismo. Un buen ejemplo es la 
acuñación de monedas, que a diario se hacen monedas, pero no pierden su valor aun habiendo tantas iguales. Para el sistema monetario esto es un beneficio ya
que si fueran no fungibles y rastreables, el valor podría ser subjetivo a lo que las personas le asignen dependiendo su procedencia.

Un NFT es algo que por definición no puede ser replicado, y aunque pueda ser copiado de alguna forma (tal y como es posible copiar y 
pegar una imagen JPG, por ejemplo), este viene con un certificado de autenticidad dentro de la blockchain, sustentado en un smart contract.

**A este tipo de smart contract en Ethereum se le conoce como ERC-721, que es un estándar diseñado específicamente para NFT.** 
Con este, se crea un token que se vincula a cierto artículo que se quiera autenticar.

Los creadores de contenido, artistas y deportistas han encontrado en los NFT una vía para poder compartir y vender sus creaciones de forma directa sin
tener que depender de nadie para su distribución y su verificación, generando mayores ganancias para ellos.

Aunque, por supuesto, puede hallarse una finalidad mucho más noble para los NFT que realmente transforme las dinámicas sociales en un contexto más
serio y profundo.

> Contribución creada con los aportes de: Luis E. Herrera.

# Qué son las aplicaciones descentralizadas o dApps

Las aplicaciones descentralizadas, también conocidas como dApps, son aquellas que no dependen de un servidor central para funcionar y mantenerse,
sino de los mismos usuarios.

## ¿En qué consisten las aplicaciones descentralizadas?

Las aplicaciones descentralizadas se organizan a través de los mecanismos del consenso dentro de la blockchain, involucrando
a todos los participantes de la red que usen cierta dApp, sin que una entidad central se apropie de la red ni intervenga o manipule los datos.

El principal atractivo de estas aplicaciones es precisamente que los datos personales no pasan por el control de un servidor concentrado, 
el cual es el responsable de administrar este tipo de información y cuenta con total acceso a ella, abriendo la posibilidad a un uso ilimitado
e inmoral, en algunos casos.

Esto también implica que los participantes tomen decisiones respecto a la dApp de forma equitativa.

Las aplicaciones descentralizadas cambian totalmente el paradigma de cómo se usan las aplicaciones de software y brindan una mayor seguridad y protección de la 
información privada, además de una genuina participación, si así se desea.

> Contribución creada con los aportes de: Luis E. Herrera.


# Proof-of-Work, Proof-of-Stake y sistemas híbridos

Los algoritmos de consenso son los encargados de coordinar y organizar la red de forma que los usuarios puedan 
interactuar con ella sin arbitrariedades ni aplicaciones donde el control sea de un solo actor.

La prueba que necesita la red para que los participantes crean, compartan y hagan transacciones de manera justa
con ciertos requerimientos hacia los usuarios con el fin de que la red sea sustentable.

## Qué es el consenso Proof of Work

El primer consenso que se conoció se llama ***Proof of Work (PoW)***, y se trata de un mecanismo que implementó Bitcoin, 
para poner en funcionamiento el proyecto distribuido y descentralizado.

Se trata de un sistema en el que la creación de la criptodivisa se da a partir de un gasto energético, proveniente de
las computadoras que están conectadas como nodos completos dentro de la red llamados mineros.

Los nodos que deseen participar en este “juego”, deben realizar un trabajo computacional para poder tener la oportunidad 
de insertar un bloque a la gran cadena de transacciones (básicamente a la base de datos que conforma la red).

Quien pueda resolver lo necesario para hacerlo, gana esa tarea para así obtener una retribución monetaria por cada
bloque generado, pagado con la misma criptodivisa.

Este consenso, si bien es efectivo, no deja de tener ciertos problemas. En primer lugar, se habla del alto
costo energético, ya que requiere miles de computadoras consumiendo la energía necesaria para un proceso
altamente exigente.

Sin duda, esto causa un impacto perjudicial para el medio ambiente, además de otras cuestiones relacionadas
con la seguridad de la red y su escalabilidad.

Proof of Work es el resultado de décadas de investigaciones previas al Bitcoin, con la intención de poder crear redes
de comunicación equilibradas, en las que no haya posibilidad de congestiones de datos que provoquen saturación en la
red, al solicitar una prueba de gasto energético si se quiere interactuar o enviar información a través de la misma.

## Qué es el consenso Proof of Stake y los sistemas híbridos

Ethereum quiso mejorar este consenso, con ayuda de uno nuevo Proof of Stake (PoS). Este protocolo cambia a los
mineros en el PoW por un plan de participación “accionaria” en el que al azar, los nodos que cuenten con cierta
cantidad de Ether, tienen derecho a convertirse en validadores, que serán los que inserten bloques nuevos a la 
cadena de bloques.

Esa cantidad de Ether estará congelada, así se garantiza que si el nodo intenta algo malicioso, perderá sus fondos.

Se espera que sea un consenso que ciertamente sea más amigable para el medio ambiente, que incentive a una mayor
incorporación de nuevos usuarios, mejorar la seguridad y las penalizaciones contra ataques, y brindar en general
una escalabilidad más rápida.

Por supuesto, existen otros protocolos como son los sistemas híbridos, que no son más que combinaciones con 
características de estos u otros consensos, incluyendo aquellas propuestas que aún carecen de la credibilidad
de la comunidad en el ecosistema.

> Contribución creada con los aportes de: Luis E. Herrera.


# Ethash y Casper

Existen diferentes mecanismos de consenso. Antes de Ethereum 2.0, el protocolo de consenso usado era “Ethash”,
este es con el que se cifran los bloques y se insertan a la cadena. Con la llegada de PoS (Proof-of-Stake), Ethereum
hará uso de un nuevo protocolo llamado “Casper”.

## Qué son los mecanismos de consenso Ethash y Casper

Ethash es el algoritmo que utiliza la blockchain de Ethereum para minar y proteger a su red, el cual hace uso
de un alto consumo energético para asegurar mayor protección y defenderla de posibles atacantes.

Sin embargo, Ethereum busca hacer transición a Casper, un mecanismo de consenso que no requiere de 
ese consumo energético.

Lo que se busca es dejar de validar bloques y transacciones con Ethash y empezar a usar un mecanismo de PoW
(Proof of Work) para validar las transacciones y con el que los nodos se van a ganar el derecho a participar
en el juego del mecanismo descentralizado para actualizar la base de datos, sin necesidad de una autoridad central.

Esta transición es lo que se conoce como Ethereum 2.0.

# Qué es un Fork en blockchain

La traducción literal de fork al español es “tenedor”. En blockchain, fork hace referencia a lo que sucede cuando
una base de datos sufre un desacuerdo o se hace una actualización que no es compatible con el pasado, esto produce
una bifurcación en el código central de un software.

El tenedor parte de una agarradera (rama principal) hacia las puntas en las que se divide. El código toma diferentes
caminos y, dependiendo de su propósito, estos siguen o pierden continuidad. Por lo tanto, las ramificaciones heredan
las características de la rama principal, pero la diferencia radicará en las variaciones y los cambios que propiciaron 
dichas divisiones en primer lugar.

En cuanto a las blockchain, estas se generan debido a un desacuerdo o la incompatibilidad entre los participantes
respecto al consenso. Al iniciar una nueva rama o más, siguen su desarrollo hasta que se formaliza su invalidez, o su 
mantenimiento cese.

## Entonces, ¿cuál camino elegir?

Es importante recalcar que la mayoría de los participantes estén de acuerdo con lo que se haga dentro de las
plataformas, así se conserva la intención de proporcionar una comunidad lo más estable posible. Claro, es posible 
pertenecer a más de una comunidad si se desea, hay que recordar que estas redes son de libre asociación.

La organización descentralizada es algo relativamente nuevo, por lo que las dinámicas aún son algo por descubrir.
Sin embargo, eso no impide que se busque una armonía entre los que quieran cambios, y los que prefieren ser más 
conservadores.

> Contribución creada con los aportes de: Luis E. Herrera.

# Qué es EIP y soluciones de escalado

EIP (Ethereum Improvement Proposals) o propuestas de mejora son protocolos para evitar, en lo posible, divisiones y desacuerdos, facilitando la
implementación y evitando que haya forks.

En estas propuestas de mejora se estipulan cambios que justifiquen debidamente una transición que pueda ser necesaria. Es por eso que se ha dado
el cambio progresivo de Ethereum a PoS, aunque cualquiera que tenga alguna otra teoría más efectiva que pueda comprobar ante la comunidad,
puede terminar aportándola para su desarrollo.

## Qué son las soluciones de escalado

Algo sumamente crucial para la adopción de estas tecnologías, es el tema de cuánto alcance tienen sus características para que la gente en general
decida hacer uso de ellas. Además de la seguridad, la meta es mejorar la usabilidad en términos prácticos, como la velocidad de las transacciones.

Es necesario que se empiecen a realizar transacciones cada vez más rápidas, y compararlas con las del sistema tradicional, o incluso superarlas.
La naturaleza de las blockchain es algo que todavía no ha definido la totalidad de su potencial, aunque ya hay propuestas que tratan de
resolver este inconveniente.

En 2022, bitcoin tenía la posibildiad de hacer 7 transacciones por segundo, Etherum 30 y Visa 1700. Por lo que es muy necesario que se puedan 
efectar más transacciones sin comprometer otros aspectos de la red, como seguridad y descentralización. 

Entre las estrategías para el escalado de la red, en general, en ciencias de la computación se conoce como **Sharding**:
> Sharding se refiere al prcoeso de fragmentación de una base de datos o motor de búsqueda, para aligerar la concentración de recursos y facilitar funciones. 

Una implementación que actualmente (2022) esta funcionando en Ethereum es **The Beacon Chain**.
> Es una cadena paralela a la Blockchain de Ethereum que sirve para validar transacciones y bloques con un sistema de PoS.


En Ethereum existen por ejemplo:

- Polygon (MATC)
- Raiden Network (LN)
- xdai (sidechain)
- Optimism (OVM Rollups)
- zkSync (scalable skRollups)

Estas propuestas se aplican en un ámbito paralelo al de la red principal, a modo de una segunda capa del código 
fuente de Ethereum (layer 2). Sin duda, hay todo un trabajo tras bambalinas que dará paso a nuevas y emocionantes posibilidades.

>  L2 Solutions. Soluciones de segunda capa. Porque la primer capa, la capa original de Ethereum (la cadena de bloques original) es descentralizada y segura.
>  Y no se quiere comprometer eso, por lo tanto se le añaden capas como soluciones para no comprometer la seguridad de la red base.

> Contribución creada con los aportes de: Luis E. Herrera.
