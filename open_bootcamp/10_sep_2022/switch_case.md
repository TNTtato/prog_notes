# Switch Case Sentences

Se usan cuando se tienen condiciones con valores especificos y se aplican sobre una variable o condicion, las palabras claves serian `switch` y `case` 

**pseudo**
```
VAR ESTACION = "VERANO"

SWITCH ESTACION
CASE "VERANO"
  IMPRIME VERANO
CASE "INVIERNO"
```

**JAVA**

```java
public class Main {
  public static void main(String[] args) {
    var estacion = "verano";
    switch(estacion) {
      case "verano":
        System.out.println("es verano");
        break;
      case "invierno":
        System.out.println("Es invierno");
        break;
      default:
        System.out.println(estacion);
    }
  }
}
```
