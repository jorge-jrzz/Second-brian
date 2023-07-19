---
banner: "![[spiro-agnew-and-lyndon-johnson-watch-the-apollo-11-liftoff_9460201254_o.jpg]]"
banner_y: 0.348
banner_icon: 👴
---

# Herencia

La herencia es un concepto fundamental en la Programación Orientada a Objetos (POO) que ==permite crear nuevas clases basadas en clases existentes.== En Java, la herencia se logra mediante la palabra clave `extends`, donde una clase hija hereda los atributos y métodos de una clase padre. ==La herencia permite la reutilización de código, la organización de clases en una jerarquía y la creación de relaciones de tipo generalización/especialización.==

Aquí tienes algunos aspectos importantes sobre la herencia en Java:

1. **Clase padre y clase hija:** En la herencia, la clase padre (también llamada superclase o clase base) es la clase de la cual se heredan los atributos y métodos, y la clase hija (también llamada subclase o clase derivada) es la clase que hereda esos atributos y métodos. La clase hija puede agregar nuevos atributos y métodos, o modificar los existentes.
2. **Sintaxis de herencia:** Para que una clase herede de otra clase, se utiliza la palabra clave `extends` seguida del nombre de la clase padre. La clase hija adquiere automáticamente los atributos y métodos públicos o protegidos de la clase padre.
	```java
	public class ClasePadre {
	    // Atributos y métodos de la clase padre
	}
	
	public class ClaseHija extends ClasePadre {
	    // Atributos y métodos adicionales de la clase hija
	}
	```

3. **Relación "es un":** La herencia establece una relación "es un" entre la clase hija y la clase padre. Por ejemplo, si tienes una clase `Animal` como clase padre y una clase `Perro` como clase hija, se puede decir que "un perro es un animal". Esto permite tratar a los objetos de la clase hija como objetos de la clase padre, lo que facilita la polimorfismo y el reemplazo de objetos.
4. **Métodos sobrescritos:** Una clase hija puede sobrescribir (redefinir) los métodos heredados de la clase padre para proporcionar una implementación específica para la clase hija. Esto se logra utilizando la misma firma de método en la clase hija y utilizando la anotación `@Override`. La sobrescritura de métodos permite adaptar el comportamiento heredado a las necesidades específicas de la clase hija.
	```java
	public class ClasePadre {
	    public void metodo() {
	        // Implementación de la clase padre
	    }
	}
	
	public class ClaseHija extends ClasePadre {
	    @Override
	    public void metodo() {
	        // Implementación específica de la clase hija
	    }
	}
	```

5. **Herencia múltiple:** Java no permite la herencia múltiple, lo que significa que una clase no puede heredar directamente de múltiples clases. Sin embargo, se puede lograr cierto grado de herencia múltiple utilizando interfaces, que permiten que una clase implemente múltiples interfaces.
6. **Clase Object:** Todas las clases en Java heredan implícitamente de la clase `Object`, que es la clase raíz en la jerarquía de clases. La clase `Object` proporciona métodos comunes como `toString()`, `equals()`, `hashCode()`, entre otros, que están disponibles para todas las clases.

La herencia es un concepto poderoso que permite la creación de jerarquías de clases y la reutilización de código en Java. Permite la organización estructurada y modular del código, facilita la aplicación del principio de sustitución de Liskov y promueve la flexibilidad y extensibilidad del sistema. Sin embargo, es importante utilizar la herencia de manera adecuada, evitando una jerarquía excesivamente profunda y frágil, y favoreciendo la composición y la interfaz en lugar de la herencia en ciertos casos.

![[Herencia.png| 400]]

### Code Smell

El término "code smell" (en español, "olor a código") se refiere a ciertos patrones o características en el código fuente de un programa que indican la posible existencia de un problema subyacente. ==Es una metáfora utilizada en el campo de la programación para describir señales que sugieren que hay una mala práctica de diseño o un posible error en el código.==
Los "code smells" son indicadores subjetivos y no necesariamente indican un error o un problema real. Sin embargo, pueden ser señales de que existe una oportunidad de mejorar el código, hacerlo más legible, mantenible y eficiente.

Algunos ejemplos comunes de "code smells" incluyen:

1. Duplicación de código: Cuando hay bloques de código repetidos en diferentes partes del programa, lo que puede dificultar el mantenimiento y la modificación del código.
2. Métodos o clases demasiado largos: Cuando los métodos o las clases son excesivamente largos, lo que puede dificultar la comprensión y la modificación del código. Esto puede ser un indicio de una falta de cohesión y responsabilidad única.
3. Clases con demasiadas responsabilidades: Cuando una clase realiza múltiples tareas o tiene muchas responsabilidades diferentes, lo que puede llevar a un código poco modular y difícil de mantener.
4. Comentarios excesivos: Cuando el código está plagado de comentarios excesivos que podrían ser indicativos de una falta de claridad en el diseño o la nomenclatura de las variables.
5. Dependencias excesivas: Cuando una clase depende de muchas otras clases o módulos, lo que puede hacer que el código sea más frágil y difícil de mantener.
6. Código con baja cohesión: Cuando el código de una clase o método no está centrado en una tarea específica o no cumple con un propósito claro.

Es importante destacar que los "code smells" no son errores en sí mismos, sino indicadores de posibles problemas. Identificar y abordar los "code smells" puede mejorar la calidad del código, facilitar el mantenimiento y mejorar la legibilidad y la eficiencia en el desarrollo de software. Sin embargo, es necesario realizar un análisis cuidadoso y utilizar el juicio profesional para determinar si un "code smell" es realmente problemático en un contexto específico.


