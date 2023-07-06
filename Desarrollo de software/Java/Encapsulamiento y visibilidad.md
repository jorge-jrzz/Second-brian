---
banner: "![[an-ancient-storm-in-the-jovian-atmosphere_9458010071_o.jpg]]"
banner_y: 0.728
banner_icon: 🪐
---

# Encapsulamiento 

El encapsulamiento es un principio fundamental de la Programación Orientada a Objetos (POO) que consiste en ocultar los detalles internos de una clase y proporcionar una interfaz pública para interactuar con los objetos. Se logra mediante el uso de modificadores de acceso y el uso de métodos getter y setter.

Aquí tienes algunos puntos clave sobre el encapsulamiento:

1. Modificadores de acceso: En Java, existen cuatro modificadores de acceso que se pueden aplicar a miembros de una clase: `public`, `private`, `protected` y el modificador de acceso por defecto (sin especificar un modificador). Estos modificadores controlan la visibilidad y el acceso a los miembros de una clase desde otras partes del código.

- `public`: El miembro es accesible desde cualquier lugar.
- `private`: El miembro es accesible solo desde dentro de la misma clase.
- `protected`: El miembro es accesible desde dentro de la misma clase, subclases y clases del mismo paquete.
- Modificador por defecto: El miembro es accesible solo desde dentro del mismo paquete.

2. Variables de instancia privadas: Se considera una buena práctica declarar las variables de instancia como `private`, lo que significa que solo se pueden acceder a ellas desde dentro de la misma clase. Esto oculta los detalles internos y protege los datos de la clase contra modificaciones no controladas.

3. Métodos getter y setter: Los métodos getter y setter se utilizan para acceder y modificar las variables de instancia privadas desde fuera de la clase. Estos métodos proporcionan una interfaz pública para interactuar con los datos de la clase, permitiendo un control y validación adecuados de los valores asignados o recuperados.

```java
public class Persona {
    private String nombre; // Variable de instancia privada

    // Método getter para acceder al nombre
    public String getNombre() {
        return nombre;
    }

    // Método setter para modificar el nombre
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
}
```

En este ejemplo, la variable de instancia `nombre` se declara como `private`, y los métodos `getNombre` y `setNombre` se utilizan para obtener y modificar el valor del nombre, respectivamente. Esto garantiza que el acceso a la variable `nombre` se realice de forma controlada a través de los métodos y permite la validación y lógica adicional si es necesario.

El encapsulamiento promueve la seguridad y la integridad de los datos al controlar el acceso a ellos y proporcionar una interfaz coherente para interactuar con los objetos. Además, al ocultar los detalles internos, permite realizar cambios en la implementación interna sin afectar el código que utiliza la clase. Esto mejora la modularidad, el mantenimiento y la reutilización del código.

En resumen, el encapsulamiento en Java implica ocultar los detalles internos de una clase y proporcionar una interfaz controlada y segura para interactuar con los objetos. Es un principio clave para garantizar la encapsulación de datos y la coherencia en la interacción con los objetos.