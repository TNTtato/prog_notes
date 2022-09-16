# El Interprete de Python

Viene integrado con el propio lenguaje.
Para ejecutar un script de python solo se debe ejecutar `python3 <file.py>`
# pip

`pip` permite la instalacion de librerias y herramientas para trabajar con algunas funcionalidad que no vienen por default en python

Por ejemplo para instalar la libreria `scipy` se usa `pip install scipy`, para desinstalar `pip uninstall <dependencia>`

Para buscar dependencias instalables con pip, habra que buscar en [pypi.org](https://pypi.org/)

Para ver que dependencias tengo instalados se ejecuta `pip list`

Para mostar una informacion del paquete se ejecuta `pip show <dependencia>`

### Problemas de pip

Si dos programas tienen de requisito la misma dependencia pero con versiones diferentes, desinstala la version mas vieja, es decir, no permite dos versiones de la misma dependencia. Esto supone un problema pues puede que un programa funcione de manera correcta debe tener una version especifica de dicha dependencia.

Para solucionar este problema existen varias opciones usando `virtual env`, que es un entorno virtual:

**Usando** `virtualenv <nombre del env>`: 

Crea un entorno virtual en la carpeta donde se quiere instalar las dependecias, esto hace que exista independencia de un entorno a otro.

Para activar ese entorno, se debe ejecutar el comando, `source <directorio>/venv/bin/activate`. Asi solo se intalan las dependencias solo en ese entorno. Para salir del entorno virtual se usa `deactivate`.

La practica usual para trabajar con virtual envs, deberia crearse una carpetar especifica para esto, donde se tengan todos los entornos

por ejemplo:

- virtualenvs (dir)
  - scipy (env)
  - numpy (env)
  - ect (env)

Y para cambiar de entorno solo se cambia al directorio en el que esta contenido virtualenvs y se ejecuta `source virtualenvs/<nombre del ev>/bin/activate`

El codigo fuente puede permanecer donde estaba originalmente sin necesidad de moverlo a una carpeta especifica, lo unico que cambia es que el environment instala en rutas independendientes en el SO

**Usando Pyenv**

Permite intalar diferentes versiones de python, mientras que con virtualenv solo la que se tenga en el SO. Esta libreria no funciona con Windows

**Usando pipenv**

Si no se tiene instalado usar `sudo apt install pipenv` en Ubuntu

Para crear un entorno virtual se crea un directorio, se navega hasta el
y se ejecuta `pipenv shell`, para salir `exit`

Luego para instalar dependencias independientes, se instala dentro del directorio del environment usando `pipenv install <nombre de la dependencia>`

Se pueden instalar paquetes desde pip, pero tambien desde el codigo fuente que no esta en pypi sino en un repositorio git usando `pipenv install -e git+<urlrepositorio>`

Con Pipfile.lock se puede pasar toda la informacion acerca de las dependencias instaladas en un entorno y se puede compartir para tambien tener todas ellas en otro entorno o a un companiero. Se copia este Pipfile.lock en el directorio donde se quiera el env y se ejecuta `pipenv install --ignore-pipfile`. De esta manera se puede reproducir todo un entorno.

### Flujo de trabajo

- Crear los files de trabajo normalmente
- Crear una carpeta que contenga el entorno virtual usando `pipenv`
- Trabajar sobre este entorno