---
banner: "![[apollo-director-phillips-monitors-apollo-11-pre-launch-activities_4858567220_o.jpg]]"
banner_y: 0.652
banner_icon: 🔻
---

# Tratamiento de excepciones

### StackTrace

Un stack trace es una lista de las funciones que se estaban ejecutando cuando ocurrió una excepción. El stack trace se puede utilizar para identificar la función en la que ocurrió la excepción y el número de línea en el que ocurrió la excepción.

El stack trace se almacena en la [[Pila de ejecucion]]. La pila de ejecución es una estructura de datos que se utiliza para almacenar información sobre las llamadas a funciones en un programa en ejecución.

El stack trace se utiliza para mantener el estado de las funciones en ejecución. Esto incluye la dirección de la función, los parámetros de la función y los valores de retorno de la función.

El stack trace también se utiliza para implementar el control de flujo de un programa. Cuando una función llama a otra función, la dirección de la función actual se almacena en la pila y la dirección de la función llamada se carga en la pila. Cuando la función llamada finaliza, su dirección se elimina de la pila y la dirección de la función actual se carga en la pila. Esto permite que el programa se ejecute en orden secuencial, incluso cuando se llaman funciones.

El stack trace es una parte importante de cualquier programa en ejecución. Permite que los programas llamen a funciones y manejen el estado de las funciones en ejecución.

Aquí hay un ejemplo de un stack trace:
```
Exception in thread "main" java.lang.NullPointerException
    at com.example.App.main(App.java:10)
```

En este ejemplo, la excepción es una **`NullPointerException`**. La excepción ocurrió en la función main() en la línea 10 del archivo App.java.

El stack trace se puede utilizar para identificar la función en la que ocurrió la excepción y el número de línea en el que ocurrió la excepción. Esta información puede ser útil para los desarrolladores para depurar el programa y encontrar el origen de la excepción.


## Uso de excepciones 

Las excepciones en Java son un mecanismo que permite a los programadores tratar situaciones anormales que pueden ocurrir durante la ejecución de un programa. Cuando ocurre una excepción, el programa se detiene y se envía un mensaje de error al usuario. El programador puede entonces utilizar un bloque **`try-catch`** para tratar la excepción y continuar la ejecución del programa.

El bloque **`try-catch`** es una estructura de control que se utiliza para tratar excepciones. El bloque try se utiliza para encerrar el código que puede generar una excepción, y el bloque catch se utiliza para tratar la excepción.

El siguiente es un ejemplo de un bloque try/catch:
```java
try {
  // Este código puede generar una excepción.
} catch (Exception e) {
  // Este bloque se ejecutará si ocurre una excepción.
  System.out.println("Ocurrió una excepción: " + e.getMessage());
}
```

En este ejemplo, el bloque try encierra el código que puede generar una excepción. El bloque catch se utiliza para tratar la excepción. Si ocurre una excepción, el bloque catch se ejecutará y se imprimirá un mensaje de error al usuario.

Es posible también utilizar un bloque **`finally`** para ejecutar código después de que el bloque try o el bloque catch se haya ejecutado. El bloque **`finally`** se ejecutará incluso si ocurre una excepción.

El siguiente es un ejemplo de un bloque **`finally`**:
```java
try {
  // Este código puede generar una excepción.
} catch (Exception e) {
  // Este bloque se ejecutará si ocurre una excepción.
  System.out.println("Ocurrió una excepción: " + e.getMessage());
} finally {
  // Este bloque se ejecutará independientemente de si ocurre una excepción.
  System.out.println("El bloque finally se ejecutó.");
}
```

En este ejemplo, el bloque **`finally`** se ejecutará independientemente de si ocurre una excepción. El bloque **`finally`** se utiliza para realizar operaciones de limpieza, como cerrar recursos.

Las excepciones son una herramienta poderosa que se puede utilizar para tratar situaciones anormales que pueden ocurrir durante la ejecución de un programa. Al utilizar bloques **`try-catch`**, los programadores pueden evitar que los programas se detengan cuando ocurren excepciones y pueden continuar la ejecución del programa.


#### Finally

El bloque **`finally`** es un bloque de código que se ejecuta después de un bloque **`try`** o un bloque **`catch`**. El bloque **`finally`** se ejecuta incluso si ocurre una excepción.

El bloque **`finally`** se utiliza para realizar operaciones de limpieza, como cerrar recursos. Por ejemplo, si abres un archivo en un bloque **`try`**, debes cerrar el archivo en un bloque **`finally`**. Esto se debe a que si ocurre una excepción, el archivo no se cerrará automáticamente.

El bloque **`finally`** se utiliza también para asegurar que se ejecute un código determinado, independientemente de si ocurre una excepción o no. Por ejemplo, si necesitas imprimir un mensaje al usuario, puedes hacerlo en un bloque **`finally`**. Esto se asegurará de que el mensaje se imprima, incluso si ocurre una excepción.

