---
banner_icon: 💅
banner: "![[crater-tsiolkovsky_9457380631_o.jpg]]"
banner_y: 0.324
---

# Métodos 

Los métodos en Java son bloques de código que realizan tareas específicas. Estos métodos pueden recibir argumentos, realizar cálculos, acceder y manipular variables, y devolver valores o realizar acciones sin retorno.

Aquí hay algunos conceptos clave relacionados con los métodos en Java:

1. Declaración de método: Para declarar un método, se utiliza la siguiente sintaxis:

```java
[modificadores] tipoRetorno nombreMetodo([argumentos]) {
    // Cuerpo del método
    // Puede contener declaraciones de variables, sentencias y expresiones
    // Puede incluir la palabra clave return para devolver un valor
}
```

- `modificadores`: Pueden ser opcionales y controlan el acceso y comportamiento del método (por ejemplo, `public`, `private`, `protected`, `static`, entre otros).
- `tipoRetorno`: Especifica el tipo de dato que el método devuelve. Puede ser un tipo primitivo, un tipo de objeto o `void` si el método no devuelve ningún valor.
- `nombreMetodo`: Es el nombre del método.
- `argumentos`: Son los parámetros que el método puede recibir. Pueden ser opcionales y permiten pasar valores al método para su procesamiento.

2. Llamada a un método: Para llamar a un método y ejecutar su código, se utiliza la siguiente sintaxis:

```java
nombreMetodo([argumentos]);
```

- `nombreMetodo`: Es el nombre del método al que se desea llamar.
- `argumentos`: Son los valores que se pasan al método en caso de que tenga parámetros.

3. Retorno de valores: Si un método tiene un tipo de retorno distinto de `void`, debe incluir una sentencia `return` para devolver un valor compatible con el tipo de retorno. Por ejemplo:

```java
public int sumar(int a, int b) {
    int suma = a + b;
    return suma;
}
```

En este ejemplo, el método `sumar` recibe dos argumentos `a` y `b`, realiza la suma y devuelve el resultado como un valor entero.

4. Paso de argumentos: Los argumentos se pasan a los métodos por valor. Esto significa que se crea una copia de los valores de los argumentos en las variables locales del método. Cualquier modificación realizada en las variables locales no afectará los valores originales fuera del método.

5. Sobrecarga de métodos: En Java, es posible tener varios métodos con el mismo nombre pero con diferentes listas de argumentos. Esto se conoce como sobrecarga de métodos. Los métodos sobrecargados deben tener firmas de método diferentes, lo que significa que deben tener diferentes tipos o cantidades de argumentos.

Aquí tienes un ejemplo que ilustra estos conceptos:

```java
public class Metodos {
    public static void main(String[] args) {
        int resultado = sumar(5, 3);  // Llamada al método sumar
        System.out.println("Resultado: " + resultado);  // Resultado: 8
        
        String saludo = obtenerSaludo("Juan");  // Llamada al método obtenerSaludo
        System.out.println(saludo);  // Hola, Juan!
    }
    
    // Método para sumar dos números enteros y devolver el resultado
    public static int sumar(int a, int b) {
        int suma = a + b;
        return suma;
    }
    
    // Método para obtener un saludo personalizado
    public static String obtenerSaludo(String nombre) {
        String saludo = "Hola, " + nombre + "!";
        return saludo;
    }
}
```

En este ejemplo, se declaran dos métodos: `sumar` y `obtenerSaludo`. El método `sumar` recibe dos argumentos de tipo entero, realiza la suma y devuelve el resultado. El método `obtenerSaludo` recibe un argumento de tipo `String`, concatena el nombre con un saludo y devuelve el resultado como una cadena.

# Uso de `this`

En Java, la palabra clave `this` se utiliza para referirse al objeto actual dentro de una clase. Proporciona una forma de diferenciar entre las variables de instancia de la clase y los parámetros o variables locales con el mismo nombre.

Aquí hay algunos casos comunes en los que se utiliza `this`:

1. Referencia a variables de instancia: `this` se utiliza para hacer referencia a las variables de instancia de la clase. Esto es útil cuando hay una ambigüedad de nombres entre las variables locales y las variables de instancia.

```java
public class Persona {
    private String nombre;

    public void setNombre(String nombre) {
        this.nombre = nombre;  // Utilizando "this" para referirse a la variable de instancia
    }
}
```

En este ejemplo, `this.nombre` se utiliza para referirse a la variable de instancia `nombre`, mientras que `nombre` sin el `this` se refiere al parámetro del método `setNombre`.

2. Invocación de constructores: `this` se puede utilizar para invocar otros constructores de la misma clase dentro de un constructor. Esto se conoce como llamada al constructor de la clase actual.

```java
public class Persona {
    private String nombre;
    private int edad;

    public Persona() {
        this("", 0);  // Llamada al constructor de la clase con argumentos por defecto
    }

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```

En este ejemplo, el constructor sin argumentos invoca al constructor de la clase con los argumentos por defecto utilizando `this("", 0)`.

3. Retorno del objeto actual: `this` se puede utilizar para devolver el objeto actual desde un método, lo que permite encadenar llamadas a métodos en el objeto.

```java
public class Persona {
    private String nombre;
    private int edad;

    public Persona withNombre(String nombre) {
        this.nombre = nombre;
        return this;  // Retorno del objeto actual
    }

    public Persona withEdad(int edad) {
        this.edad = edad;
        return this;  // Retorno del objeto actual
    }
}
```

En este ejemplo, los métodos `withNombre` y `withEdad` modifican los atributos correspondientes del objeto y devuelven el objeto actual utilizando `return this`, lo que permite encadenar llamadas de métodos.

En resumen, `this` se utiliza en Java para hacer referencia al objeto actual dentro de una clase. Puede ser útil para acceder a las variables de instancia, invocar constructores de la clase o devolver el objeto actual desde un método.

## Preguntas

- ==¿Que aprendimos sobre métodos?==
	1. Es posible que un método no tenga parámetros. Un método puede tener ninguno, uno o más parámetros.
	2. Un método define el comportamiento o la forma de hacer algo. Este es el objetivo de los métodos, definir lo que un objeto sabe hacer. El comportamiento se implementa dentro del método.
	3. Por convención, el nombre del método en el mundo Java debe comenzar con una letra minúscula Los ejemplos de nombres de métodos son: `transferir` `transferirPara` `transferisParaOtroTitular`. Tenga en cuenta que todos los nombres comienzan con una letra minúscula y luego usan "CamelCase".

- ==¿Cuál es la sintaxis y el orden correctos para llamar a un método con Java?==
	nombreDeReferencia.nombreDelMetodo();

+ ==De las siguientes declaraciones, seleccione las dos correctas:==
	+ El `this` es una palabra clave. El `this` es una palabra clave igual al `void`, `class`, `new`, `int` y varias otras. El IDE Eclipce muestra todas las palabras claves en un color diferente, el color "púrpura".
	+ El `this` es una referencia. El `this` esta es una referencia, es decir, "apunta" a un objeto.