Hay 5 tipos de transacciones:
2 que necesitan ser firmados por ambos: channel_new, channel_team_close,
Y 3 que están firmados por uno: channel_solo_close, channel_slash, channel_timeout

Si su compañero desaparece y desea cerrar el canal, primero publica un solo_close, que da el estado actual del canal, que se define por un contrato completo de turing que da salida a un nonce.
El contrato se divide en 2 partes, la parte scriptpubkey, que ambos participantes firmaron, y la parte scripsig, que sólo uno firmó.

Si su socio ve que usted publica un solo_close que no emite la más alta nonce posible, entonces pueden hacer una transacción channel_slash que genera un nonce superior, y esto se convierte en el estado final que el canal se cierra en.

Si tu pareja no te corta, entonces eventualmente puedes hacer una transacción channel_timeout, que cierra el canal en el estado desde solo_close.

Los datos que se graban en la cadena para cada canal son:
Cuánto dinero hay en el canal. Los 2 identificadores de cuentas que controlan el canal.