La sintaxis para un bloque **`finally`** es la siguiente:
```java
try {
  // Este código puede generar una excepción.
} catch (Exception e) {
  // Este bloque se ejecutará si ocurre una excepción.
} finally {
  // Este bloque se ejecutará independientemente de si ocurre una excepción.
}
```

Como se menciono, también es posible utilizar un **`finally`** sin la necesidad de un **`catch`**: 
```java
try {
  // Este código puede generar una excepción.
} finally {
  // Este bloque se ejecutará independientemente de si ocurre una excepción.
}
```

En este ejemplo, el bloque **`finally`** se ejecutará independientemente de si ocurre una excepción. El bloque **`finally`** se utiliza para cerrar el archivo.
El bloque **`finally`** es una herramienta poderosa que se puede utilizar para realizar operaciones de limpieza y asegurar que se ejecute un código determinado, independientemente de si ocurre una excepción o no.


### Multi-catch

En Java, puedes atrapar múltiples excepciones utilizando un bloque **`catch`** múltiple. El bloque **`catch`** múltiple se utiliza para atrapar varias excepciones diferentes en el mismo bloque.

La sintaxis para un bloque **`catch`** múltiple es la siguiente:
```java
try {
  // Este código puede generar una excepción.
} catch (Exception1 e1) {
  // Este bloque se ejecutará si ocurre una excepción de tipo Exception1.
} catch (Exception2 e2) {
  // Este bloque se ejecutará si ocurre una excepción de tipo Exception2.
}
```

En este ejemplo, el bloque `catch` múltiple atrapará tanto las excepciones de tipo `Exception1` como las excepciones de tipo `Exception2`. Si ocurre una excepción de un tipo diferente, el bloque `catch` múltiple no la atrapará y el programa se interrumpirá.

También se pude utilizar un bloque catch que puede capturar múltiples excepciones. Esto se hace utilizando el operador **`|`** (or) entre los tipos de excepción.

Por ejemplo, el siguiente código captura tanto la excepción ArithmeticException como la excepción NullPointerException:

```java
try {
  // Este código puede generar una excepción ArithmeticException o NullPointerException.
} catch (ArithmeticException | NullPointerException e) {
  // Este bloque se ejecutará si ocurre una excepción ArithmeticException o NullPointerException.
  System.out.println("Ocurrió una excepción: " + e.getMessage());
}
```

Los bloques catch múltiples se pueden utilizar para simplificar el código y hacer que sea más fácil de leer. También se pueden utilizar para tratar múltiples excepciones en el mismo bloque.

Los multi-catches se pueden utilizar para capturar cualquier número de tipos de excepciones. Sin embargo, ==es importante recordar que las excepciones capturadas deben estar relacionadas entre sí. Por ejemplo, no sería correcto capturar una excepción `ArithmeticException` y una excepción `IOException` en el mismo multi-catch, ya que estas excepciones no están relacionadas.==

Los multi-catches pueden ser una herramienta útil para simplificar el código y evitar la necesidad de escribir múltiples declaraciones catch separadas. Sin embargo, es importante utilizarlos con cuidado para evitar errores.


## Lanzando excepciones

En Java, puedes lanzar excepciones para indicar que ha ocurrido un problema o error en la ejecución del programa. Cuando se produce una excepción, el flujo normal del programa se interrumpe y se busca un bloque de código que maneje la excepción (llamado bloque "catch") para tratarla apropiadamente.

Para lanzar una excepción, debes seguir estos pasos:

1. Elige el tipo de excepción: En Java, existen varias clases de excepción predefinidas, como **`NullPointerException`**, **`IllegalArgumentException`**, **`ArithmeticException`**, entre otras. Debes elegir la clase de excepción que mejor describa el error que ocurrió.

2. Lanza la excepción: Utiliza la palabra clave **`throw`** seguida de una instancia de la clase de excepción que deseas lanzar.

Veamos un ejemplo de cómo lanzar una excepción:

