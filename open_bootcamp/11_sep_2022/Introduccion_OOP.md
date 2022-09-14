# Introduccion a la Programacion Orientada a Objetos (OOP)

## Objetos

Los objetos pretenden emular los objetos de la vida real y como ellos tienen propiedades y acciones realizables.
Las propiedades se llaman variables de estado o de instancia y las acciones se denominan metodos

Los objetos se declaran mediante `clases`

## Clases

Las clases son, por decirlo de una manera, recetas para crear un objetos, son el plano por el cual se contruyen.

**Ejemplo JAVA**

```java
public class static Main {
  
  public static void main(String[] args) {
    Coche coche = new Coche(); //Instanciar coche, construir un objeto

  }
}

class Coche { // clase
  int numeroDePuertas = 4; //propiedades

  public void acelerar() {} //methods
}
```

Las clases tienen **contructor**, que no es otra cosa que una forma o metodo de la clase, que inicializa las propiedades del objeto que esta siendo intanciado. 

**ejemplo:**

```java
class Coche { // clase
  int numeroDePuertas = 4; //propiedades
  int velocidadMaxima;
  //...

  public Coche(int puertas, int velocidad) { //constructor
    this.numeroDePuertas = puertas;
    this.velocidadMaxima = velocidad;
  }


  public void acelerar() {} //methods
}
```

Los constructores no devuelven ningun valor, como se ve en el ejemplo, las variables de cada objeto se puede inicializar de manera distinta

## Propiedades privadas y públicas, su abstracción y encapsulación.

### Propiedades y methods public and private

Las propiedades y methods publicos son aquellos que se pueden usar fuera y dentro de la clase y las privadas son aquellas que se solo se pueden usar dentro de la clase

**JAVA**

**public property**

```java

//in main...

Some some = new Some();

some.type = "Some type";

//Property type now is "Some type"

//

class Some {
  String type;
}
```

**private property**

```java

//in main...

Some some = new Some();

some.type = "Some type";

//Error, private access

//

class Some {
  private String type;
}
```

De igual manera sucede con los metodos

### Encapsulacion

Es un concepto que busca abstraer el codigo y no compartir toda la informarcion del objeto, sino unicamente dar acceso a lo necesario.

Una forma de implementar la encapsulacion, es designar todas las propiedades privadas y luego acceder a ellas mediante `setters` y `getters` cuya funcion serian, modificar y leer la propiedad respectivamente

**JAVA**

```java
class Foo {
  private String type;

  public void setType(String type){ //setter
    this.type = type;
  }

  public String getType() { //getter
    return this.type;
  }
}
```

### Abstraccion

Consiste en implementar parte de una clase y elresto al libre albedrio, utilizando la herencia para pasar metodos abstractos a hijos
