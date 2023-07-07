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

## <mark class="hltr-cyan">Getters</mark> 

Los getters, también conocidos como métodos de acceso, son métodos que se utilizan para obtener el valor de un atributo privado de una clase desde fuera de la misma. Proporcionan una forma controlada de acceder a los datos encapsulados dentro de un objeto. Los getters siguen la convención de nomenclatura común de comenzar con el prefijo "get" seguido del nombre del atributo en camelCase.

Aquí hay algunos aspectos importantes sobre los getters en Java:

1. Propósito de los getters: Los getters se utilizan para permitir el acceso a los atributos privados de una clase desde fuera de ella. Al utilizar getters, se evita el acceso directo a los atributos y se proporciona una interfaz pública para obtener los valores de esos atributos. Esto ayuda a mantener el encapsulamiento y permite aplicar lógica adicional en el proceso de obtención del valor si es necesario.

2. Convención de nomenclatura: Por convención, el nombre de un getter comienza con el prefijo "get" seguido del nombre del atributo en camelCase. Por ejemplo, si tienes un atributo privado llamado `nombre`, el getter asociado se llamaría `getNombre()`.

3. Sintaxis de un getter: La sintaxis básica de un getter es la siguiente:

```java
public tipoDeDato getNombreAtributo() {
    // Lógica adicional (opcional)
    return nombreAtributo;
}
```

- `public`: Define el modificador de acceso del getter, que determina desde dónde se puede acceder al método.
- `tipoDeDato`: Especifica el tipo de dato que el getter va a devolver.
- `getNombreAtributo()`: Es el nombre del getter que sigue la convención de nomenclatura.

4. Ejemplo de un getter:

```java
public class Persona {
    private String nombre;

    public String getNombre() {
        return nombre;
    }
}
```

En este ejemplo, el getter `getNombre()` permite obtener el valor del atributo `nombre` de un objeto `Persona`. Desde fuera de la clase `Persona`, se puede llamar al getter para obtener el valor actual del nombre:

```java
Persona persona = new Persona();
String nombre = persona.getNombre();
```

Es importante tener en cuenta que los getters solo devuelven el valor del atributo, no proporcionan una referencia directa al objeto subyacente. Esto significa que, si el atributo es un objeto, se devuelve una copia de la referencia al objeto, no el objeto en sí. Cualquier modificación realizada en la referencia devuelta por el getter no afectará directamente al objeto original.

En resumen, los getters son métodos utilizados para obtener los valores de los atributos privados de una clase desde fuera de ella. Proporcionan una forma controlada y encapsulada de acceder a los datos de un objeto. Al seguir las convenciones de nomenclatura y utilizar getters apropiadamente, se promueve el encapsulamiento y se facilita el mantenimiento y la evolución del código.

## <mark class="hltr-cyan">Setters</mark> 

Los setters, también conocidos como métodos de modificación, son métodos utilizados para asignar un nuevo valor a un atributo privado de una clase. Proporcionan una forma controlada de modificar los datos encapsulados dentro de un objeto. Los setters siguen la convención de nomenclatura común de comenzar con el prefijo "set" seguido del nombre del atributo en camelCase.

Aquí tienes algunos aspectos importantes sobre los setters en Java:

1. Propósito de los setters: Los setters se utilizan para permitir la modificación de los atributos privados de una clase desde fuera de ella. Al utilizar setters, se evita el acceso directo a los atributos y se proporciona una interfaz pública para asignar nuevos valores a esos atributos. Esto ayuda a mantener el encapsulamiento y permite aplicar lógica adicional en el proceso de asignación del valor si es necesario.

2. Convención de nomenclatura: Por convención, el nombre de un setter comienza con el prefijo "set" seguido del nombre del atributo en camelCase y, en general, no devuelve ningún valor. Por ejemplo, si tienes un atributo privado llamado `nombre`, el setter asociado se llamaría `setNombre()`.

3. Sintaxis de un setter: La sintaxis básica de un setter es la siguiente:

```java
public void setNombreAtributo(tipoDeDato nuevoValor) {
    // Lógica adicional (opcional)
    nombreAtributo = nuevoValor;
}
```

- `public`: Define el modificador de acceso del setter, que determina desde dónde se puede acceder al método.
- `void`: Indica que el setter no devuelve ningún valor.
- `setNombreAtributo(tipoDeDato nuevoValor)`: Es el nombre del setter que sigue la convención de nomenclatura. `tipoDeDato` representa el tipo de dato del atributo y `nuevoValor` es el nuevo valor que se va a asignar al atributo.

4. Ejemplo de un setter:

```java
public class Persona {
    private String nombre;

    public void setNombre(String nuevoNombre) {
        nombre = nuevoNombre;
    }
}
```

En este ejemplo, el setter `setNombre()` permite asignar un nuevo valor al atributo `nombre` de un objeto `Persona`. Desde fuera de la clase `Persona`, se puede llamar al setter para asignar un nuevo valor al nombre:

```java
Persona persona = new Persona();
persona.setNombre("John Doe");
```

Es importante tener en cuenta que los setters permiten aplicar lógica adicional, como validaciones, antes de asignar el nuevo valor al atributo. Esto puede ayudar a garantizar que los datos asignados cumplan con ciertas reglas o restricciones antes de ser almacenados.

En resumen, los setters son métodos utilizados para asignar un nuevo valor a los atributos privados de una clase desde fuera de ella. Proporcionan una forma controlada y encapsulada de modificar los datos de un objeto. Al seguir las convenciones de nomenclatura y utilizar setters adecuadamente, se promueve el encapsulamiento y se facilita el mantenimiento y la evolución del código.

## Preguntas 

+ Romulo creó una clase con varios atributos privados, pero no sabe exactamente qué ventaja utilizar este enfoque. ==¿Que opcione define mejor la ventaja de usar atributos privados?==
	La implementación interna se puede modificar sin afectar ningún código fuera de la clase misma.