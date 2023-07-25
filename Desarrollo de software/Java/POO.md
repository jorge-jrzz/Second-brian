---
banner_icon: 🌮
banner: "![[apollo-17-commandservice-modules-photographed-from-lunar-module-in-orbit_52477538895_o.jpg]]"
banner_y: 0.224
---

# Programación Orientada a Objetos

La POO es un paradigma de programación que se basa en la idea de organizar el código en objetos que contienen datos y métodos relacionados.

Algunos de los conceptos clave en la POO incluyen:

1. **Clases y objetos**: Las clases son plantillas o estructuras que definen las propiedades y comportamientos de los objetos. Los objetos son instancias concretas de una clase, que pueden tener datos únicos y realizar operaciones específicas.

2. **Encapsulamiento**: Es el concepto de ocultar los detalles internos de una clase y proporcionar una interfaz pública para interactuar con los objetos. Se logra mediante el uso de modificadores de acceso (public, private, protected) y métodos getter y setter.

3. **Herencia**: Es un mecanismo que permite crear nuevas clases basadas en clases existentes. La herencia permite la reutilización de código y define una relación "es-un" entre las clases.

4. **Polimorfismo**: Es la capacidad de un objeto para tomar muchas formas diferentes. En Java, se puede lograr a través de la herencia y la implementación de interfaces, lo que permite que objetos de diferentes clases sean tratados de manera uniforme.

5. **Abstracción**: Es el proceso de identificar las características esenciales de un objeto y crear una representación simplificada de dicho objeto en forma de una clase abstracta o una interfaz.

# Características

| Característica          | Programación Orientada a Objetos (POO)                                      | Programación Secuencial                                                       |
|-------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Organización del código | El código se organiza en objetos que agrupan datos y comportamientos relacionados. | El código se organiza en funciones y procedimientos secuenciales.                  |
| Reutilización de código | La reutilización de código se promueve a través de la herencia y la composición.     | La reutilización de código puede ser más limitada, lo que puede llevar a la duplicación de código. |
| Modularidad             | El código se divide en unidades independientes (clases) que pueden ser modificadas y probadas por separado.  | El código puede volverse extenso y difícil de mantener a medida que el programa crece.    |
| Abstracción             | Permite representar conceptos del mundo real mediante clases y objetos.     | La abstracción puede ser limitada, ya que el código se centra más en la secuencia de instrucciones. |
| Polimorfismo            | Permite que los objetos de diferentes clases sean tratados de manera uniforme.      | No hay soporte directo para el polimorfismo, lo que puede dificultar la flexibilidad del código. |
| Encapsulamiento         | Los detalles internos de una clase se ocultan, y solo se expone una interfaz pública para interactuar con los objetos. | No hay una estructura formal para el encapsulamiento, lo que puede resultar en un acceso no controlado a los datos. |

###### <mark class="hltr-orange">Ventajas de la POO:</mark>
- **Reutilización** de código: La herencia y la composición permiten aprovechar y extender el código existente, lo que reduce la duplicación y mejora la eficiencia.
- **Modularidad**: La división del código en unidades independientes facilita la comprensión, el mantenimiento y la colaboración en proyectos de gran escala.
- **Abstracción**: Permite modelar y representar conceptos del mundo real de manera más intuitiva, lo que facilita el diseño y la implementación del software.
- **Flexibilidad y extensibilidad**: El polimorfismo permite tratar objetos de diferentes clases de manera uniforme, lo que brinda flexibilidad y extensibilidad al código.

###### <mark class="hltr-orange">Desventajas de la POO:</mark>
- **Curva de aprendizaje**: La POO puede requerir un enfoque conceptual y un c
- ambio de mentalidad para aquellos acostumbrados a la programación secuencial.
- **Overhead**: La estructura y abstracción adicional en la POO pueden resultar en un ligero aumento en el consumo de recursos y rendimiento en comparación con un enfoque secuencial más eficiente.
- **Complejidad potencial**: La modularidad y flexibilidad de la POO pueden dar lugar a un diseño complicado y una mayor complejidad si no se planifica y gestiona adecuadamente.

Es importante tener en cuenta que la elección del paradigma de programación depende del contexto, los requisitos del proyecto y las preferencias del equipo de desarrollo. La POO es ampliamente utilizada y ofrece muchas ventajas para el desarrollo de software, pero es importante considerar las características y desventajas antes de adoptarla en un proyecto en particular.

