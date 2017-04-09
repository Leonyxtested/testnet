Blockchains permiten mercados de predicción, lo que nos permite prepararnos para el futuro.
Para mostrar lo poderosos que pueden ser los mercados de predicción, usaremos un mercado de predicción para jugar contra un profesional y ganaremos.

Primero vamos a hacer el gran mercado, que vende 2 tipos de acciones. Las acciones de "IA" solo pagan si el profesional pierde. Las acciones "humanas" sólo pagan si el profesional gana.

Después de cada movimiento, el precio relativo de las acciones "Humana" y "IA" cambiará.
Para cada movimiento, hacemos 2 mercados de predicción, cada uno con <= 381 opciones posibles. La única diferencia entre los dos mercados es que uno tiene un precio en acciones "Human" y el otro en acciones "IA".

Así que por ejemplo, digamos que el precio actual es 60% probable que el humano ganará,
Y usted piensa que si el IA juega el 5C, que las probabilidades cambiarán al 50% probable que el humano ganará.
(Que haría que tus fichas IA 5/4 como valioso)
Usted también piensa que si la IA juega en cualquier lugar aparte de 5C, que las probabilidades del ganador humano aumentará al 80%.
(Que haría que sus fichas IA 1/2 fueran valiosas)

Hay 4 lugares en el cuadrado de Nash definidos por 2 preguntas:
1) ¿La IA juega en el 5C?
2) ¿El IA gana?

No apuestas directamente a ninguna de estas preguntas, sino apostas en la correlación.
Usted compraría acciones de (sí, sí), y compraría acciones de (no, no). Usted vendería acciones de (sí, no) y (no, sí).
Sigue haciendo esto hasta que los precios de las acciones son tales que si la IA juega 5C, el precio de las acciones de IA aumenta al 50%, y si la IA juega en cualquier otro lugar, el precio de las acciones de IA disminuye al 20%.





Para decidir los valores iniciales de los <= 381 resultados para cada mercado, usamos los valores finales de la ronda anterior de apuestas. La mayoría de los buenos movimientos siguen siendo buenos, la mayoría de los malos movimientos siguen siendo malos.
