# Definicion y Uso de Funciones

Las funciones son una forma de escribir codigo reutilizable que hagan una sola actividad. Si una funcion se llama `suma` solo debe realizar sumas, no debe multiplicar o dividir.

En python se definen asi:

```py
def funName(params):
  pass
```

Las partes de la definicion, son la palabra reservada `def`, el nombre de la funcion que debe ser desciptiva respecto a lo que hace, los parametros que pueden ser o no opcionales y el cuerpo de la funcion.

Las funciones deben ser definidas antes de ser llamadas por primera vez.

Las funciones se llaman asi:

```py
funcion(params) #params si los requiere
```

Se pueden tener funciones definidas dentro de las funciones, que seran invocables dentro de la funcion

```py
def math(a, b):
  def add(a, b):
    return a + b
  
  def product(a, b):
    return a * b
  
  print(add(a, b))
  print(product(a, b))

```

Los parametros de las funciones, son variables utilizables dentro de ellas. Se denominan para cuando se define la funcion y se denominan argumentos cuando se pasan a una funcion durante una llamada.

Las variables dentro de una funcion, son de naturaleza local, no pueden ser usadas desde fuera

Las variables fuera de una funcion, si pueden ser usadas dentro de la funcion, a no ser que dentro exista una con el mismo nombre


```py 
name = 'Gus'

def printName():
  print(name)

printName() #=> Gus
```

```py
name = 'Gus'

def printName():
  name = 'Alonso'
  print(name)

printName() #=> Alonso
```

Una varible dentro de una funcion puede ser usada desde fuera, si se la hace global con la palabra reservada `global`

```py
temp = 12.0

def printTemp():
  global temp
  temp = 22.0
  print("La temp es, ", temp)

printTemp() #=> La temp es, 22.0

print(temp) #=> 22.0
```

Esto quiere decir que una variable fuera de una funcion, puede ser manipulada dentro, si se le antecede la palabra `global`

Los parametros pueden tener valores predeterminados, lo que hace que al ejecutar la funcion sin esos parametros, trabaja con los predeterminados.

La regla para usar parametros opcionales, es que sean todos, o que los opcionales, sean los ultimos

```py
# All params are optional
def aFun(a = 1, b = 2):
  pass

# Just one is optional. Defined last
def otherFun(a, b, c = 3):
  pass
```

Se pueden pasar argumentos a los parametros, por su nombre. Esto se denominda `named parameters`

```py
def func(a,b,c):
  pass

# all pass as named parameters
func(c = 3, a = 1, b = 2) 

# one in order, two as named parameters
func(1, c = 3, b = 2)
```

Se puede tener un numero de parametros variables, que puede ser ninguno o muchos

Con `*` se pasan argumentos en forma de tupla a la variable, en este caso, `args`

```py
def foo(*args):
  pass

foo(1,2,3,4,5) #args => (1,2,3,4,5) 
foo(1) #args => (1)
```

Con `**` se pasan como una estructura tipo `hash`, en python un diccionario

```py
def foo(**kwargs):
  for key, value in kwargs.items():
    print(key, ' --> ', value)

foo('a' = 1, 'b' = 2, 'c' = 3)
# a --> 1
# b --> 2
# c --> 3
```

Las funciones devuelven valores con la palabra reservada `return`

Se pueden devolver mas de un valor, en forma de tupla, de la siguiente manera

```py
def opera(a,b):
  return a + b, a - b, a * b, a / b

opera(2,4) # devuelve tupla
#=> (6, -2, 8, 0.5)

add, subs, prod, div = opera(2, 4) # asigna valores consecutivos a las variables
# add = 4
# subs = -2
# prod = 8
# div = 0.5
```

Cuando se devuelven varios valores, o se guardan en una sola tupla, o en tantas variables como datos retornados

**Ejemplo usando \*\***

```py
def sumador(**kwargs):
  inicial = kwargs['inicial']
  final = kwargs['final']
  resultado = 0
  for x in range(inicial, final + 1):
    resultado += x
  
  return resultado

print('inicial' = 15, 'final' = 30) # 360 
```

En el ejemplo anterior se le puede aniadir un operador ternario, para evitar errores de argumentos. En python el operador ternario es tal que asi

```py
# Sin asignacion
accion() if condicion else otro()

# Con asignacion
var = accion() if condicion else otro()
```

En el ejemplo la linea 

```py
final = kwargs['final']
``` 
podria ser

```py
final = kwargs['final'] if 'final' in kwargs else 0
``` 

Existen las funciones anonimas, tambien llamadas lambdas.

Esta se puede asignar a una variable, de modo que es como si se estuviera guardando ese codigo

```py
# Sin param
anonym = lambda: print('hello')

# Con param
anonym = lambda param1, param2: print('hello', param1, param2)
```

