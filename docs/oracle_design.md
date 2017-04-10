Utilizamos un trie para almacenar todas las preguntas que se han hecho del oráculo.
Usamos otro trie para almacenar las respuestas, para cualquier pregunta que fue contestada.

Para las preguntas que están en el proceso de respuesta, almacenamos un mercado en el estado en cadena.
El mercado recuerda cuántas acciones de cada tipo se han vendido, y recuerda cuál era su liquidez inicial, y debería tener un libro de órdenes.

El mercado tiene 6 resultados posibles:
1) la dificultad sube, y el resultado del oráculo es verdadero
2) la dificultad sube, y el resultado del oráculo es falso
3) la dificultad baja y el resultado del oráculo es verdadero
4) la dificultad baja, y el resultado del oráculo es falso
5) la dificultad sube, y el resultado del oráculo es mala respuesta
6) la dificultad baja, y el resultado del oráculo es mala respuesta

Cada mercado debe tener un trie para almacenar órdenes en el libro de órdenes, y debe tener un trie de cuentas, para recordar cuánto dinero tiene cada cuenta.

Todas las raíces del mercado deben combinarse como un merkle trie en el bloque, de modo que a medida que el número de mercados crece por N, el aumento en el costo es sólo O (log (N)).

También necesitamos mantener un registro de cuántas órdenes abiertas existen a cada precio, de esa manera el fabricante del bloque no puede censurar ningún oficio.

En total, eso fue 6 intentos:
* Preguntas. Cada bloque tiene una raíz
* Respuestas. Cada bloque tiene una raíz de esta
* Operaciones de libros de pedidos
* Cuántas acciones posee cada cuenta
* Un trie que almacena pares, que contienen uno de los dos tipos anteriores de raíces, un libro de órdenes de la raíz, y una cuenta de acciones-raíz. Cada bloque tiene una raíz de esto.
* Cuántas órdenes abiertas en cada precio

Las raíces en cada bloque deben combinarse para formar una sola raíz que se almacena en el bloque hash.

El resultado del oráculo se mide mirando la correlación entre los resultados.
Sumamos las diagonales, y vemos qué camino es más grande.
Si la correlación está en la misma dirección para suficientes bloques, entonces ese es el resultado del oráculo.
Dado que usamos un libro de pedidos, es caro para los atacantes DDOS nosotros moviendo el precio más allá del 50% cada vez que el oráculo está casi terminado.


Tx tipos:
Pregunta
OracleBet
OracleFinish
Recoger la recompensa

Pregunta
Esto cuesta un gran depósito. Si la pregunta se responde de la manera esperada, obtiene la mayor parte del depósito de vuelta.
Si deciden que es una mala pregunta, su depósito se elimina.

OracleBet
Así es como usted hace una apuesta en el mercado de la cadena, que mide la correlación entre las respuestas a las preguntas del oráculo, y la dificultad de la minería. Es un libro de órdenes LMSR, por lo que usted dice cuántas acciones por el precio más bajo está dispuesto a vender, o cuántas acciones por el precio más alto que está dispuesto a comprar.

Pregunta de respuesta
Si la correlación del oráculo ha demostrado con un margen suficientemente alto durante un período suficientemente largo de tiempo que una respuesta es preferible, entonces cualquier persona puede hacer esta transacción para registrar permanentemente la respuesta a la pregunta.

Recoger la recompensa
Si has hecho una apuesta ganadora, así es como recaudas tus ganancias.


La liquidez inicial se recopilará utilizando un contrato de garantía dominante fuera de la cadena.
