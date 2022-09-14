# Intalacion Java e Intellij

## Windows
### OPENjdk
1. Descargar OPENjdk, software development enviroment de JAVA zip
2. Guardar descomprimido en una carpeta especifica. Por ejemplo C:\users\\.jdks\
3. Copiar la ruta hacia la carpeta descomprimida y configurar variable de entorno:
- Buscar "variable de entorno" en el explorador y click en variables de entorno
- click en nueva, seguidamente asignar un nombre (JAVA_HOME), y pegar la ruta hacia la carpeta
- en path, seleccionar la variable JAVA_HOME, para cuando se ejecute java desde la terminal sea capaz de encontarlo
### Intellij
1. Descargar la version community
2. Se abre el entorno de desarrollo

## Ubuntu
Al momento de instalar Java con OPENjdk e Intellij, uso Xubuntu 20.04, Instalo OPENjdk-17 e Intellij 2022.2.1

### OPENjdk
1. para instalar usar el comando `sudo apt install openjdk-17-jdk`
- Si algo no funciona ingresar `sudo apt upgrade` y luego `apt list --upgradable` y revisar si despues de el siguiente comando `sudo apt search openjdk` esta la version que se quiere instalar
2. revisar si hay mas de una version instalada con el comando `update-alternatives --config java`
3. configurar variable de entorno
- encontrar la ubicacion del jdk usando `sudo update-alternatives --config java` y copiar la ruta del jdk que se quiere utilizar
- editar la variable `PATH`, usar `sudo nano /etc/environment`
- Agregar las lineas: `JAVA_HOME="/usr/lib/jvm/java-17-openjdk-amd64"` y modificar `PATH="<rutas que hayan>:$JAVA_HOME"`
- dar a `ctrl + o`, `enter` para indicar el archivo que se esta modificando y por ultimo `ctrl + x` para salir del edito `nano`
- indicar la fuente con el comando `source /etc/environment` y comprobar que la variable `$JAVA_HOME` usando `echo $JAVA_HOME`

Esto seria todo respecto a OPENjdk

### Intellij 
1. ejecutar: `sudo snap intellij-idea-community --classic`

That would be all