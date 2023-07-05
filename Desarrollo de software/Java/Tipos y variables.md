---
banner_icon: 🛗
banner: "![[charles-duke_29881269755_o.jpg]]"
banner_y: 0.244
---

# Tipos de datos

En Java, hay varios tipos de variables que puedes utilizar para almacenar diferentes tipos de datos. Aquí están los tipos de variables más comunes:

1. **Variables numéricas**: Estas variables se utilizan para almacenar valores numéricos. Hay varios tipos numéricos en Java, que incluyen:

   - `byte`: Almacena números enteros en el rango de -128 a 127.
   - `short`: Almacena números enteros en el rango de -32,768 a 32,767.
   - `int`: Almacena números enteros en el rango de -2,147,483,648 a 2,147,483,647.
   - `long`: Almacena números enteros en un rango mucho mayor que `int`, de -9,223,372,036,854,775,808 a 9,223,372,036,854,775,807.
   - `float`: Almacena números de punto flotante con precisión simple.
   - `double`: Almacena números de punto flotante con mayor precisión que `float`.

2. **Variables de caracteres**: Estas variables se utilizan para almacenar caracteres individuales. El tipo de variable para caracteres es `char`, y se puede asignar un solo carácter entre comillas simples, como `'A'` o `'x'`.

3. **Variables booleanas**: Estas variables se utilizan para representar valores lógicos verdadero/falso. El tipo de variable para booleanos es `boolean`, y puede tener dos posibles valores: `true` o `false`.

4. **Variables de texto**: Estas variables se utilizan para almacenar cadenas de texto. El tipo de variable para cadenas es `String`, que es una clase en Java. Las cadenas se definen entre comillas dobles, como `"Hola"` o `"Java"`.

Además de estos tipos básicos, Java también permite definir y utilizar tipos de variables más complejos, como arreglos (arrays), objetos personalizados y tipos de datos enumerados.

Es importante tener en cuenta que en Java, ==las variables deben declararse antes de usarlas==. Esto implica especificar el tipo de variable y el nombre que le asignas. Por ejemplo, para declarar una variable entera llamada `edad`, puedes escribir `int edad;`. Luego, puedes asignarle un valor utilizando el operador de asignación, como `edad = 25;`.

![[tipos_datos.png| 700]]

###### **Nota:**
Cómo declarar los tipos de datos mencionados anteriormente en Java:

1. **Variables numéricas**:
   - `byte`: Se declara utilizando la palabra clave `byte`, seguida del nombre de la variable. Por ejemplo: `byte edad = 30;`
   - `short`: Se declara utilizando la palabra clave `short`. Por ejemplo: `short temperatura = -10;`
   - `int`: Se declara utilizando la palabra clave `int`. Por ejemplo: `int cantidad = 1000;`
   - `long`: Se declara utilizando la palabra clave `long` y se le añade la letra "L" al final del valor para indicar que es un `long`. Por ejemplo: `long poblacion = 10000000000L;`
   - `float`: Se declara utilizando la palabra clave `float` y se le añade la letra "f" al final del valor para indicar que es un `float`. Por ejemplo: `float precio = 10.99f;`
   - `double`: Se declara utilizando la palabra clave `double`. Por ejemplo: `double pi = 3.14159;`

2. **Variables de caracteres**:
   - `char`: Se declara utilizando la palabra clave `char` y se asigna un valor entre comillas simples. Por ejemplo: `char letra = 'A';`

3. **Variables booleanas**:
   - `boolean`: Se declara utilizando la palabra clave `boolean` y se asigna `true` o `false`. Por ejemplo: `boolean esVerdadero = true;`

4. **Variables de texto**:
   - `String`: Se declara utilizando la clase `String`. Por ejemplo: `String nombre = "Juan";`

Recuerda que al declarar una variable, debes especificar el tipo de dato, seguido del nombre de la variable que elijas. También puedes inicializar la variable con un valor en el momento de la declaración, utilizando el operador de asignación `=`.

