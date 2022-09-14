# Definicion y conceptos

## Funciones

La funcion principal de una funcion es evitar la repeticion y poder reutilizar codigo.
Las funciones se declaran con un nombre, parametros que usa y el valor que retorna.
Con su nombre se identifica, los parametros son los datos con los que opera dentro de la funcion.

Ejemplos de definicion de funcion

**En Java**

```java
public class Main {

  public static void main(String[] args) {
    int resultado = 0;
    resultado = suma(a: 4, b: 2); //Invocaion de la funcion
    System.out.println(resultado);
  }

  public static int suma(int a, intb) { //Definicion de una funcion suma
    return a + b; 
  }
}
```

**En Go**

```go
package main

import "fmt"

func main() {
  resultado := suma(10, 30) //Invocaion de la funcion
  fmt.Println(resultado)
}

func suma(a int, b int) int { //Definicion de una funcion
  return a + b
}
```

Los parametros solo existen dentro de las funciones, a esto se le conoce como scope y vendria a ser el contexto en el que existe una variable

Se puede modularizar las funciones y tienen la posibilidad de compartir, se llaman librerias
Se pueden pasar argumentos a una funcion de dos maneras:

- **Paso por Valor**: Se pasa directamente el valor como argumento a una funcion, lo que hace que duplique o se haga una copia del argumento que se ha pasado

```java
suma(a: 3, b: 4);
//
//
int param1 = 3
int param2 = 4

suma(param1, param2);
```

- **Paso por Referencia**: Se pasa una direccion de memoria, y la funcion se encarga de modificar lo que haya en la direccion de memoria y por lo tanto no asigna mas direcciones de memoria, es decir, no duplica la informacion una forma de hacer esto, es pasar instancias u objetos. Esto se debe a que se utiliza el concepto de punteros, que es simplemente una referencia a una direccion de memoria especifica.

```go
package main

import "fmt"

func main() {
  param1 := 10
  param2 := 30
  var resultado int

  suma(param1, param2, &resultado) //& crea una referencia a una direccion de memoria en la que se encuentra resultado
  fmt.Println(resultado)
}

func suma(a int, b int, c *int) { //Definicion de una funcion
  *c = a + b //Al pasar de esta manera el parametro c, se modifica directamente sobre resultado
}
```

**Funciones Recursivas**:

Son funciones que retornan un resultado y luego se llama a si misma para volver a ejecutarse, estas funciones deben contar con condiones de clausura para evitar bucles infinitos

**Ejemplo recursion Python:**

```py
def recur_fibo(n): #Se usa la recursion para calcular el termino n, de la serie de Fibonacci
#la clausura o termino de ejecucion llega cuando n <= 1
   if n <= 1:
       return n
   else:
       return(recur_fibo(n-1) + recur_fibo(n-2))
```

**Callbacks**

Es asignar una funcion a una variable, para poder ser llamada en otro contexto, es algo como guardar el codigo de la funcion en una variable. Por lo que llama indirectamente a la funcion.