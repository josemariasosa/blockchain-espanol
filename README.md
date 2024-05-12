# Blockchain en Español

***Para Alice.*** 🧿

## Introducción técnica a blockchain, o cadena de bloques.

```
1 byte == 8 bits
32 bytes == 256 bits
```

La blockchain es un nuevo tipo de bases de datos. Se trata de una nueva estructura de datos. La mayoría de quienes trabajan en el mundo de la tecnología digital habrán escuchado de SQL.

Ahora, se están proponiendo dos tipos nuevos de estructuras para almacenar información. La primera y la más importante es Bitcoin, con su algoritmo de prueba de trabajo (proof-of-work, o simplemente POW). Este algoritmo está construido siguiendo una estructura de UTXOs. 

Los UTXOs, del inglés Unspent Transactions Outputs, son un fragmentos de monedas que se encuentran dentro de la cadena de bloques, exclusivamente bajo el control de una llave privada.

Cada blockchain elige, al momento de iniciar en mainnet, la unidad más baja de cada una de las monedas. Por ejemplo, para bitcoin son 8 decimales y la unidad se conoce como satoshi.

```
Satoshi     (sats)	    Bitcoin	                U.S. Dollar (2024-may)
-----------------------------------------------------------------------
100,000     Satoshi     0.00100000 Bitcoin	    $63.672
1,000,000   Satoshi	    0.01000000 Bitcoin	    $636.723
10,000,000  Satoshi	    0.10000000 Bitcoin	    $6367.229
100,000,000 Satoshi	    1.00000000 Bitcoin	    $63672.291
```

Hay otras cadenas como ethereum y near que utilizan 18 y 24 decimales, respectivamente.

El método de almacenar información basado en UTXOs, en conjunto con la prueba de trabajo, permite llegar a un consenso entre de nodos, o servidores, sobre el estado de un conjunto de datos. En bitcoin, los datos son representados, por lo general, en transacciones que van de un dirección, una address, de un origen, hacia un destino final.

De esta manera se pueden dar a conocer la cantidad de monedas en circulación. Los incentivos del Bitcoin están alineados primero a la seguridad y descentralización, bajo consideración del trilema de blockchain. La escalabilidad está siendo directamente delegada a un mercado de segundas capas, más conocidas como L2s. Los bitcoins circulantes jamás serán más de 21 millones.

El protocolo de bitcoin permite la ejecución de pequeños chunks, o batches, de transacciones que se acomodan dentro de una estructura conocida como bloque. Un bloque está conformado por la siguiente información:

La fecha, o timestamp, en la que se llevó a cabo el acuerdo.
El hash de del bloque anterior. El hash de bitcoin es el resultado de la doble ejecución del algoritmo de SHA-256 el encabezado y las transacciones del bloque anterior.
Un valor nonce, o valor que se utiliza solamente una vez, que regrese un resultado válido del algoritmo matemático que permite la minería y creación de moneda nueva circulante, conocida como coinbase.

Posteriormente, se encuentra todo el ecosistema de ethereum. La innovación de ethereum fue la creación de una máquina virtual, conocida como la EVM, que permite la ejecución de programas más complejos, del tipo Turing completo, de los que permiten las cadenas basadas con la estructura de UTXOs.

El acceso a esta máquina virtual, que corre de manera descentralizada dentro de un cluster de nodos, o servidores; se lleva a cabo principalmente mediante el lenguaje de programación Solidity. Este lenguaje de programación, capaz de compilar para la evm, permite la creación de contratos inteligentes que corrieran dentro de una infraestructura coordinada.

Esta coordinación se logra mediante el algoritmo de prueba de apilamiento, proof of stake o POS, entre grupos de nodos que aseguran 32 ETH y validan que todas las transacciones cumplan las reglas previamente acordadas por todos los miembros. Estos nodos, o servidores, se conocen como nodo validador.

A su vez, existen también los nodos de ejecución, que permiten interactuar de manera descentralizada y sin la necesidad de permiso, permissionless, con la cadena de bloques que desee y utilice una máquina virtual de tipo evm. Los proveedores más famosos de nodos de ejecución de grado institucional son Infura y Alchemy, entre otras. Sin embargo, cualquier usuario con o sin balance de monedas de ether puede correr su propio nodo de ejecución, o si se prefiere contribuir con la descentralización de la red, corriendo su propio nodo validador.

```
Unit	                Wei         Value
----------------------------------------------------------------
Wei	                    1 wei	    1
Kwei (KiloWei/babbage)	10^3 wei	1,000
Mwei (MegaWei/lovelace)	10^6 wei	1,000,000
Gwei (GigaWei/shannon)	10^9 wei	1,000,000,000
microether (szabo)	    10^12 wei	1,000,000,000,000
milliether (finney)	    10^15 wei	1,000,000,000,000,000
ether	                10^18 wei	1,000,000,000,000,000,000
```

Ethereum es más que una cadena de bloques, ethereum es un ecosistema de estándares y código abierto que permite la creación de activos virtuales que puedan ser custodiados bajo una llave privada, o bajo la lógica completa de un contrato inteligente.

La máquina virtual de ethereum es modular, por lo que se permite el desarrollo independiente de múltiples áreas, que siempre serán capaces de llegar a un acuerdo, como protocolos que mejoran la seguridad y privacidad de los usuarios. O innovaciones en escalabilidad, como las propias L2s de ethereum basadas en la tecnología de rollups, que se pueden clasificar en dos tipos principalmente:

Rollups optimistas, que poseen un algoritmo para resolver disputas en alguna transacción en particular, se conocen como Fraud Proof, o prueba de fraude.
ZK Rolloups. Rolloups que utilizan la tecnología de zero knowledge, o de conocimiento cero, que permiten generar bloques que puedan ser validados criptográficamente, sin la necesidad de pasar por un periodo para evaluar la prueba de fraude, que a veces alcanza los 7 días.

Ethereum no utiliza una estructura basada en UTXOs, sino que utiliza un enfoque basado en la cuenta cuenta de un usuario, o account. Por lo general, un account en ethereum luce de la siguiente manera:

```
0xA9D1e08C7793af67e992fe308d5697FB1234567b (no enviar nada a esta dirección)
```

Las cuentas, conocidas también como EOAs que significa en inglés, Externally Owned Account, o cuentas controladas por un usuario.

Pero también existen cuentas que son controladas exclusivamente por código que corre y se valida dentro de la blockchain. Este código existe dentro de un contrato inteligente que dicta los roles, actividades, balances y cualquier información de una cuenta. El contrato inteligente de Compound para USDC en ethereum mainnet es: 

```
0xc3d688B66703497DAA19211EEdff47f25384cdc3
```

Un contrato permite correr lógica sencilla, tanto para la transferencia, acuñar, comprar y vender tokens basados en el estándar de ERC-20. Pero también, es posible la elaboración de complejos protocolos que permiten una automatización que genere resultados determinísticos y seguros para los usuarios. Como: Compound, MakerDAO, Aave, Decentraland, Meta Pool, entre muchas otras.

Los principales casos de uso son financieros, pero también abre un abanico para otros casos de uso como juegos, arte, derechos de autor, trazabilidad, entre otros.





