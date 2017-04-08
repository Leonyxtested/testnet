æternity
==========

Este es el código utilizado para testnet para el proyecto [æternity](www.aeternity.com).

Este testnet utiliza un simple consenso de PoW. Su propósito es mostrar cómo funcionan los canales.

### Compilando y Empezando
Necesitarás Erlang y un par de librerias. Sigue las instrucciones:
[For Ubuntu](docs/compile.md)

A continuación, inicie su nodo con el siguiente comando:
```
sh start.sh
```

### Commandos

#### Sincronizar con la red
Para sincronizar con la red y descargar la cadena de bloques:
```
easy:sync().
```

#### Mineria
Después de la instalación, se puede iniciar la minería.

Para iniciar la minería con todos los núcleos de la CPU:
```
mine:start().
```
Para detener la minería:
```
mine:stop().
```
Para comprobar si está minando:
```
mine:is_on().
```

#### Gasto
```
easy:spend(To, Amount).
```
"To" es el ID de cuenta del destinatario,ejemplo: easy:spend(5, 10).

#### Transacciones
```
tx_pool:data().
```

#### Descubre el ID de tu cuenta
```
keys:id().
```
Si devuelve algo menos de 1, eso significa que aún no tienes una cuenta.

#### Crear una cuenta
(Se hace automáticamente cuando no se inicia la cuenta y la minería)
[Hacer una cuenta](docs/new_account.md)

#### Revisar tu balance
```
easy:balance().
```

#### Parar el nodo
Para detener la ejecución de nodo:
```
easy:off().
```


### Mas
Si desea saber más, consulte nuestro whitepaper en [aeternity.com](https://aeternity.com) y ponerse en contacto con nosotros a través de [Gitter Chat](https://gitter.im/aeternity?Lobby) o escríbanos (emails en el whitepaper). 