```java
public class EjemploExcepcion {

    public static void dividir(int numerador, int denominador) {
        if (denominador == 0) {
            throw new ArithmeticException("No se puede dividir por cero");
        }

        int resultado = numerador / denominador;
        System.out.println("El resultado de la división es: " + resultado);
    }

    public static void main(String[] args) {
        int a = 10;
        int b = 0;

        try {
            dividir(a, b);
        } catch (ArithmeticException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

En este ejemplo, el método **`dividir()`** recibe dos parámetros, **`numerador`** y **`denominador`**, y realiza una división. Antes de realizar la división, se verifica si el denominador es igual a cero. Si es así, se lanza una excepción de tipo **`ArithmeticException`** utilizando **`throw`**. El mensaje "No se puede dividir por cero" se pasa como argumento al constructor de la excepción.
En el método **`main()`**, se llama al método **`dividir()`** dentro de un bloque **`try-catch`**. Si se produce una excepción dentro del método **`dividir()`**, el flujo del programa se desvía al bloque **`catch`**, donde se imprime el mensaje de error.

Es importante lanzar excepciones cuando ocurran situaciones excepcionales o errores en el programa para proporcionar información útil sobre el problema y permitir que el código sea más robusto y confiable. También es importante manejar las excepciones adecuadamente utilizando bloques **`try-catch`** para que el programa no se detenga abruptamente debido a errores inesperados.


### Errores vs excepciones

En Java, ==un error es una condición que indica que el programa no puede continuar ejecutándose.== Un error puede ser causado por un problema con el programa en sí, o por un problema con el entorno en el que se ejecuta el programa.

==Una excepción es una condición que ocurre durante la ejecución de un programa y que puede interrumpir el flujo normal de ejecución.== Una excepción puede ser causada por una variedad de factores, como un error en el código, un valor de entrada no válido, o una condición de tiempo de ejecución.

La diferencia clave entre un error y una excepción es que _un error no se puede tratar, mientras que una excepción se puede tratar._ Cuando ocurre un error, el programa se interrumpirá y se mostrará un mensaje de error al usuario. Cuando ocurre una excepción, el programador puede utilizar un bloque **`try-catch`** para tratar la excepción y continuar la ejecución del programa.

Aquí hay un ejemplo de un error:
```java
int x = 1 / 0;
```

En este ejemplo, el programa intentará dividir 1 por 0. Esto no es imposible, y el programa se interrumpirá con el siguiente mensaje de error:
```
java.lang.ArithmeticException: / by zero
```

Aquí hay un ejemplo de una excepción:
```java
try {
  int x = Integer.parseInt(null);
} catch (NumberFormatException e) {
  System.out.println("El valor no es un número válido.");
}
```

En este ejemplo, el programa intentará convertir la cadena `null` en un número entero. Esto no es imposible, y el programa lanzará una excepción **`NumberFormatException`**. El bloque **`catch`** atrapará la excepción y mostrará el siguiente mensaje al usuario:
```
El valor no es un número válido.
```

Las excepciones son una herramienta poderosa que se puede utilizar para tratar situaciones anormales que pueden ocurrir durante la ejecución de un programa. Al utilizar bloques **`try-catch`** , los programadores pueden evitar que los programas se detengan cuando ocurren excepciones y pueden continuar la ejecución del programa.

![[clase_Throwable.png | 500]]

## Excepciones personalizadas

Para crear tus propias excepciones personalizadas en Java, debes seguir los siguientes pasos:

1. Crear una clase que extienda **`Exception`** (o alguna de sus subclases).
2. Definir constructores para la excepción que proporcionen mensajes descriptivos sobre el error o información adicional.
3. Opcionalmente, puedes agregar métodos o campos adicionales a la clase para proporcionar más información sobre el error.
4. Puedes lanzar tu excepción personalizada en cualquier lugar del código donde ocurra una situación excepcional.

Veamos un ejemplo de cómo crear una excepción personalizada llamada **`MiExcepcionPersonalizada`**:
```java
public class MiExcepcionPersonalizada extends Exception {

    public MiExcepcionPersonalizada() {
        super();
    }

    public MiExcepcionPersonalizada(String mensaje) {
        super(mensaje);
    }

    public MiExcepcionPersonalizada(String mensaje, Throwable causa) {
        super(mensaje, causa);
    }
}
```

En este ejemplo, hemos creado una clase **`MiExcepcionPersonalizada`** que extiende **`Exception`**. La clase tiene tres constructores que invocan a los constructores de la clase base (**`Exception`**) utilizando la palabra clave **`super`**. Esto permite proporcionar mensajes descriptivos o la causa de la excepción.

Ahora, podemos usar nuestra excepción personalizada en cualquier lugar donde sea necesario. Por ejemplo:

```java
public class EjemploExcepcionPersonalizada {

    public static void miMetodo() throws MiExcepcionPersonalizada {
        // Simulación de una situación excepcional
        throw new MiExcepcionPersonalizada("Ocurrió una excepción personalizada");
    }

