El precio futuro de los bloques se divide en P posibilidades. Entre 3 y 20.

El valor futuro de los oráculos se divide en 2 posibilidades.

El valor futuro de las variables de gobernabilidad se divide en las posibilidades de G. Entre 300 y 100000.

Vamos a utilizar un mercado para hacer los tipos P de acciones.
Haremos los mercados de P para cada oráculo, tasado en cada una de las acciones de P.
Haremos los mercados de P para cada variable de gobierno, tasada en cada una de las acciones de P.

Estándar LMSR.
C = b*ln(Sum[i from 0 to 1-P](e^(q_i/b)))


En cada bloque, los usuarios pueden apostar en los mercados que quieran.
C bloques más tarde, hacemos algunas estadísticas y determinar los ganadores y pagarlos. Los ganadores demuestran sus apuestas para ganar, el consenso sólo sostiene la raíz merkle de sus apuestas.
Desafortunadamente, no podemos pagar a los ganadores de forma lenta y exponencial, porque es demasiado costoso desde el punto de vista computacional leer cada bloque C pasado, y dar recompensas por cada apuesta.
