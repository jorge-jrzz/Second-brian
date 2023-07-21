---
banner_icon: 🕴️
banner: "![[ed-mitchell_29681523075_o.jpg]]"
banner_y: 0.42
---

# Interfaces

## ¿Herencia múltiple?

No, Java no admite herencia múltiple directa, lo que significa que una clase no puede heredar de múltiples clases directamente. Esto se debe a que la herencia múltiple puede llevar a problemas de ambigüedad y complejidad en la resolución de referencias y conflictos entre diferentes clases base.

Sin embargo, Java ofrece una forma limitada de herencia múltiple a través del uso de interfaces. Una clase puede implementar múltiples interfaces, lo que le permite heredar comportamientos de diferentes fuentes. Las interfaces son como "contratos" que una clase puede implementar, y estas pueden contener métodos abstractos que deben ser implementados por la clase.
Veamos un ejemplo para ilustrar cómo se logra cierto grado de herencia múltiple con interfaces en Java:

Supongamos que tenemos dos interfaces: `InterfazA` y `InterfazB`, ambas con un método abstracto llamado `metodo()`. Luego, una clase `ClaseHija` puede implementar ambas interfaces y, de esta manera, heredar comportamientos de ambas.
```java
// Interfaz A
public interface InterfazA {
    void metodo();
}

// Interfaz B
public interface InterfazB {
    void metodo();
}

// Clase que implementa ambas interfaces
public class ClaseHija implements InterfazA, InterfazB {
    @Override
    public void metodo() {
        System.out.println("Implementación del método en ClaseHija");
    }
}
```

En este ejemplo, `ClaseHija` implementa tanto `InterfazA` como `InterfazB`. La clase proporciona una única implementación del método `metodo()`, que cumple con los contratos de ambas interfaces.
A través del uso de interfaces, Java permite que una clase implemente múltiples comportamientos, evitando los problemas que podrían surgir con la herencia múltiple directa. Esto promueve un diseño más flexible y modular en el cual las clases pueden adaptar múltiples funcionalidades a través de la implementación de diferentes interfaces.

En conclusión, Java no permite herencia múltiple directa de clases, pero ofrece una forma de lograr herencia múltiple a través del uso de interfaces, lo que permite que una clase implemente múltiples comportamientos definidos en distintas interfaces. Esto brinda una flexibilidad significativa en el diseño y promueve la reutilización de código a través de contratos bien definidos.


## Características de las interfaces

Las interfaces en Java son una herramienta poderosa para lograr la abstracción y el polimorfismo. Una interfaz es similar a una clase abstracta, pero tiene ciertas diferencias clave:

1. Definición de interfaz: Una interfaz se define utilizando la palabra clave `interface`. A diferencia de una clase, una interfaz no puede contener implementaciones de métodos ni variables miembro.
	```java
	public interface MiInterfaz {
	    // Métodos abstractos (sin implementación)
	    void metodo1();
	    void metodo2();
	}
	```
	En este ejemplo, hemos definido una interfaz llamada `MiInterfaz` con dos métodos abstractos `metodo1()` y `metodo2()`. Las interfaces también pueden tener constantes, que son automáticamente consideradas como `public`, `static` y `final`.

2. Implementación de una interfaz: Para que una clase utilice una interfaz, debe implementarla utilizando la palabra clave `implements`. Una clase puede implementar múltiples interfaces separadas por coma.
	```java
	public class MiClase implements MiInterfaz {
	    @Override
	    public void metodo1() {
	        // Implementación del método 1
	    }
	
	    @Override
	    public void metodo2() {
	        // Implementación del método 2
	    }
	}
	```
	En este ejemplo, la clase `MiClase` implementa la interfaz `MiInterfaz` y proporciona una implementación para los métodos `metodo1()` y `metodo2()`.

3. Múltiple herencia a través de interfaces: Como mencionamos en la explicación anterior, Java no permite herencia múltiple de clases, pero sí permite que una clase implemente múltiples interfaces. Esto significa que una clase puede heredar comportamientos de múltiples fuentes a través de las interfaces que implementa.
4. Contratos: Las interfaces actúan como contratos que garantizan que cualquier clase que las implemente proporcionará la implementación de los métodos definidos en la interfaz. Esto promueve un diseño flexible, ya que las clases pueden adaptar diferentes funcionalidades a través de la implementación de diferentes interfaces.
5. Uso en polimorfismo: Las interfaces son esenciales para lograr el polimorfismo en Java. Al referenciar objetos a través de una referencia de tipo de interfaz, se puede tratar los objetos de diferentes clases que implementan esa interfaz de manera uniforme y acceder a sus métodos comunes.
	```java
	public static void main(String[] args) {
	    MiInterfaz objeto1 = new MiClase();
	    objeto1.metodo1(); // Llamada al método 1 de la interfaz
	
	    MiInterfaz objeto2 = new OtraClase();
	    objeto2.metodo1(); // Llamada al método 1 de otra clase que implementa la interfaz
	}
	```
	En este ejemplo, hemos creado dos objetos que son referenciados a través de una variable de tipo `MiInterfaz`. Ambos objetos pueden ser tratados de manera uniforme a través de la interfaz y acceder a los métodos definidos en ella.

Las interfaces son una parte fundamental de la Programación Orientada a Objetos en Java. Proporcionan una forma de definir contratos y comportamientos comunes, permiten el uso de polimorfismo y promueven un diseño flexible y extensible. Al utilizar interfaces de manera efectiva, puedes lograr una arquitectura modular y facilitar la colaboración entre diferentes componentes de tu código.

![[Interface.png| 450]]

---

- #herencia_multiple
- #interface