# Instalacion e Introduccion

Lenguaje de programacion  interpretado, existen varias versiones:

- Cyton: Escrita en C
- Jython
- Entre otras

Version de python en mi sistema es python3

**Interprete**: Es un programa que ejecuta linea a linea el codigo fuente que escribimos. Los lenguajes interpretados tienen como ventajas mas importantes que aportan son la de poderse ejecutar casi en cualquier parte teniendo solo el codigo y la de poder depurar facilmente el codigo

Python se puede usar de forma secuancial o con el paradigma OOP

**Secuencial**

```py
x = '5'
print('x tiene de valor ' + x)
# x tiene de valor 5
```

**OOP**

```py
class clase:
  def suma(self, a, b):
    return a + b

datos = clase()
print(datos.suma(2, 2))
# 4
```

**Lenguajes de tipado estatico y de tipado dinamico**

Para la definicion del tipo ver [Introduccion](../01_sep_2022/notes/Introduccion.md)

Python determina automaticamente el tipo de dato de una variable, es decir, es de tipado dinamico

**Tipado fuerte y tipado debil**

Los tipados fuertes quiere decir que solo se pueden realizar operaciones entre datos del mismo tipo, los de tipado debil permiten estas operaciones. Python es de tipado fuerte.

**Usos de python**

- **Automatizacion:** gestionar de manera automatica sistemas, ejemplo de esto serian el programma [Ansible](https://www.redhat.com/es/technologies/management/ansible) y [Salt Project](https://saltproject.io/)

- Sirve para crear **interfaces de usuario** mediante el uso de librerias como [PyGTK](https://pypi.org/project/PyGTK/) y la mas usada seria [tkinter](https://docs.python.org/es/3/library/tkinter.html)

- En el Back-End web mediante los frameworkd [django](https://www.djangoproject.com/) y [flask](https://flask.palletsprojects.com/en/2.2.x/)

- Para acceder a **bases de datos**

- En **Data Science**, **Data analisys** y demas. Ejemplo de esto es la libreria [NumPy](https://numpy.org/) y [Pandas](https://pandas.pydata.org/)
