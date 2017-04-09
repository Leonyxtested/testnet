Cuando inicia un nodo completo, al principio no tiene ningún eón.

Su dirección se genera automáticamente para usted, y se asegura con la contraseña "". La cadena vacía es la contraseña predeterminada.

Para generar una dirección con una contraseña mejor, escriba siguiente comando:

```
keys:new("NO_USE_ESTA_CONTRASEÑA").   
```

Asegúrese de haber reemplazado "NO_USE_ESTA_CONTRASEÑA" con una contraseña mejor y entrecomillado "MEJOR_CONTRASEÑA".
Esta contraseña se utiliza para cifrar la clave privada en su ordenador.

Si desea cambiar la contraseña, haga lo siguiente:
```
keys:change_password("VIEJA_CONTRASEÑA", "NUEVA_CONTRASEÑA").
```

Reemplace "VIEJA_CONTRAEÑA" con la contraseña que está reemplazando.
Reemplace "NUEVA_CONTRASEÑA" con la nueva contraseña que desee.
Siempre en entrecomillado.


Antes de usar su nodo, asegúrese de que su _account_ esté desbloqueada usando su contraseña:
```
keys:unlock("NO_USE_ESTA_CONTRAEÑA").
```


Una manera de conseguir aeons es compartir tu _address_ con alguien que ya tenga eones, para que te envíen algo.


Genere su dirección:
```
keys:address().
```

Para gastar dinero en una nueva _account_, es necesario realizar una transacción:
``` 
easy:create_account(Address, AmountOfMoney, Fee, NewID).
```