    public static void main(String[] args) {
        try {
            miMetodo();
        } catch (MiExcepcionPersonalizada e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

En este ejemplo, el método **`miMetodo()`** lanza nuestra excepción personalizada mediante la instrucción **`throw new MiExcepcionPersonalizada("Ocurrió una excepción personalizada")`**. Luego, en el método **`main()`**, capturamos la excepción con un bloque **`try-catch`** y mostramos el mensaje de error.

Recuerda que cuando creas tus propias excepciones personalizadas, es importante proporcionar mensajes descriptivos y precisos para ayudar a los desarrolladores a entender el error cuando se produzca la excepción.
Crear excepciones personalizadas es útil para representar situaciones excepcionales específicas en tu programa y permite un manejo más preciso y detallado de los errores. Además, facilita la legibilidad del código, ya que los mensajes de error serán más significativos y claros para los desarrolladores que utilizan tu código.


### Checked y unchecked

En Java, existen dos tipos de excepciones: las que extienden de la clase **`Exception`** y las que extienden de la clase **`RuntimeException`**. La principal diferencia entre estas dos clases radica en cómo se manejan durante el tiempo de compilación y el tiempo de ejecución:

1. Excepciones que extienden de **`Exception`**:
   - Estas son conocidas como "excepciones comprobadas" o "checked exceptions" en inglés.
   - Las excepciones que extienden directamente de **`Exception`**, o alguna de sus subclases, deben ser declaradas en la firma del método utilizando la palabra clave **`throws`** o capturadas dentro de un bloque **`try-catch`**.
   - Esto significa que el compilador te obliga a manejar explícitamente estas excepciones en tiempo de compilación, lo que garantiza que el código maneje los posibles errores de manera adecuada.
   - Ejemplos de excepciones comprobadas incluyen **`IOException`**, **`SQLException`**, **`FileNotFoundException`**, entre otras.

2. Excepciones que extienden de **`RuntimeException`**:
   - Estas son conocidas como "excepciones no comprobadas" o "unchecked exceptions" en inglés.
   - Las excepciones que extienden directamente de **`RuntimeException`**, o alguna de sus subclases, no están obligadas a ser declaradas en la firma del método ni capturadas en un bloque **`try-catch`**.
   - Esto significa que el compilador no te fuerza a manejar estas excepciones en tiempo de compilación.
   - Las excepciones no comprobadas se utilizan generalmente para representar errores que son causados por errores de programación o situaciones inesperadas que no se pueden recuperar fácilmente.
   - Ejemplos de excepciones no comprobadas incluyen **`NullPointerException`**, **`ArrayIndexOutOfBoundsException`**, **`ArithmeticException`**, entre otras.

Ejemplo de cómo crear una excepción personalizada que extienda de **`RuntimeException`**:
```java
public class MiExcepcionNoComprobada extends RuntimeException {

    public MiExcepcionNoComprobada() {
        super();
    }

    public MiExcepcionNoComprobada(String mensaje) {
        super(mensaje);
    }

    public MiExcepcionNoComprobada(String mensaje, Throwable causa) {
        super(mensaje, causa);
    }
}
```

En este ejemplo, hemos creado una clase **`MiExcepcionNoComprobada`** que extiende de **`RuntimeException`.** Al heredar de **`RuntimeException`**, esta excepción se considera como una excepción no comprobada, lo que significa que no está obligada a ser capturada o declarada en la firma del método.

Ahora, podemos usar nuestra excepción personalizada en cualquier lugar donde sea necesario, y no es necesario manejarla explícitamente en tiempo de compilación. Por ejemplo:
```java
public class EjemploExcepcionNoComprobada {

    public static void metodoConExcepcion() {
        throw new MiExcepcionNoComprobada("Ocurrió una excepción no comprobada");
    }

    public static void main(String[] args) {
        try {
            metodoConExcepcion();
        } catch (MiExcepcionNoComprobada e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

En este ejemplo, el método **`metodoConExcepcion()`** lanza nuestra excepción personalizada utilizando la instrucción **`throw new MiExcepcionNoComprobada("Ocurrió una excepción no comprobada")`**. Dado que esta excepción extiende de `RuntimeException`, no es necesario capturarla o declararla en la firma del método.
Recuerda que aunque las excepciones no comprobadas no estén obligadas a ser capturadas o declaradas en la firma del método, aún es importante manejarlas adecuadamente. Las excepciones no comprobadas generalmente se utilizan para representar errores causados por errores de programación o situaciones inesperadas que no se pueden recuperar fácilmente. Al lanzar excepciones no comprobadas, asegúrate de proporcionar mensajes descriptivos y útiles para facilitar la depuración y el entendimiento del problema.

En resumen, la diferencia principal entre extender de **`RuntimeException`** y **`Exception`** radica en cómo el compilador trata estas excepciones. Las excepciones que extienden de **`Exception`** son consideradas como excepciones comprobadas y ==deben ser manejadas en tiempo de compilación==, mientras que las excepciones que extienden de **`RuntimeException`** son consideradas como excepciones no comprobadas y ==no están obligadas a ser manejadas en tiempo de compilación.==


---

+ #excepciones
+ #excepciones_personalizadas
+ #StackTrace