---
banner: "![[backpacking_5134455469_o.jpg]]"
banner_y: 0.168
banner_icon: 🏗️
---

# Constructores

Los constructores son métodos especiales utilizados para crear e inicializar objetos de una clase en Java. Se llaman automáticamente al crear una nueva instancia de la clase utilizando la palabra clave `new`. Los constructores tienen el mismo nombre que la clase y pueden tener parámetros para aceptar valores iniciales y configurar el estado inicial del objeto.

Aquí tienes algunos aspectos importantes sobre los constructores en Java:

1. Propósito de los constructores: Los constructores se utilizan para inicializar el estado de un objeto cuando se crea una nueva instancia de una clase. Permiten asignar valores a los atributos y realizar cualquier otra inicialización necesaria antes de que el objeto esté listo para su uso.

2. Sintaxis de un constructor: La sintaxis básica de un constructor es la siguiente:

```java
public class NombreClase {
    // Atributos y métodos de la clase
    
    // Constructor
    public NombreClase() {
        // Código de inicialización
    }
}
```

- `public`: Define el modificador de acceso del constructor, que determina desde dónde se puede acceder al constructor.
- `NombreClase`: Es el nombre de la clase, que debe coincidir con el nombre del archivo fuente `.java` que contiene la clase.
- `()`: Representa los paréntesis de los argumentos del constructor, que pueden estar vacíos si el constructor no acepta parámetros.
- Código de inicialización: Aquí se coloca el código necesario para inicializar los atributos u otras tareas de inicialización.

3. Constructores con parámetros: Los constructores pueden tener parámetros para aceptar valores iniciales. Esto permite configurar el estado inicial del objeto al momento de su creación. Por ejemplo:

```java
public class Persona {
    private String nombre;
    private int edad;

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```

En este ejemplo, el constructor `Persona` acepta dos parámetros: `nombre` y `edad`. Estos valores se utilizan para inicializar los atributos `nombre` y `edad` del objeto `Persona`.

4. Constructor por defecto: Si no se define ningún constructor en una clase, Java proporciona automáticamente un constructor por defecto sin parámetros. Este constructor no realiza ninguna inicialización especial y tiene una implementación vacía. Sin embargo, si defines un constructor con parámetros en la clase, el constructor por defecto no se proporcionará automáticamente y tendrás que definirlo explícitamente si lo necesitas.

5. Llamada a constructores desde otros constructores: En Java, es posible llamar a un constructor desde otro constructor de la misma clase utilizando la palabra clave `this`. Esto se conoce como llamada al constructor de la misma clase y se utiliza para reutilizar código común de inicialización. Por ejemplo:

```java
public class Persona {
    private String nombre;
    private int edad;

    public Persona(String nombre) {
        this(nombre, 0);  // Llamada al constructor con parámetros
    }

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```

En este ejemplo, el constructor `Persona(String nombre)` llama al constructor `Persona(String nombre, int edad)` utilizando `this(nombre, 0)`. Esto evita la duplicación de código y permite establecer un valor predeterminado para la edad si no se proporciona.

Los constructores son esenciales en la creación y configuración de objetos en Java. Permiten la inicialización de atributos y otras tareas necesarias para preparar el objeto para su uso. Al definir y utilizar constructores adecuadamente, puedes garantizar que los objetos se creen correctamente y tengan el estado inicial deseado.

# Variables estaticas 

Las variables estáticas en Java son variables que se asocian con la clase en lugar de con instancias individuales de la clase. Estas variables se declaran con la palabra clave `static` y se comparten entre todas las instancias de la clase. Pueden ser accedidas directamente desde la clase sin necesidad de crear una instancia de la misma.

Aquí tienes algunos aspectos importantes sobre las variables estáticas:

1. Declaración de variables estáticas: Las variables estáticas se declaran utilizando la palabra clave `static` antes de la declaración del tipo de dato. Pueden ser de cualquier tipo válido en Java, incluyendo tipos primitivos y tipos de referencia.

```java
public class MiClase {
    static int contador; // Variable estática
    static final double PI = 3.14159; // Constante estática (final)
}
```

En este ejemplo, `contador` es una variable estática que pertenece a la clase `MiClase`, mientras que `PI` es una constante estática. Ambas variables pueden ser accedidas directamente a través de la clase sin necesidad de crear una instancia de la misma.

2. Acceso a variables estáticas: Las variables estáticas se pueden acceder utilizando el nombre de la clase seguido del operador de punto (`.`) y el nombre de la variable estática.

```java
int valor = MiClase.contador; // Acceso a la variable estática "contador"
double valorPi = MiClase.PI; // Acceso a la constante estática "PI"
```

En este ejemplo, se accede a la variable estática `contador` y a la constante estática `PI` utilizando el nombre de la clase `MiClase`.

3. Compartición de valores: Las variables estáticas se comparten entre todas las instancias de la clase. Esto significa que cualquier modificación realizada en una variable estática afectará a todas las instancias de la clase.

4. Inicialización de variables estáticas: Las variables estáticas se inicializan una sola vez, cuando la clase es cargada por primera vez en la memoria. Esto ocurre antes de que se cree cualquier instancia de la clase. Pueden ser inicializadas directamente en su declaración o en un bloque de inicialización estático.

```java
public class MiClase {
    static int contador = 0; // Inicialización directa
    static {
        // Bloque de inicialización estático
        contador = 100;
    }
}
```

En este ejemplo, `contador` se inicializa directamente con el valor `0` y luego se actualiza a `100` en el bloque de inicialización estático.

5. Uso común de variables estáticas: Las variables estáticas son útiles para almacenar información compartida o datos que son relevantes para toda la clase. Se utilizan con frecuencia para implementar constantes, contadores, datos de configuración y métodos utilitarios que no dependen de una instancia específica de la clase.

Es importante tener en cuenta que las variables estáticas tienen algunas limitaciones. No pueden acceder a variables no estáticas ni a métodos no estáticos directamente, ya que se ejecutan en el contexto de la clase en lugar de una instancia particular.

En resumen, las variables estáticas en Java se asocian con la clase en lugar de con instancias individuales de la misma. Se declaran con la palabra clave `static` y se comparten entre todas las instancias de la clase. Son útiles para almacenar información compartida y datos relevantes para toda la clase.

## Preguntas

- A continuación, se presentan algunas declaraciones sobre el uso de los constructores, ==¿cuál es cierto?==
	Los constructores se utilizan para inicializar los atributos.