# Metodos de clase

## Metodos de Instancia

Son funciones aplicables a las intacias de la clase, pueden ser publicas o privadas, pueden recibir parametros y retornar valores, para invocar se hace

```
objetoDeUnaClase.metodo_de_obj(params)
```

## Metodos de Clase

Son funciones que se aplican sobre la clase unicamente, de igual manera reciben paramentros y devuelven valores

```
UnaClase.unMetodoDeClase(params)
```

## Como usar una interfaz

**JAVA**

```java
interface Vehicule {
  void speedUp(int speedVariation);
  void slowDown(int speedVariation);
}

class Car implements Vehicule {
  public void speedUp(int speedVariation) {
    System.out.println("Car() -> Speed Up");
  }

  public void slowDown(int speedVariation) {
    System.out.println("Car() -> Slow Down");
  }
}

class Motorcicle implements Vehicule {
  public void speedUp(int speedVariation) {
    System.out.println("Motorcicle() -> Speed Up");
  }

  public void slowDown(int speedVariation) {
    System.out.println("Motorcicle() -> Slow Down");
  }
}

// In class Main:
public static void executeSpeedUp(Vehicule vehicule) {
  //code
  car.speedUp(15)
}

// In main function:
Car car = new Car();
Motorcicle moto = new Motorcicle();
executeSpeedUp(car);
executeSpeedUp(moto);
```

Esto quiere decir que para ejecutae una interfaz, se va  crear una funcion de clase en Main, que requiere como parametro a un objeto de la clase que implemente la interfaz. Esto es utul en cuanto se puede pasar a esa funcion cualquiero objeto, de cualquier clase que implemente esa funcion y podra ejecutar, el codigo sobre ese objeto sea cual sea


**Ejemplo**

**Pseduo**

```
Interfaz Usuarios
  metodo getUsuarios()

clase UsuariosTXT implementa Interfaz Usuarios
  metodo getUsuarios()
    leer fichero.txt
    return todas las lineas

clase UsuariosBBDD implementa Interfaz Usuarios
  metodo getUsuarios()
    conectarme a mySQL
    ejecutar "SElECT*FROM..."
    return todos los resultados


funcion listarUsuarios(clase impl inter Usuarios)
  de la interfaz usuarios ejecute getUsuarios()


listarUsuarios(obj de class UsuariosTXT)
```

La funcion que implementa la interfaz, se denomina Wrapper

## Recursividad

Es llamar a la funcion, dentro de la misma funcion, una y otra vez y se detiene en un caso o prblema base. Las llamadas a la funcion subsecuentes se hacen con parametros ligeramente a los originales.