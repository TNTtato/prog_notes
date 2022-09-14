# Condicionales

Los condicionales son una forma de controlar el comportamiento de un programa de la manera en que queremos, comparando condiciones:

**Condiciones logicas:**

las mas usadas son `Y` y `O`, tambien la negacion `NOT`

Las condiciones `Y` solo son verdaderas cuando ambas condiciones son verdaderas

Las condiciones `O`, solo son falsas cuando ambas condiones son falsas

Las condiciones `NOT`, cambian el estado de la condicion, si era verdadera ahora en falsa y viceversa

**Comparaciones:**

Son operaciones de comparacion para descubrir la relacion que existe entre dos datos, cantidades, variables...

Estas son, `Mayor que`, `Menor que`, `Mayor igual que`, `Menor igual que`, `Igual a`, `Diferente a`

**Bloques `IF/ELSE`, `IF/ELSE IF/ELSE`:**

Sirven para tomar una u otras acciones, dependiendo de si se cumplen ciertas condiciones

**IF/ELSE**

```
IF CONDICIONES1 THEN:
  ACCIONES1
ELSE
  ACCIONES_ELSE
```

**IF/ELSE IF/ELSE**

```
IF CONDICIONES1 THEN:
  ACCIONES1
ELSE IF CONDICIONES2 THEN:
  ACCIONES2
ELSE
  ACCIONES_ELSE
```

## Ejemplo JAVA

```java
public class Main {

  public static void main(String[] args) {
    String estacion = "primavera";

    if (estacion == "primavera") {
      System.out.println("Es primavera");
    } else if (estacion == "verano") {
      System.out.println("Es verano");
    } else {
      System.out.println("Es otra estacion");
    }
  }
}
```

**output:**

```
Es primavera


Process finished with exit code 0
```