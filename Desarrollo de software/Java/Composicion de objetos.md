---
banner: "![[astronaut-charles-duke-with-lunar-rover-on-moon_9460223832_o.jpg]]"
banner_y: 0.18
banner_icon: ⚛️
---

# Referencia a objetos

En Java, es posible tener atributos en una clase que sean referencias a otros objetos. Esto permite establecer relaciones y estructuras más complejas entre diferentes objetos.

Cuando un atributo de una clase es una referencia a otro objeto, se crea un enlace entre ambos. El atributo de referencia almacenará la dirección de memoria donde se encuentra el objeto referenciado.

Aquí tienes un ejemplo que ilustra cómo se puede utilizar una referencia a otro objeto como atributo:

```java
public class Persona {
    private String nombre;
    private int edad;
    private Direccion direccion; // Atributo de referencia a otro objeto

    public Persona(String nombre, int edad, Direccion direccion) {
        this.nombre = nombre;
        this.edad = edad;
        this.direccion = direccion;
    }

    // Métodos getter y setter para el atributo "direccion"
    public Direccion getDireccion() {
        return direccion;
    }

    public void setDireccion(Direccion direccion) {
        this.direccion = direccion;
    }
}

public class Direccion {
    private String calle;
    private String ciudad;

    public Direccion(String calle, String ciudad) {
        this.calle = calle;
        this.ciudad = ciudad;
    }

    // Métodos getter y setter para los atributos "calle" y "ciudad"
    // ...
}
```

En este ejemplo, la clase `Persona` tiene un atributo `direccion` que es una referencia a un objeto de la clase `Direccion`. El atributo `direccion` puede ser utilizado para acceder y manipular los datos de la dirección asociada a la persona.

Para establecer la referencia a un objeto `Direccion`, se puede pasar una instancia de `Direccion` al crear una instancia de `Persona` o utilizando el método `setDireccion`. Por ejemplo:

```java
Direccion direccion = new Direccion("Calle Principal", "Ciudad Ejemplo");
Persona persona = new Persona("John Doe", 30, direccion);

// O utilizando el método setter
Direccion nuevaDireccion = new Direccion("Otra Calle", "Otra Ciudad");
persona.setDireccion(nuevaDireccion);
```

Una vez establecida la referencia, se puede acceder a los métodos y atributos del objeto referenciado utilizando la notación de punto. Por ejemplo:

```java
String calle = persona.getDireccion().getCalle();
String ciudad = persona.getDireccion().getCiudad();
```

En resumen, la referencia a objetos permite establecer relaciones y estructuras más complejas en Java. Los atributos de referencia pueden ser utilizados para almacenar referencias a otros objetos y acceder a sus métodos y atributos. Esto es útil para modelar relaciones entre entidades y construir estructuras de datos más flexibles y organizadas.

# Valores NULL

En Java, el valor `null` se utiliza para indicar que una referencia no apunta a ningún objeto en la memoria. En otras palabras, cuando una variable de referencia tiene el valor `null`, significa que no está referenciando ningún objeto válido en ese momento.

Aquí tienes algunas cosas importantes que debes saber sobre el valor `null`:

1. Significado de `null`: El valor `null` representa la ausencia de un objeto. Se utiliza para indicar que una referencia no está inicializada o que ha sido desasignada.

2. Tipos de referencia y `null`: Solo las variables de referencia, es decir, aquellas que tienen un tipo de objeto (clase, interfaz, arreglo), pueden tener el valor `null`. Los tipos primitivos en Java, como `int`, `double`, `boolean`, no pueden tener el valor `null`.

3. Uso de `null`: Puedes asignar el valor `null` a una variable de referencia cuando deseas indicar que no hay un objeto válido asociado. Por ejemplo, después de desasignar un objeto o antes de asignar un objeto válido.

```java
Persona persona = null;  // Asignando el valor null a la variable de referencia "persona"
```

4. Manejo de `null`: Al usar una referencia que podría tener el valor `null`, debes asegurarte de verificar si es `null` antes de intentar acceder a cualquier método o atributo del objeto referenciado. Intentar acceder a un método o atributo en una referencia `null` causará una excepción `NullPointerException`.

```java
if (persona != null) {
    // Acceder a los métodos o atributos del objeto referenciado
    persona.metodo();
    int edad = persona.getEdad();
} else {
    // Manejar la situación cuando la referencia es null
    System.out.println("La referencia a persona es null.");
}
```

5. Comparación con `null`: Puedes comparar una referencia con el valor `null` utilizando el operador de igualdad `==`. Por ejemplo:

```java
if (persona == null) {
    // La referencia es null
} else {
    // La referencia no es null
}
```

Es importante tener en cuenta que el uso de `null` debe hacerse de manera adecuada y controlada. Un manejo incorrecto de las referencias `null` puede llevar a errores y excepciones en tiempo de ejecución. Es recomendable realizar una verificación cuidadosa de las referencias antes de utilizarlas para evitar `NullPointerExceptions` y asegurarse de que se asignen valores adecuados a las variables de referencia.