Es importante destacar que los nombres de las variables deben seguir las convenciones de nomenclatura de Java, como comenzar con una letra minúscula y utilizar ==camelCase==.

# Operaciones

#### <mark class="hltr-pink">Operaciones numéricas</mark>:
- Para los tipos numéricos (`byte`, `short`, `int`, `long`, `float` y `double`), se pueden realizar operaciones aritméticas básicas como suma (`+`), resta (`-`), multiplicación (`*`), división (`/`) y módulo (`%`). También se pueden utilizar los operadores de incremento (`++`) y decremento (`--`) para aumentar o disminuir el valor de una variable en una unidad.

#### <mark class="hltr-pink">Operaciones de caracteres</mark>:
- El tipo `char` permite operaciones como la concatenación, donde puedes unir dos caracteres utilizando el operador de suma (`+`), por ejemplo: `'H' + 'i'` resultaría en `'Hi'`. Además, se pueden comparar caracteres utilizando operadores de comparación, como `==`, `!=`, `<`, `>`, `<=` y `>=`.

#### <mark class="hltr-pink">Operaciones booleanas</mark>**:
- Las variables de tipo `boolean` permiten realizar operaciones lógicas, como la negación (`!`), la conjunción lógica (`&&`) y la disyunción lógica (`||`). Estas operaciones se utilizan para evaluar y combinar expresiones booleanas.

#### <mark class="hltr-pink">Operaciones de texto</mark>:
- Las cadenas (`String`) admiten la concatenación mediante el operador de suma (`+`). Por ejemplo, `"Hola" + " Mundo"` resultaría en `"Hola Mundo"`. También se pueden comparar cadenas utilizando los operadores de comparación, como `==`, `!=`, `<`, `>`, `<=` y `>=`.

Es importante tener en cuenta que las operaciones pueden variar según el tipo de datos. Por ejemplo, la división entre dos números enteros (`int`) produce un resultado entero truncado, mientras que la división entre dos números de punto flotante (`float` o `double`) produce un resultado con decimales.

