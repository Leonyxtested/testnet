Asegúrese de que su sistema está actualizado y de que está ejecutando Ubuntu 16 o posterior:

(Las versiones anteriores de ubuntu requieren instalar manualmente la última versión de erlang, porque el gestor de paquetes instala una versión antigua)

```
sudo apt-get update
```
y
```
sudo apt-get upgrade
```

Para Ubuntu, instale las siguientes dependencias:

```
sudo apt-get install erlang libncurses5-dev libssl-dev unixodbc-dev g++ git erlang-base-hipe
```

A continuación, descargue Aeternity Testnet. Opcionalmente, puede ejecutar los siguientes pasos con un usuario no root, para una mejor seguridad.

```
git clone https://github.com/aeternity/testnet.git
```
Ahora usted puede entrar en el directorio, y compilar el testnet de aeternity.

```
cd testnet/
sh install.sh
```

La instalación debe hacerse. Ahora puede ejecutar su nodo.
