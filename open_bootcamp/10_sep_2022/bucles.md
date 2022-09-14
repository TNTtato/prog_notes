# Bucles

Un bucle es repetir un bloque de codigo, mientras se comple una condicion, puede ser un numero de veces especifca o cualquier tipo de condicion

## Bucle While

Es un bucle que ejecuta un bloque de codigo, mientras se cumple la codicion dada. Todos los lenguajes de programacion existe a excepcion de `Go`

**pseudo**

```
VAR CONTADOR = 10
WHILE (CONTADOR MAYOR A CERO):
  RESTA UNO A CONTADOR
  ACCIONES
```

**JAVA**

```java
public class Main {

  public static void main(String[] args) {
    int contador = 10;

    while (contador > 0) {
      System.out.println("Contador es: " + contador);
      contador--;
    }
  }
}
```

**output:**

```
Contador es: 10
Contador es: 9
Contador es: 8
Contador es: 7
Contador es: 6
Contador es: 5
Contador es: 4
Contador es: 3
Contador es: 2
Contador es: 1


Process finished with exit code 0
```

## Bucle for

Es un bucle que se inicializa, compara una condicion y una accion:

**pseudo**

```
VAR CONTADOR = 10
    //INICIO     ; COND; ACCION
FOR(i = CONTADOR; i > 0; i--)
  IMPRIME LA VARIABLE i
```

**JAVA**

```java
public class Main {

  public static void main(String[] args) {
    for (int i = 10; i > 0; i--) {
      System.out.println("Contador: " + i);
    }
  }
}
```

**output:**

```
Contador: 10
Contador: 9
Contador: 8
Contador: 7
Contador: 6
Contador: 5
Contador: 4
Contador: 3
Contador: 2
Contador: 1


Process finished with exit code 0
```