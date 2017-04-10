En otros documentos, discutimos por qué el oráculo será un mercado, y cómo funcionará este mercado.

Podríamos construir este mercado en la cadena, pero que vendría con graves costos anti-escalabilidad.
Tendríamos que recordar la lista ordenada de órdenes abiertas en muchas alturas de bloques diferentes.

Aquí puede leer acerca de cómo el oráculo puede ser construido fuera de cadena.

Los pasos son los siguientes:
1) Alguien se compromete a ejecutar el mercado del oráculo. Permiten que cualquier persona haga los canales con ellos y apueste.
2) Los mineros hacen apuestas múltiples en el mercado para cancelar su riesgo. Los mineros lo hacen anónimamente.
3) El oráculo publica periódicamente los precios de los diferentes tipos de acciones en el oráculo. El acto de publicar un precio cierra muchas órdenes abiertas hechas en muchos canales diferentes. Cierra todas las órdenes que acordaron comerciar a ese precio.
4) Una vez que el precio se mantiene estable durante un período de tiempo suficientemente largo, se calcula la coordinación de la resolución del oráculo con la dificultad y de ella la cadena de bloques aprende el verdadero hecho de nuestro mundo.

Vectores de ataque para analizar
1) ¿Qué pasa si el oráculo se niega a tomar cualquier apuesta en el mercado?, entonces el oráculo no tiene incentivos para escribir los precios correctos.
* Los mineros hacen apuestas múltiples en el mercado para cancelar su riesgo. Los mineros lo hacen anónimamente a través de relámpagos de cebolla. Hacen suficientes apuestas para tener confianza estadística sobre el porcentaje de apuestas censuradas.
* Si demasiadas de las apuestas del minero son censuradas (>~ 95%), entonces los mineros censuran al oráculo de publicar el resultado.

2) ¿Qué pasa si el oráculo escribe un precio equivocado en el último minuto, por lo que el volumen de operaciones es pequeño?
* El oráculo no se establece hasta que el precio permanezca en un intervalo durante mucho tiempo.

3) ¿Qué pasa si el oráculo censura sólo suficientes votos para que la mitad de los mineros se divida en un lado de un fork y la otra mitad esté en el otro lado de un fork?

*Hay 3 resultados posibles:
*1> 95% de las apuestas son censuradas, en cuyo caso censuramos el oráculo, los mineros se niegan a construir sobre los bloques que incluyen transacciones de oráculo.
*2 Menos del 80% de las apuestas son cesuradas, en cuyo caso no censuramos el oráculo, y tenemos una fuerte preferencia por el lado del fork que publica el resultado del oráculo. No importa la altura en la que un fork incluya las transacciones del oráculo.
*3 Entre el 80% y el 95% son censurados, en cuyo caso los mineros aceptan cualquier lado del fork es más largo sin preferencia, y censuran el oráculo txs de los bloques que mina.