Además de estas operaciones básicas, Java también proporciona operadores adicionales para realizar operaciones más complejas, como operaciones de bits, desplazamiento de bits, comparaciones detalladas, entre otros. Puedes explorar la documentación oficial de Java para obtener más información sobre todas las operaciones y operadores disponibles para cada tipo de dato, esta información esta disponible en este [link](https://docs.oracle.com/cd/E19253-01/819-6957/6n8uft4b8/index.html)

# Conversiones

En Java, es posible realizar conversiones entre diferentes tipos de datos. A continuación, estas son las conversiones más comunes:

1. **Casting implícito**: Se produce cuando se asigna un valor de un tipo de dato más pequeño a un tipo de dato más grande. Java realiza esta conversión automáticamente sin requerir una sintaxis especial. Por ejemplo:

   ```java
   int num1 = 10;
   double num2 = num1;  // Casting implícito de int a double
   ```

   En este caso, el valor entero `num1` se convierte implícitamente en un valor de tipo `double` y se asigna a la variable `num2`.

2. **Casting explícito**: También conocido como "==casting==", se utiliza cuando deseas convertir un valor de un tipo de dato más grande a un tipo de dato más pequeño. Esto requiere una sintaxis especial y puede resultar en una pérdida de precisión o truncamiento de datos si el valor no es compatible con el tipo de destino. Por ejemplo:

   ```java
   double num1 = 3.14;
   int num2 = (int) num1;  // Casting explícito de double a int
   ```

   En este caso, se utiliza el casting explícito para convertir el valor de tipo `double` en un valor de tipo `int`. Ten en cuenta que la parte decimal se truncará y se perderá.

3. **Métodos de conversión**: Java proporciona métodos específicos para convertir valores entre diferentes tipos de datos. Algunos de estos métodos son:

   - `Integer.parseInt()`: Convierte una cadena de caracteres en un valor entero (`int`).
   - `Double.parseDouble()`: Convierte una cadena de caracteres en un valor de punto flotante (`double`).
   - `String.valueOf()`: Convierte un valor de cualquier tipo en una cadena de caracteres (`String`).

   Por ejemplo:

   ```java
   String str = "123";
   int num = Integer.parseInt(str);  // Convierte la cadena en un entero
   ```

   Aquí, el método `Integer.parseInt()` se utiliza para convertir la cadena `"123"` en un valor entero y asignarlo a la variable `num`.

Es importante tener en cuenta que algunas conversiones pueden provocar errores si los tipos de datos no son compatibles o si ocurre una pérdida de precisión. Por lo tanto, debes tener cuidado al realizar conversiones y asegurarte de que los datos sean compatibles y de que no se pierda información importante en el proceso.

Funcionamiento del cast implícito y explícito:

|DE/PARA|byte|short|char|int|long|float|double|
|---|---|---|---|---|---|---|---|
|byte|----|_Impl._|(char)|_Impl._|_Impl._|_Impl._|_Impl._|
|short|(byte)|----|(char)|_Impl._|_Impl._|_Impl._|_Impl._|
|char|(byte)|(short)|----|_Impl._|_Impl._|_Impl._|_Impl._|
|int|(byte)|(short)|(char)|----|_Impl._|_Impl._|_Impl._|
|long|(byte)|(short)|(char)|(int)|----|_Impl._|_Impl._|
|float|(byte)|(short)|(char)|(int)|(long)|----|_Impl._|
|double|(byte)|(short)|(char)|(int)|(long)|(float)|----|

# Scope e inicialización

El scope (ámbito) y la inicialización son conceptos importantes relacionados con las variables en Java. 

- **Scope (Ámbito)**: El scope se refiere a la visibilidad o alcance de una variable en un programa. Determina en qué partes del código una variable es accesible y puede ser utilizada. En Java, existen diferentes niveles de scope, incluyendo:

  - **Scope de bloque**: Una variable declarada dentro de un bloque de código, como un método, una estructura condicional (`if`, `while`, `for`), o un bloque de código definido entre llaves `{}`, tiene un scope limitado a ese bloque y sus bloques internos. La variable solo es visible y accesible dentro del bloque en el que se declaró. Ejemplo:

    ```java
    public void ejemploScope() {
        int x = 10; // Variable con scope de bloque

        if (x > 5) {
            int y = 20; // Otra variable con scope de bloque dentro del if
            System.out.println(x + y); // Acceso válido a x y y dentro del if
        }

        System.out.println(x); // Acceso válido a x fuera del if
        // System.out.println(y); // Error: y no es accesible aquí
    }
    ```

  - **Scope de clase**: Una variable declarada en una clase, pero fuera de cualquier método o bloque de código, tiene un scope de clase. Se puede acceder a esa variable desde cualquier parte de la clase. Ejemplo:

    ```java
    public class EjemploScope {
        private int x; // Variable con scope de clase

        public void setX(int valor) {
            x = valor; // Acceso válido a x dentro de un método de la clase
        }

        public void imprimirX() {
            System.out.println(x); // Acceso válido a x desde otro método de la clase
        }
    }
    ```

- **Inicialización de variables**: La inicialización de una variable implica asignarle un valor inicial antes de utilizarla. En Java, las variables locales (variables dentro de un método o bloque de código) no se inicializan automáticamente y deben recibir un valor antes de utilizarse. Las variables de instancia (variables de clase) se inicializan automáticamente con un valor predeterminado si no se les asigna un valor explícitamente. Ejemplo:

  ```java
  public void ejemploInicializacion() {
      int x; // Variable sin inicializar, no se puede usar hasta recibir un valor

      int y = 10; // Variable inicializada con un valor

      System.out.println(y); // Acceso válido a y

      // System.out.println(x); // Error: x no está inicializada
  }
  ```

  En este ejemplo, `y` está inicializada con el valor `10`, por lo que puede ser utilizada sin problemas. Sin embargo, `x` no está inicializada y su uso antes de recibir un valor provocaría un error de compilación.

Es importante entender el scope y asegurarse de que las variables sean declaradas e inicializadas adecuadamente en el lugar correcto para garantizar su correcto uso y evitar errores.