---
banner_icon: 👅
banner: "![[full-moon_36176574191_o.jpg]]"
banner_y: 0.56
---


# package java.lang

El paquete `java.lang` es un paquete especial en Java que ==contiene clases y tipos fundamentales que son automáticamente importados en todos los programas Java.== No es necesario importar explícitamente las clases del paquete `java.lang`, ya que están disponibles globalmente en cualquier programa Java sin requerir una declaración de importación.

El paquete `java.lang` contiene clases y tipos esenciales que son utilizados ampliamente en la mayoría de los programas Java. Algunos de los tipos más comunes y fundamentales en este paquete incluyen:

1. **Object**: La clase `Object` es la clase raíz de todas las clases en Java. Cada clase que creas hereda directa o indirectamente de la clase `Object`. La clase `Object` proporciona métodos como `equals`, `hashCode`, `toString`, entre otros, que son utilizados en la mayoría de las clases.
2. **String**: La clase `String` es utilizada para representar cadenas de caracteres. Es una de las clases más utilizadas en Java y proporciona una amplia gama de métodos para manipular y trabajar con cadenas.
3. **Integer, Double, Boolean, etc.**: Estas clases envuelven tipos primitivos en objetos. Por ejemplo, `Integer` envuelve un valor `int` en un objeto, lo que permite realizar operaciones más avanzadas con números enteros.
4. **System**: La clase `System` proporciona métodos para interactuar con el sistema operativo y el entorno de ejecución. Por ejemplo, `System.out` es una instancia de `PrintStream` que se usa comúnmente para imprimir en la consola.
5. **Exception**: La clase `Exception` es la clase base para todas las excepciones en Java. Todas las clases de excepción heredan de esta clase, lo que permite capturar y manejar excepciones de manera uniforme.
6. **Thread**: La clase `Thread` se utiliza para trabajar con hilos de ejecución en Java. Permite crear, controlar y coordinar hilos de manera eficiente.
7. **Math**: La clase `Math` proporciona funciones matemáticas y operaciones comunes, como cálculos trigonométricos, logarítmicos y exponenciales.
8. **Enum**: A partir de Java 5, la clase `Enum` y otras clases relacionadas en el paquete `java.lang` se utilizan para implementar enumeraciones.

Estos son solo algunos ejemplos de las clases y tipos fundamentales proporcionados por el paquete `java.lang`. Debido a su importación automática, puedes usar estos tipos en cualquier programa Java sin necesidad de importar explícitamente el paquete. El paquete `java.lang` es un componente esencial del lenguaje y proporciona las bases para muchas de las características y funcionalidades de Java.


## Clase **`Object`**

La clase `Object` es una clase fundamental en Java que es la raíz de la jerarquía de clases en el lenguaje. Cada clase en Java, ya sea creada por el programador o proporcionada por el sistema, hereda directa o indirectamente de la clase `Object`. Por lo tanto, todos los objetos en Java tienen acceso a los métodos y funcionalidades definidos en la clase `Object`.

Algunos de los métodos más comunes y útiles proporcionados por la clase `Object` son:

1. **`equals(Object obj)`**: Compara dos objetos para verificar si son iguales. Por defecto, este método compara referencias de objetos, pero puede ser sobrescrito para comparar contenido si es necesario.
2. **`hashCode()`**: Devuelve un valor entero único para el objeto. Es utilizado por estructuras de datos basadas en hash, como `HashMap`, para almacenar y recuperar objetos de manera eficiente.
3. **`toString()`**: Devuelve una representación en cadena del objeto. Por defecto, devuelve el nombre de la clase seguido de la dirección de memoria del objeto. Este método se utiliza comúnmente para imprimir objetos en la consola.
4. **`getClass()`**: Devuelve el objeto `Class` que representa la clase del objeto en tiempo de ejecución. La clase `Class` proporciona información sobre la estructura y las capacidades de la clase.
5. **`finalize()`**: Este método es llamado por el recolector de basura antes de liberar la memoria ocupada por el objeto. Puede ser sobrescrito para liberar recursos externos antes de que el objeto sea destruido.
6. **`clone()`**: Crea y devuelve una copia superficial del objeto. Se debe tener cuidado al usar este método, ya que puede ser complicado mantener la integridad del objeto clonado.

La clase `Object` es especialmente útil para cuando se necesita implementar comportamientos comunes que aplican a todas las clases, como la comparación de objetos, la generación de cadenas representativas y la administración de la igualdad. Además, cuando se crea una clase personalizada, automáticamente heredará estos métodos de `Object`, aunque es posible sobrescribirlos según sea necesario para adaptar el comportamiento a la clase específica.

En resumen, la clase `Object` es la base de la jerarquía de clases en Java y proporciona métodos esenciales para la manipulación y comparación de objetos. Cada clase en Java, sin importar cuán compleja, hereda los métodos y funcionalidades definidos en `Object`.


## Clase **`String`** en Java:

==La clase `String` en Java es inmutable, lo que significa que una vez que se crea un objeto `String`, no se puede modificar su contenido.== Cualquier modificación a una cadena resultará en la creación de una nueva instancia de `String`.

Algunas operaciones comunes que se pueden realizar con la clase `String` incluyen:

- Concatenación de cadenas:
	```java
	String str1 = "Hola";
	String str2 = "Mundo";
	String resultado = str1 + " " + str2; // "Hola Mundo"
	```

- Comparación de cadenas:
	```java
	String a = "hola";
	String b = "Hola";
	boolean igual = a.equals(b); // false
	boolean igualIgnorandoCase = a.equalsIgnoreCase(b); // true
	```

- Obtener longitud de cadena:
	```java
	String mensaje = "¡Hola!";
	int longitud = mensaje.length(); // 6
	```

- Buscar y reemplazar:
	```java
	String original = "Java es genial";
	String reemplazado = original.replace("Java", "Python"); // "Python es genial"
	```


### StringBuilder

`StringBuilder` es una clase en Java que se utiliza para crear y manipular cadenas de caracteres de manera eficiente y mutable. A diferencia de la clase `String`, que es inmutable, `StringBuilder` permite modificar el contenido de una cadena sin crear múltiples instancias nuevas.

En otras palabras, `StringBuilder` es útil cuando necesitas realizar muchas operaciones de concatenación o modificación en una cadena sin incurrir en el costo de crear nuevos objetos `String` en cada operación. Esto mejora la eficiencia en situaciones en las que se requieren muchas manipulaciones de cadenas, como en bucles o en la construcción gradual de una cadena.

Ejemplo de uso de `StringBuilder`:
```java
StringBuilder sb = new StringBuilder();
sb.append("Hola");
sb.append(" ");
sb.append("Mundo");
String resultado = sb.toString(); // "Hola Mundo"
```

En este ejemplo, estamos utilizando un objeto `StringBuilder` para construir la cadena "Hola Mundo". Usamos el método `append()` para agregar cada parte de la cadena, y finalmente, utilizamos `toString()` para obtener la cadena completa.

Recuerda que si estás realizando operaciones de concatenación en un solo lugar sin la necesidad de modificar la cadena posteriormente, la clase `String` puede ser suficiente. Sin embargo, si necesitas manipular o concatenar cadenas en bucles u otras situaciones que puedan ser intensivas en recursos, usar `StringBuilder` puede ser más eficiente en términos de rendimiento.


### Interfaz `CharSequence`:

La interfaz `CharSequence` en Java ==es una interfaz que representa una secuencia de caracteres==. La clase `String` implementa esta interfaz, lo que significa que cualquier cadena de caracteres puede tratarse como una instancia de `CharSequence`.

Esta interfaz define varios métodos para acceder a los caracteres de la secuencia y manipularla. Algunos métodos importantes de la interfaz `CharSequence` incluyen:

- `length()`: Devuelve la longitud de la secuencia.
- `charAt(int index)`: Devuelve el carácter en el índice dado.
- `subSequence(int start, int end)`: Devuelve una subsecuencia de caracteres dentro del rango especificado.

El uso de la interfaz `CharSequence` permite escribir código más genérico que puede manejar diferentes tipos de secuencias de caracteres, incluyendo objetos `String` y otros tipos que implementen esta interfaz.

En resumen, las cadenas de caracteres (`String`) son fundamentales en Java para manejar texto. La clase `String` proporciona métodos para trabajar con cadenas de manera eficiente y efectiva. La interfaz `CharSequence` define un conjunto de métodos comunes para trabajar con secuencias de caracteres, lo que facilita el manejo de diferentes tipos de cadenas.


## Método `toString()`

El método `toString()` es un método muy común y útil en Java que pertenece a la clase `Object`. Este método se utiliza para obtener una representación en forma de cadena de un objeto. La representación resultante generalmente es utilizada para imprimir o mostrar información sobre el objeto en la consola, en archivos de registro o en interfaces de usuario.

Cuando se llama al método `toString()` en un objeto, por defecto, devuelve una cadena que incluye el nombre de la clase seguido de una representación hexadecimal de la dirección de memoria del objeto. Sin embargo, este comportamiento predeterminado no siempre es útil ni informativo, especialmente cuando se trabaja con clases personalizadas.

Por esta razón, es común sobrescribir el método `toString()` en clases personalizadas para proporcionar una representación más legible y significativa del objeto. Al sobrescribir este método, puedes devolver una cadena que incluya información relevante sobre el estado del objeto.

Ejemplo de sobrescritura del método `toString()`:

```java
public class Persona {
    private String nombre;
    private int edad;

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    @Override
    public String toString() {
        return "Nombre: " + nombre + ", Edad: " + edad;
    }
}

public class Main {
    public static void main(String[] args) {
        Persona persona = new Persona("Juan", 30);
        System.out.println(persona); // Imprime: Nombre: Juan, Edad: 30
    }
}
```

En este ejemplo, hemos sobrescrito el método `toString()` en la clase `Persona` para proporcionar una representación más informativa del objeto. Luego, cuando imprimimos un objeto `Persona`, la representación definida en el método `toString()` se mostrará en lugar de la representación predeterminada.

La sobrescritura del método `toString()` es una práctica común en la programación de Java, ya que facilita la depuración, el registro y la presentación de información en una forma más legible y significativa.


---

+ #polimorfismo 
+ #herencia
+ #Strings
+ #librerias 
+ #decoradores 