## Palabra clave **`super`**

La palabra clave `super` en Java se utiliza para acceder a miembros (atributos y métodos) de la clase padre en una clase hija. Proporciona una forma de referenciar y llamar a la implementación de la clase padre desde la clase hija.

Aquí tienes algunos aspectos importantes sobre la palabra clave `super` y la sobreescritura de métodos:

1. *Acceso a miembros de la clase padre:* Al utilizar `super`, puedes acceder a los miembros (atributos y métodos) de la clase padre que están ocultos por miembros con el mismo nombre en la clase hija. Esto es útil cuando quieres utilizar o modificar la implementación de la clase padre desde la clase hija.
2. *Llamada al constructor de la clase padre:* Al construir una instancia de una clase hija, se debe llamar al constructor de la clase padre antes de ejecutar cualquier código adicional en el constructor de la clase hija. Esto se logra utilizando `super()` como la primera línea de código en el constructor de la clase hija.
	```java
	public class ClasePadre {
	    public ClasePadre() {
	        // Constructor de la clase padre
	    }
	}
	
	public class ClaseHija extends ClasePadre {
	    public ClaseHija() {
	        super(); // Llamada al constructor de la clase padre
	        // Código adicional en el constructor de la clase hija
	    }
	}
	```

	En este ejemplo, `super()` se utiliza para llamar al constructor de la clase padre `ClasePadre` antes de ejecutar el código adicional en el constructor de la clase hija `ClaseHija`.

3. *Sobreescritura de métodos:* La sobreescritura de métodos ocurre cuando una clase hija redefine (sobrescribe) un método heredado de la clase padre para proporcionar una implementación específica de la clase hija. La sobreescritura se realiza utilizando la anotación `@Override` para indicar que el método de la clase hija está sobrescribiendo un método de la clase padre.
	```java
	public class ClasePadre {
	    public void metodo() {
	        // Implementación de la clase padre
	    }
	}
	
	public class ClaseHija extends ClasePadre {
	    @Override
	    public void metodo() {
	        super.metodo(); // Llamada al método de la clase padre
	        // Implementación específica de la clase hija
	    }
	}
	```

	En este ejemplo, el método `metodo()` de la clase hija `ClaseHija` sobrescribe el método de la clase padre `ClasePadre`. Al utilizar `super.metodo()`, se puede acceder a la implementación del método en la clase padre antes de ejecutar el código adicional en el método de la clase hija.

La palabra clave `super` es esencial en la jerarquía de herencia para acceder a miembros de la clase padre y garantizar el correcto funcionamiento de la herencia y la sobreescritura de métodos. Permite una relación de complemento entre la clase hija y la clase padre, permitiendo el uso y extensión de la funcionalidad heredada.

##### Diferencia entre **`this`** y **`super`**

| _this_                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | _super_ |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| La palabra clave this se refiere al objeto actual en un método o constructor. El uso más común de este término es eliminar la confusión entre los atributos de clase y los parámetros del mismo nombre (porque un atributo de clase está sombreado por un parámetro de método constructor). Además de este uso, esta palabra se puede utilizar para: <br> - Invoca al constructor de la clase actual. <br> - Invocar el método de clase actual. <br> - Devuelve el objeto de clase actual. <br> - Pase un argumento en la llamada al método. <br> - Pase un argumento en la llamada al constructor | La palabra clave super se refiere a objetos de superclase (madre). Se utiliza para llamar a los métodos de la superclase y para acceder al constructor de la superclase. El uso más común de la palabra clave super es eliminar la confusión entre superclases y subclases que tienen métodos con el mismo nombre. <br> - ﻿﻿`super`: <br>   \+ Utilizado para referirse a la variable de instancia de la clase inmediatamente superior (clase madre). <br>   \+ Se usa para invocar métodos de la clase inmediatamente superior (clase madre). <br> - ﻿﻿`super()`: <br>   \+ Se utiliza para invocar al constructor de la clase inmediatamente superior (clase madre). 

### Modificadores de acceso

Los modificadores de acceso o accesibilidad son algunas palabras claves utilizadas en el lenguaje Java para definir el nivel de accesibilidad que los elementos de una clase (atributos y métodos) e incluso la propia clase puede tener los mismos elementos de otra clase.

##### Public
Este es el modificador menos **restrictivo** de todos. De esta manera, cualquier componente puede acceder a los miembros de la clase, las clases y las interfaces.

##### Protected
Al usar este modificador de acceso, los miembros de la clase y las clases son accesibles para otros elementos siempre que estén dentro del mismo package o, si pertenecen a otros packages, siempre que tengan una relación extendida (herencia), es decir, las clases secundarias pueden acceder a los miembros de su clase principal (o clase de abuelos, etc.).

##### Private
Este es el modificador de acceso **más restrictivo** de todos. Solo se puede acceder a los miembros definidos como privados desde dentro de la clase y desde ningún otro lugar, independientemente del paquete o la herencia.


## Preguntas

* ==¿Cuál es el orden correcto de los modificadores de visibilidad, de menor a mayor visibilidad?==
	`private < protected < public`
    La palabra llave con menor visibilidad es _private_, después viene _protected_ y después _public_.
    _private_ - solo visible dentro de la clase.
    _protected_ - visible dentro de la clase y también para las hijas.
    _public_ - visible en todo lugar.
    También tenga en cuenta que _protected_ está relacionado con la herencia.