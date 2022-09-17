# Tipos de Objetos en Python

**Mutabilidad e Inmutabilidad**

**Objeto inmutable** es un objeto cuyo estado no puede ser modificado una vez creado. ​ Es el opuesto a los **objetos mutables** que pueden ser modificados tras su creación. 

En python los objetos tipo *bool, complex, int, float, frozenset, strings, tuplas, ranges, Bytes* son inmutables, pues cuando se cambia el valor a la variable no se modifica sino que se reserva otra direccion de memoria para el nuevo objeto. Luego se eliminan todas las zonas de memoria que no son referenciadas.

Los objetos mutables son los de tipo *List, Bytearray, Memoryview, Dict, sets y clases definidas*. Esos son asi pues cuando se modifica la variable, se modifica tambien la zona de memoria en la que estan almacenados.

**Listas**

```py
lista = [1, 2, 3, 4]

lista[0] #>>> 1
```

**Diccionario**

```py
dictionary = {'clave': 'valor', 'clave': 15}
dictionary['clave'] # >>> 'valor'
```

**sets**

```py
set1 = {1,2,3,1,2,3}
print(set1) # {1,2,3}
# Los sets no pueden tener valores duplicados
```

## Operadores

**De asignacion**

- `=` es el operador de asignacion
- `+=` aumenta el valor de la variable
- `-=` quita el valor a la variable
- `/=` divide completo a la variable
- `//=` divide entero a la variable
- `*=` multiplica a la varible
- `**=` eleva a la variable
 
**Aritmeticos**

- `+` adicion
- `-` resta
- `%` modulo
- `//` division entera
- `/` division float
- `*` multiplicacion
- `**` exponenciacion

**De comparacion**

- `==` identidad
- `>` mayor que
- `<` menor que
- `>=` mayor-igual que
- `<=` menor-igual que

De esta manera muchos mas