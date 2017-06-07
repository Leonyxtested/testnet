Para intalar el Testnet en Windows 10 necesitas actualizar la ultima versión de Windows o la actualización Creator Update.

Luego hay que intalar el Bash de Ubuntu:

-Tienes que acceder a Configuración –> Actualización y seguridad –> Para programadores , aquí seleccionas "Modo programador".

-Seguidamente verás un mensaje avisando que podrías exponer tu dispositivo y tus datos personales a riesgos de seguridad o 
 causar daños en el dispositivo.Aquí tienes que hacer clic en Sí.

-Una vez activado el modo desarrollador tienes que abrir el Panel de control –> Programas –> Activar o desactivar las 
 características de Windows y marcar la casilla Subsistema de Windows para Linux (beta). Ahora pulsa en Aceptar y una vez 
 termine la instalación te pedirá reiniciar el equipo.

-Una vez hayas reiniciado tienes que abrir el "Símbolo del sistema" –CMD–, tecla Windows+R, y teclear bash.

-Aquí no tienes que hacer mucho, avisa que esta opción instalará Ubuntu en Windows, si estás de acuerdo tienes que pulsar la 
 tecla “y” para continuar. Ahora solo tienes que esperar, una vez finalice la instalación te pedirá un nombre de usuario y 
 contraseña.

-Para entrar tecleas en el buscador de Windows "Ubuntu", aparecera el Bash, clickas y aparecera un terminal de Ubuntu.

-A partir de aqui sigue los pasos de instalación de [Ubuntu](docs/compile_ubuntu.md).


En caso de que haya algún problema con el terminal y desea reinstalarlo:

-Abrir el CMD,tecla Windows+R, o buscando "Símbolo del sistema".

-Escribe ```lxrun /uninstall``` para eliminarlo pero dejando el directorio ```/home``` y ```/root```; para eliminarlo completo escribe 
 ```lxrun /uninstall /full```.

-Para instalarlo de nuevo escriba ```lxrun /install```, empezara a descargarlo he instalarlo, tardara un poco,cuando termine te 
 pedira un nombre de usuario y contraseña.


Si desea eliminarlo por completo de su Windows 10:

-Abre el Panel de control y ve hasta los programas> Activar o desactivar las características de Windows. Desactive la opción 
 “Subsistema de Windows para Linux”.
