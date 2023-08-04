---
banner_icon: 🚦
banner: "![[premiere-apollo-11-first-steps-edition_47804504192_o.jpg]]"
banner_y: 0.488
---

# Try with resources

El bloque _try with resources_ es una estructura de control que se introdujo en Java 7. El bloque _try with resources_ se utiliza para asegurar que los recursos se cierren correctamente, incluso si ocurre una excepción.

El bloque _try with resources_ se utiliza para tratar con recursos que implementan la interfaz **`AutoCloseable`**. La interfaz **`AutoCloseable`** tiene un método **`close()`** que se utiliza para cerrar el recurso.

La sintaxis para un bloque _try with resources_ es la siguiente:
```java
try (
  // Declara los recursos que se van a utilizar.
  Recurso1 r1 = new Recurso1();
  Recurso2 r2 = new Recurso2();
) {
  // Este código utiliza los recursos.
} catch (Exception e) {
  // Este bloque se ejecutará si ocurre una excepción.
}
```

En este ejemplo, el bloque _try with resources_ asegurará que los recursos **`r1`** y **`r2`** se cierren correctamente, incluso si ocurre una excepción.

El bloque _try with resources_ es una herramienta poderosa que se puede utilizar para asegurar que los recursos se cierren correctamente, incluso si ocurre una excepción.

Aquí hay un ejemplo de cómo utilizar el bloque _try with resources_ para abrir y cerrar un archivo:
```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class EjemploTryWithResources {

    public static void leerArchivo(String nombreArchivo) {
        try (BufferedReader br = new BufferedReader(new FileReader(nombreArchivo))) {
            String linea;
            while ((linea = br.readLine()) != null) {
                System.out.println(linea);
            }
        } catch (IOException e) {
            System.out.println("Error al leer el archivo: " + e.getMessage());
        }
    }

    public static void main(String[] args) {
        leerArchivo("mi_archivo.txt");
    }
}
```

En este ejemplo, el método **`leerArchivo()`** utiliza _try with resources_ para leer líneas de un archivo. El recurso **`BufferedReader`** se declara e inicializa dentro del bloque **`try`**. Una vez que el bloque **`try`** finaliza, ya sea por el final del archivo o por una excepción, el recurso **`BufferedReader`** se cierra automáticamente, evitando fugas de recursos y asegurando que se libere adecuadamente.

_Try with resources_ es una práctica recomendada para trabajar con recursos que necesitan ser cerrados explícitamente, y simplifica el manejo de excepciones y el código necesario para asegurarse de que los recursos se cierren correctamente.


---

+ #excepciones
+ #excepciones_personalizadas