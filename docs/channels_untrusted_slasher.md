Una propiedad deseada de los canales es que los usuarios no quieren tener que estar en línea 24/7 para estar listo para proporcionar pruebas. Preferirían pagar a otras personas para estar en línea con la evidencia.

Esto crea varios nuevos vectores de ataque que tendremos que considerar al diseñar los canales.
Los viejos canales parecían esto:
New_channel_tx, grow_channel, grow_channel, channel_team_close.

Los grow_channels tienen que aumentar la cantidad de dinero controlada por el canal.

O como esto:
New_channel_tx, grow_channel, channel_solo_close, channel_slash
O como esto:
New_channel, channel_solo_close, channel_timeout

Los nuevos canales tienen este aspecto:
New_channel_tx, grow_channel, canal de crecimiento, channel_solo_close, channel_slash, channel_slash, channel_slash, channel_timeout

