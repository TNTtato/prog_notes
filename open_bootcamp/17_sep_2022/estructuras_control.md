# Estructuras de Control

**Control de flujo:** 

Es una forma de guiar la ejecucion del programa para que haga lo que se desea mediante condiciones logicas

Para ello se hacen test de veracidad, que devuelven uno de dos valores, `True` o `False`

**Ejemplo operadores condicionales**

```py
a = 5
b = 6

result = a < b
print(result) # True

result = a > b
print(result) # False

# De igual manera con el resto de operadores
```

**Operadores Logicos**

Estos son `and` y `or`

**Ejemplo**

```py
a = 4
b = 10

result = a >= 5 and c < 20
print(result) #True

result = a > 6 or c == 10
print(result) # True
```

El operador `and` solo es `True` si ambas condiciones son `True`, y `or` solo es `False` si ambas condiciones son `False`. Existe la negacion, `not` que niega el valor de una variable o condicion booleana, si es `True` entonces `not True` es `False` y viceversa

## Sentencias if

Es una sentencia que ejecuta un bloque de codigo si una condicion es verdadera.

```py
if condicion:
  bloque_cod()
```

Se puede ejecutar otro bloque de codigo en caso que no sea verdadera la condicion usando `else`.

```py
if condicion:
  bloque_cond()
else:
  bloque_else
```

Se puede evaluar mas de una condicion usando `elif`.

```py
if cond1:
  bloque1()
elif:
  bloque1()
else:
  bloque_else()
```

**NOTA**: Un bloque de codigo hace parte de una sentencia si la identacion del codigo es la misma justo de declarar la sentencia.

## Sentencia while

Es un loop mientras la condicion sea verdadera, cuando se vuelva falsa para.

```py
while condicion:
  bloque_while
  # Se ejecuta hasta que condicion == False

## EJEMPLO
contador = 1
while contador <= 10:
  print("cont:", contador)
  contador += 1
```

Se puede parar el loop o pasar por encima de una iteracion usando `break` o `continue` respectivamente

## Sentencia for

Un bucle for establece la variable iteradora en cada valor de una lista, arreglo o cadena proporcionada y repite el código en el cuerpo del bucle for para cada valor de la variable iteradora.

```py
valores = [1, 2, 3, 4, 5]
for valor in valores:
  print(valor, end=", ") 
```

**Usando range**

`range` es una funcion que proporciona una secuencia de enteros dada unas condiciones dadas

```py
range(parar) #(de 0 hasta parar-1 con paso 1)
range(inicio, parar) #(inicio hasta parar - 1 con paso 1)
range(inicio, parar, paso) # de inicio a parar - 1 con saltos de paso
```

**palabra reservada in**

`in` sirve para saber si un dato esta en un conjunto de datos y devuelve `True` si esta, `False` si no esta

**else**

`else` se puede agregrar despues de un for y este se ejecutara siempre al finalizar el loop, siempre y cuando no se haya *roto*.

```py
for val in values:
  if someCondition: #if true else no se ejecuta
    someCode()
    break
else:
  someElseCodeFor()
```

## Switch

`switch` solo esta disponible a partir de la version 3.10 de python, versiones anteriores no la soportan

```py
match valor:
  case 1:
    bloque1
  case 2:
    bloque1
  case 3:
    bloque1
  case 4:
    bloque1
```

## Scope

El scope es el entorno o contexto en que vive una variable, puede que una variable sea global, es decir accesible a todo el codigo o local, accesible solo dentro del bloque en que se crea. Tambien existen las variables de clase que solo estan disponibles dentro de una clase