# Clases

Para crear una clase en Java, debes seguir los siguientes pasos:

1. Declarar la clase: Utiliza la palabra clave `class` seguida del nombre de la clase. Por convención, los nombres de las clases comienzan con una letra mayúscula. Aquí tienes un ejemplo básico de declaración de una clase llamada "MiClase":

```java
public class MiClase {
    // Código de la clase
}
```

2. Agregar variables y métodos: Dentro de la clase, puedes agregar variables para almacenar datos y métodos para definir el comportamiento de los objetos. Aquí tienes un ejemplo de cómo agregar una variable y un método a la clase "MiClase":

```java
public class MiClase {
    // Variable
    private int miVariable;

    // Método
    public void miMetodo() {
        // Código del método
    }
}
```

3. Crear una instancia (objeto) de la clase: Para utilizar una clase, debes crear una instancia (objeto) de la misma. Utiliza el operador `new` seguido del nombre de la clase y paréntesis. Puedes asignar la instancia a una variable para poder acceder y utilizar los miembros de la clase. Aquí tienes un ejemplo de cómo crear una instancia de la clase "MiClase":

```java
MiClase objeto = new MiClase();
```

En este ejemplo, se crea una instancia de la clase "MiClase" y se asigna a la variable `objeto`.

A partir de este punto, puedes acceder a los miembros (variables y métodos) de la clase utilizando el operador de punto (`.`) seguido del nombre del objeto y el miembro al que deseas acceder. Por ejemplo:

```java
objeto.miVariable = 10;    // Acceder a la variable
objeto.miMetodo();         // Llamar al método
```

Recuerda que los miembros de la clase pueden tener modificadores de acceso, como `public`, `private` o `protected`, que determinan su visibilidad y acceso desde otras partes del código.

Ten en cuenta que es común tener una clase principal (con un método `main`) que actúa como punto de entrada para la ejecución del programa. Esta clase principal puede crear instancias de otras clases y utilizar sus funcionalidades.

![[Instancias.png| 650]]

## Valores default 

En Java, los valores por defecto son aquellos asignados automáticamente a las variables si no se les ha proporcionado un valor explícito. Los valores por defecto dependen del tipo de dato de la variable y se asignan automáticamente cuando se crea una instancia de una clase o se declara una variable.

Lista de los valores por defecto para cada tipo de dato en Java:

- Para tipos de dato numéricos enteros (`byte`, `short`, `int`, `long`): El valor por defecto es `0`.
- Para tipo de dato numérico de punto flotante (`float`, `double`): El valor por defecto es `0.0`.
- Para tipo de dato `boolean`: El valor por defecto es `false`.
- Para tipo de dato `char`: El valor por defecto es el carácter nulo `'\u0000'`.
- Para tipos de dato de referencia (clases, interfaces, arreglos): El valor por defecto es `null`.

Ejemplo que muestra los valores por defecto de variables sin asignarles un valor explícito:

```java
public class ValoresDefault {
    static int numero;        // Valor por defecto: 0
    static double decimal;    // Valor por defecto: 0.0
    static boolean estado;    // Valor por defecto: false
    static char caracter;     // Valor por defecto: '\u0000'
    static String texto;      // Valor por defecto: null

    public static void main(String[] args) {
        System.out.println("Número: " + numero);
        System.out.println("Decimal: " + decimal);
        System.out.println("Estado: " + estado);
        System.out.println("Carácter: " + caracter);
        System.out.println("Texto: " + texto);
    }
}
```

La salida de este código será:

```bash
Número: 0
Decimal: 0.0
Estado: false
Carácter:
Texto: null
```

Es importante tener en cuenta los valores por defecto al utilizar variables sin inicializarlas explícitamente, ya que pueden afectar el comportamiento del programa si se asume incorrectamente un valor por defecto diferente. Por lo tanto, es recomendable asignar valores explícitos a las variables antes de utilizarlas para evitar confusiones.

# Referencias

En Java, las referencias se utilizan para acceder y manipular objetos en memoria. Una referencia es un tipo de dato que almacena la ubicación en memoria de un objeto, en lugar de contener directamente los datos del objeto en sí. A través de las referencias, es posible acceder a los métodos y variables de instancia de un objeto, así como compartir y manipular el objeto en diferentes partes del código.

