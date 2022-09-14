# Herencia, polimorfismo e interfaces.

## Herencia

Es un mecanismo por el que una clase comparte propiedades y metodos a otra clase. 

La clase que cede propiedades y metodos se denomina clase padre, superior, etc. La clase que hereda se denomida clase hija.

Las clases hijas pueden tener propiedades y funciones propias, aniadiendo asi funcionalidades, ademas de tener ellas mismas mas hijas, siendo esto conocido como herencia multinivel.

**pseudo**:

```
class Vehicule
  private maxSpeed;
  private fuelType;

  function sayHello()
    print "Hello";

class Car inherits from Vehicule
  (inherit) maxSpeed
  (inherit) fuelType
  private doorNumber; //own property

  (inherit) function sayHello()
    print "Hello";

  function setDoorNumber(int doors)
    thisClass.doorNumber = doors;

  function getDoorNumber() int
    return thisClass.doorNumber

class Coupe inherits from Car
  (inherit) maxSpeed
  (inherit) fuelType
  (inherit) doorNumbe

  (inherit) function sayHello()
    print "Hello";

  (inherit) function setDoorNumber(int doors)
    thisClass.doorNumber = doors;

  (inherit) function getDoorNumber() int
    return thisClass.doorNumber
```

**JAVA**

```java
//...
class Vehicule {
  private int maxSpeed;
  private String fuelType;

  public void sayHello(){
    System.out.println("Hello");
  }
}

class Car extends Vehicule { // inherits from Vehicule
  private int doorNumber;

  public void setDoorNumber(int doors) {
    this.doorNumber = doors;
  }

  public int getDoorNumber() {
    return this.doorNumber;
  }
}

class Coupe extends Car { //Inherits from Car
  public void imCoupe() {
    System.out.println("I'm a coupe");
  }
}

//In main function
Coupe coupe = new Coupe(); //new coupe object

coupe.imCoupe(); //print I'm a coupe
coupe.setDoorNumber(2);
System.out.println(coupe.getDoorNumber()); //Prints 2
```

Las clases pueden heredar de otras pero se puede indicar que de ella no se herede mas, se denomina clase final

## Abstraccion

Es implementar funciones dentro de una clase abstracta, para que sus hijas completen o extiendad las funcionalidades. La clase padre le dice a las hijas que funciones se deben implementar pero no como, eso depende de las hijas.

Las clases abstractas no se pueden instanciar

**JAVA**

```java
abstract class Vehicule {
  String sound;

  public void Vehicule() {
    System.out.println("Im in vehicule");
  }

  abstract public String getSound();
  abstract public void setSound(String sound);
}

class Car extends Vehicule {
  public String getSound() {
    return "I'm super Fast " + this.sound;
  }

  public void setSound(String sound) {
    this.sound = sound;
  }
}
class Motorbike extends Vehicule {
  public String getSound() {
    return "I'm super slow " + this.sound;
  }

  public void setSound(String sound) {
    this.sound = sound;
  }
}
```

Existe la herencia multiple, aca es donde se heredan propiedades de dos o mas clases

La herencia jerarquica hereda como un arbol genealogico, existe un ancestro en comun del cual derivan otras ramificaciones

La herencia hibrida combina herencia simple una clase en multiples y luego estas se combinan en una sola usando herencia multiple

## Polimorfismo

Dos clases hijas implementar la misma funcion del padre, pero tienen diferentes funcionalidades o comportamiento, esto se logra sobreescibiendo en las clases hijas, sobre la funcion heredada

**JAVA**

```java
class Parent {
  public void sayHello() {
    System.out.println("Hello!!!");
  }
}

class Daugther1 extends Parent {
  public void sayHello() {
    System.out.println("Hello, I am daugther1");
  }
  //sayHello outputs Hello, I am daugther1
}

class Daugther2 extends Parent {
  public void sayHello() {
    System.out.println("I am daugther2 and I say HELLO!!");
    //sayHello outputs I am daugther2 and I say HELLO!!
  }
}

class Daugther1 extends Parent {
  //sayHello outputs Hello!!!
}
```

Esto quiere decir, que la funcion primero sera buscada de la clase en la que se esta llamando, pero si no existe alli, entonces se busca en la clase padre.

Algunos lenguajes soportan funciones polimorficas, que son la misma funcion, pero que hacen diferentes cosas y aceptan diferentes tipos de parametros, dentro de la misma clase. La variante que se ejecuta depende del tipo de datos que se le ingresen

**JAVA**

```java
class Sums {
  public int sumNumbers(int a, int b) {
    System.out.println("Int sum");
    return a + b;
  }

  public float sumNumbers(float a, float b) {
    System.out.println("Float sum");
    return a + b *(float)9;
  }

  public void sumNumbers(double a, double b) {
    System.out.println("Double sum");
    System.out.println("Sum is: " + (a + b));
  }
}
```

## Interfaces

Son las instrucciones o descripciones de lo que un objeto debe hacer. Existe una lista de funciones a modo de prototype, es decir funciones declaradas sin cuerpo que se deben implementar en la clase

**JAVA**

```java
interface Vehicule {
  void speedUp(int speedVariation);
  void slowDown(int speedVariation);
}

class Car implements Vehicule {
  public void speedUp(int speedVariation) {

  }

  public void slowDown(int speedVariation) {
    
  }
}
```