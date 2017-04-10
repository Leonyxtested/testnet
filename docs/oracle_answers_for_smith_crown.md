La pieza que todavía nos confunde es el proceso de consenso que involucra oráculos - en particular, determinar quién tiene razón entre dos reconvenciones sobre quién ganó las elecciones.
Es un mercado. Todo el mundo puede participar y hacer "reclamaciones", que mueven el precio (correspondiente a la probabilidad de correlación con la dificultad)

Es un mercado. Todo el mundo puede apostar en este mercado. No hay "reclamaciones" o "contra-reclamaciones".


El white paper dice: "Cualquier poseedor de eones puede lanzar un oráculo comprometiéndose a responder a una pregunta sí / no ... una vez que el lanzador del oráculo haya proporcionado una respuesta o hasta que haya transcurrido un cierto tiempo, cualquier otro usuario puede enviar un contador -reivindicaciones depositando la misma cantidad de eón ... Si se presentan contra-reclamos, entonces el mecanismo de consenso para los bloques se utilizará para responder al oráculo.
 Esto parece diferente de abrir un oráculo apostando en un resultado y tener otros apostando en su contra si no están de acuerdo, a menos que sepamos seriamente una de estas.

Esta sección del libro blanco está muy anticuada, hemos aprendido mucho desde que lo escribimos.

¿Es el proceso de consenso para determinar la respuesta a un oráculo en disputa similar al de Augur, en que alguna forma de árbitraje (como un representante) llega a servir como fuente de verificación? Si es así, ¿cómo se elige a ese árbitro?

El oráculo de Augur es un mecanismo de consenso basado en el voto.
El mecanismo de consenso del oráculo de la Aeternidad está basado en el mercado.

Un inconveniente de los mecanismos basados en la votación es que el costo de sobornar a un votante para votar maliciosamente disminuye por el cuadrado de la porción de monedas que poseen. Si 100 personas cada uno poseen 1%, entonces el costo de sobornar a todos para votar maliciosamente es de 1% de las monedas. Esto se llama tragedia de los comunes.
Augur también utiliza una subcuerda. Un inconveniente de las subcuenta es que el incentivo para votar correctamente está limitado por el tope de mercado de la subcuenta. Así que para que el oráculo sea preciso, el límite de mercado de la subcuenta debe ser mayor que el volumen de apuestas abiertas. Mantener el límite de mercado de la subcuenta tan alto significa que tendríamos que pagar a los titulares de la subcuenta mucho dinero, que es muy caro. Los oráculos basados ​​en el mercado son mucho más asequibles.

El resultado del oráculo de la aeternidad se basa en los precios en un mercado.

Si todavía está por definirse con más precisión, está bien, háganoslo saber. Si nos falta algo obvio, también déjenoslo saber por favor.
No somos cripto-genios técnicos, pero tampoco los inversionistas que leen nuestra investigación. Si no lo entendemos, otros ciertamente no lo harán y no podremos explicar más que decir "dicen que funciona y tienen un equipo inteligente, pero no estamos seguros de cómo hacerlo". Eso podría ser suficiente para usted, pero en general queremos representar el buen pensamiento con precisión.

Ok, lo defino con más precisión:
    El mercado del oráculo será una cadena de pedidos LMSR (regla logarítmica de puntuación de mercado) en cadena con 6 posibles resultados:
 1) alta dificultad, la decisión del oráculo es sí
 2) alta dificultad, la decisión del oráculo no es
 3) alta dificultad, la decisión del oráculo es indefinida
 4) dificultad baja, la decisión del oráculo es sí
 5) dificultad baja, la decisión del oráculo no es
 6) dificultad baja, la decisión del oráculo es indefinida
   
   La liquidez inicial para el mercado será proporcionada por un contrato dominante de aseguramiento (también llamado "crowdfunding asegurado") que se puede leer en la página 14 de este: http://bitcoinhivemind.com/papers/3_PM_Applications.pdf
   La decisión del oráculo se hará si el precio del mercado se mantiene cerca de una decisión por un tiempo suficiente.
   Estamos midiendo la correlación entre la decisión del oráculo y el precio de las fichas.
  
  La fórmula para LMSR es
  
  C = B * ln (suma de i = 0 a i = 2 de e ^ (P_i / B))
  Donde C es el dinero total dentro del creador del mercado,
  B * ln (3) es el dinero inicial antes de que se vendan las acciones
  P_i es cuántas acciones se han vendido de tipo i.

Los comercios serán emparejados en lotes donde cada uno consigue el mismo precio, una hornada cada 10 o 100 bloques mas o menos.
Los nodos completos tendrán que recordar las listas de operaciones sin igual para todos los bloques recientes, ordenados por precio.

Vamos a considerar la teoría detrás de por qué este mecanismo debería funcionar:
    Imagine que la cadena de bloques se dividió en una bifurcación, un lado registró la respuesta al oráculo honestamente y el otro lado mintió. Es mi expectativa de que el lado honesto de la bifurcación tendrá fichas más valiosas porque los usuarios preferirían poseer fichas en una cadena de bloque que tenga un oráculo exacto.

Ahora, vamos a considerar un par de ataques:
    ¿Qué pasa si un atacante hace apuestas en el mercado para manipular el precio y obtener el oráculo para mentir?
        > Cualquier manipulación de precios actúa como un premio para los comerciantes honestos para venir y poner el precio a donde pertenece. La investigación muestra que los esfuerzos para manipular los mercados de predicción en realidad los hacen más precisos.

¿Qué pasa si los atacantes no sólo manipular el mercado, sino también censuran a los comerciantes honestos, por lo que el precio sigue siendo mal?
         > Los mineros sólo pueden censurar a los comerciantes si controlan el 50% de toda la potencia minera. Si esto sucedió, entonces nuestras suposiciones de seguridad se rompen, y la cadena de bloques es insegura en muchos aspectos.
