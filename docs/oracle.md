Utilizamos un trie para almacenar todas las preguntas que se han hecho del oráculo.
Usamos otro trie para almacenar las respuestas, para cualquier pregunta que fue contestada.
Utilizamos un trie para almacenar todas las preguntas que se le han hecho al oráculo.
Usamos otro trie para almacenar las respuestas, para cualquier pregunta que fue contestada.

Para las preguntas que están en el proceso de respuesta, almacenamos un mercado en el estado en cadena.
El mercado recuerda cuántas acciones de cada tipo se han vendido, y recuerda cuál era su liquidez inicial, y debería tener un libro de órdenes.

El mercado tiene 4 resultados posibles:

1) la dificultad sube, y el resultado del oráculo es verdadero
2) la dificultad sube, y el resultado del oráculo es falso
3) la dificultad baja y el resultado del oráculo es verdadero
4) la dificultad baja, y el resultado del oráculo es falso

*** De alguna manera, necesitamos saber cuántas acciones de cada tipo posee cada cuenta.

La liquidez inicial se recopilará utilizando un contrato de garantía dominante fuera de la cadena.

El resultado del oráculo se mide mirando la correlación entre los resultados.
Sumamos las diagonales, y vemos qué camino es más grande.
Si la correlación está en la misma dirección para suficientes bloques, entonces ese es el resultado del oráculo.
Dado que usamos un libro de pedidos, es caro para los atacantes DDOS mover el precio más allá del 50% cada vez que el oráculo está casi terminado.


Deberíamos pagar al jugador de una sola vez, porque sólo un fork puede sobrevivir.
Cuando un jugador quiere ser pagado, necesitan una manera de probar cómo apuestan.
*** Tal vez deberíamos tener una raíz merkle de apuestas en cada cuenta?
