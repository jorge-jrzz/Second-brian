---
banner_icon: ⚓
banner: "![[discovery-seen-from-mir_9459341204_o.jpg]]"
banner_y: 0.264
---

# Clases abstractas

Las clases abstractas en Java son clases que no pueden ser instanciadas directamente, lo que significa que no se pueden crear objetos directamente a partir de ellas. En cambio, se utilizan como clases base para otras clases, proporcionando una estructura común y definiendo métodos que deben ser implementados por las clases hijas.

**Definición de una clase abstracta:** Para declarar una clase como abstracta, se utiliza la palabra clave `abstract` antes de la palabra clave `class`.
```java
public abstract class ClaseAbstracta {
	// Atributos y métodos (incluso métodos abstractos)...
}
```

### Métodos abstractos:
Una clase abstracta puede contener métodos abstractos, que son métodos declarados sin una implementación concreta en la clase abstracta. Estos métodos deben ser implementados por las clases hijas. Para declarar un método abstracto, se omite el cuerpo del método y se utiliza la palabra clave `abstract` antes del tipo de retorno del método.
```java
public abstract class ClaseAbstracta {
	public abstract void metodoAbstracto();
}
```

En este ejemplo, `metodoAbstracto()` es un método abstracto que debe ser implementado por las clases hijas de `ClaseAbstracta`.

**Clases hijas y la implementación de métodos abstractos:** Cualquier clase que herede de una clase abstracta debe proporcionar implementaciones para todos los métodos abstractos de la clase padre. Si una clase hija no proporciona implementaciones para todos los métodos abstractos, también debe declararse como abstracta.
```java
public class ClaseHija extends ClaseAbstracta {
    @Override
    public void metodoAbstracto() {
        // Implementación del método abstracto en la clase hija
    }
}
```

En este ejemplo, `ClaseHija` es una clase hija que hereda de `ClaseAbstracta` y proporciona una implementación para el método abstracto `metodoAbstracto()`.

**Uso de clases abstractas:** Las clases abstractas se utilizan cuando deseas definir una estructura común para un grupo de clases relacionadas, pero no deseas que la clase base sea instanciada directamente. Las clases abstractas permiten definir comportamientos comunes y obligar a las clases hijas a implementar ciertos métodos específicos.

**Relación con el polimorfismo:** Las clases abstractas son fundamentales para el polimorfismo en Java. Al referenciar objetos de clases hijas a través de una referencia de tipo de clase abstracta, se pueden tratar los objetos de diferentes clases hijas de manera uniforme y acceder a sus métodos comunes, incluidos los métodos abstractos.

En resumen, las clases abstractas son clases que no pueden ser instanciadas directamente y se utilizan como clases base para otras clases relacionadas. Pueden contener métodos abstractos que deben ser implementados por las clases hijas. Las clases abstractas proporcionan una estructura común y son esenciales para el polimorfismo en Java, permitiendo tratar objetos de clases hijas de manera uniforme a través de una interfaz común definida en la clase abstracta.

##### Diferencia entre **interfaz** y **clase abstracta**

| *Interfaz*                                                                                    | *Clase abstracta*                                               |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| Palabra clave: **`implements`**.                                                              | Palabra clave: **`extends`**.                                   |
| La interfaz admite gherencia multiple.                                                        | La clase abstracta no admite herencia multiple.                 |
| Proporciona una abstracción absoluta y no puedo tener implementaciones de métodos.            | Puede tener métodos con implementaciones.                      |
| La interfaz no contiene constructor.                                                           | La clase abstracta contiene constructor.                         |
| La interfaz no puede tener modificador de acceso, por defecto todos los accesos son públicos. | La clase abstracta puede tener modificadores de acceso.         |
| Los miembros de la interfaz no pueden ser `static`.                                           | Solo los miembros completamente abstractos pueden ser `static`. |


## Preguntas

- ==¿Cuál de las siguientes afirmaciones es verdadera sobre las clases abstractas?==
	No se pueden ser instanciadas. Para crear una instancia, primero debemos crear una clase hija no abstracta. Una clase abstracta representa un concepto, algo abstracto, y el compilador no permite instanciar un objeto de esa clase. Para crear una instancia, es necesario crear primero una clase hija no abstracta.

- ==¿Cuál de las siguientes afirmaciones es verdadera sobre los métodos abstractos?==
	No tienen cuerpo (implementación), solo definen la firma, un método abstracto define solo la firma (visibilidad, retorno, nombre del método y parámetros).

- ==Acerca de las clases y métodos abstractos, de las siguientes declaraciones, cuáles son verdaderas?==
	- Las clases abstractas son útiles cuando queremos utilizar comportamientos y atributos basados ​​en clases con comportamientos comunes.
	- Usamos métodos abstractos cuando queremos "forzar" a un hijo concreto (clase concreta) a implementar un método. Ese es el significado de los métodos abstractos, garantizar que el hijo implemente un comportamiento.

---

* #clases_abstractas
* #metodos_abstractos