Cuando se crea un objeto en Java utilizando el operador `new`, se reserva un bloque de memoria para almacenar los datos del objeto. La referencia, que es un tipo de dato especializado para el tipo de objeto, se utiliza para señalar a ese bloque de memoria.

Aquí tienes un ejemplo que ilustra cómo funciona la referencia en Java:

```java
public class Referencias {
    public static void main(String[] args) {
        // Creación de un objeto de la clase "Persona"
        Persona persona1 = new Persona("John", 25);
        
        // Creación de otra referencia al mismo objeto
        Persona persona2 = persona1;
        
        // Acceso a los datos del objeto a través de las referencias
        System.out.println(persona1.getNombre());  // John
        System.out.println(persona2.getEdad());    // 25
        
        // Modificación de los datos del objeto a través de una de las referencias
        persona2.setNombre("Jane");
        persona2.setEdad(30);
        
        // Acceso a los datos actualizados del objeto a través de ambas referencias
        System.out.println(persona1.getNombre());  // Jane
        System.out.println(persona2.getEdad());    // 30
    }
}

class Persona {
    private String nombre;
    private int edad;
    
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
    
    // Métodos getter y setter
    
    public String getNombre() {
        return nombre;
    }
    
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
    
    public int getEdad() {
        return edad;
    }
    
    public void setEdad(int edad) {
        this.edad = edad;
    }
}
```

En este ejemplo, se crea un objeto de la clase `Persona` y se asigna una referencia (`persona1`) a ese objeto. Luego, se crea otra referencia (`persona2`) y se le asigna el valor de `persona1`. Ambas referencias apuntan al mismo objeto en memoria.

Al modificar los datos del objeto a través de una de las referencias (`persona2`), los cambios son visibles a través de ambas referencias (`persona1` y `persona2`), ya que ambas apuntan al mismo objeto en memoria.

Es importante entender que, en Java, las referencias almacenan direcciones de memoria, no los datos del objeto en sí. Esto permite la creación y manipulación de objetos dinámicos y la gestión eficiente de la memoria en tiempo de ejecución.

## Preguntas

+ ==Según lo que escuchó en el video, seleccione la alternativa que exprese la idea central del paradigma de Orientación de objetos.==
	Los datos y la funcionalidad de una entidad van de la mano.

- ==De acuerdo con las situaciones mencionadas en el video, elija la única alternativa que **no sea** un signo de la programación procedural.==
	Múltiples equipos trabajando en un solo proyecto. Para que varios equipos puedan trabajar en el mismo proyecto, es necesario que las responsabilidades de cada código estén bien definidas y claras, evitando conflictos al hacer cambios y evoluciones. El código con responsabilidades cohesivas es un signo del paradigma OO.

- ==¿Cómo llamamos, en orientación a objeto, las características de una clase?==
    Atributo

- Jonas creó un objeto de tipo Persona para representar un personaje de un juego que está creando.
	Observe la clase que creó:
	
	```java
	public class Persona {
	
		String nombre;
		int edad;
		int peso;
	
	}
	```
	==¿Cuál de las siguientes es la opción correcta para crear un objeto y establecer un valor para sus atributos?==
	```java
	Persona heroe = new Persona();
	heroe.nombre =  "Jonny";
	```
	Correcto. El objeto se crea y su referencia se asigna a la variable heroe, luego el atributo de nombre se define en el lugar correcto para que la asignación sea exitosa.

- Usando lo aprendido sobre referencias y asignación de valores definiremos una clase a continuación.
	```java
	public class Cuenta {
	    double saldo;
	}
	```
	==A partir de esta clase, diga qué imprime el código:==
	```java
	public class Test {
	
	    public static void main(String[] args) {
	
	        Cuenta miCuenta = new Cuenta();
	        miCuenta.saldo = 500.0;
	        Cuenta otraCuenta = miCuenta;
	        otraCuenta.saldo += 1000.0;
	
	        System.out.println(miCuenta.saldo);
	    }
	}
	```
	Imprime 1500, porque las dos referencias (miCuenta y otraCuenta) apuntan al mismo objeto, lo que hace que se agregue la cantidad 1000 a los 500 anteriores.

