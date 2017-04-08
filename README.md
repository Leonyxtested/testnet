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
to check if you are currently mining:
```
mine:is_on().
```

#### Spend
```
easy:spend(To, Amount).
```
To is the recipient's account ID

#### Last transactions
```
tx_pool:data().
```

#### Find out your account ID
```
keys:id().
```
If it returns something less than 1, that means you don't have an account yet.

#### Create an account
(does get done automatically when no accocunt and mining starts)
[Make an account](docs/new_account.md)

#### Check your balance
```
easy:balance().
```

#### Stop a node
To stop a node run:
```
easy:off().
```


### Else
If you want to know more, check out our whitepaper on [aeternity.com](https://aeternity.com) and get in touch with us via [Gitter Chat](https://gitter.im/aeternity?Lobby) or write us (emails in whitepaper). 
