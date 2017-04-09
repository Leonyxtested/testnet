¿Qué pasa si alguien paga dinero en el mercado que usamos como un oráculo para tratar de conseguir que mienta?

Ejemplo: estábamos apostando a un partido de fútbol, pero ahora el juego ha terminado y todos sabemos que Alice ganó.
El resultado correcto es que la decisión A es 99.99% probable que sea la horquilla de la cadena bloque con alta dificultad, y la decisión B es 0.01% probable que sea la horquilla con alta dificultad.
Un atacante sigue comprando B para empujar el precio por encima del 50%.
Los defensores se muestran para comprar acciones de A en uno-a-uno las probabilidades.
Los atacantes poseen muchas fichas en la horquilla A, y actualizan su software para usar la horquilla A.
Los defensores poseen muchas fichas en el tenedor B, y actualizan su software para usar el tenedor B.
Todo el mundo prefiere el tenedor que es honesto, porque quieren un tenedor con un oráculo de trabajo.
Es el punto de bombardeo.

Cuando el precio es 50-50, el acto de defender tiene esta tasa de retorno:

`1- (tasa de interés * finalidad)`

Cuando el tipo de interés es la tasa de mercado, debe pagar a alguien que esté dispuesto a mantener Aeons por un tiempo y no pueda acceder a ellos.
Finalidad es la cantidad de tiempo hasta que las apuestas pagan.
Los defensores sólo defenderán si obtienen ganancias, por lo que el oráculo sólo es seguro cuando

`(tasa de interes * finalidad) <1`.


Blockchains son pequeños e inestables, por lo que la tasa de interés debe ser una cantidad muy alta de 10% al mes, que es de alrededor del 0,3% por día.

La cantidad de tiempo hasta que las apuestas pueden pagar debe ser más largo que el período de retargetting de dificultad.
De esta forma, la cadena de bloques puede conocer la demanda de monedas.
En bitcoin, el período de retargetting es de 2000 bloques, que es aproximadamente una semana.
Así que vamos a establecer nuestra finalidad a 7 días = alrededor de 2,5% de interés

Conectando a la fórmula:

`(0,025 * 1) <1`

Cual es verdad. Así que es seguro.




Además de usar los mercados para decirnos cosas binarias verdaderas / falsas, también hacemos las preguntas del oráculo con menos certeza. Por ejemplo: "Si duplicamos el tamaño de los bloques, ¿eso hará que las monedas sean más o menos valiosas?"
Dependiendo del precio, actualizamos el protocolo.
¿Qué tan valioso debe ser un cambio para que podamos medirlo?

Digamos que el precio debe ser X, que está entre 0,5 y 0.
Un atacante sigue presionando el precio a 0,51, por lo que cambiar el resultado y forzar el protocolo para actualizar lo que le gusta.
Los defensores ganan por defender es

`1 - (2 * X) - (interest_rate * finality)

= 1 - (2 * X) - 0,025`

El defensor sólo defenderá si esto es positivo, así que

`0,975 - 2X> 0 

X <0,975 / 2

X <0,4875`

Así que el atacante sólo puede empujar el precio un máximo de `(interest_rate * finality) / 2`
Si empuja más que eso, entonces se convierte en rentable defenderse contra la manipulación.

Si sólo tenemos <2% de confianza en que la decisión A es mejor que B, entonces no es importante la decisión que tomamos. No importa si no podemos evitar esas pequeñas manipulaciones.
