---
banner_icon: 🔪
banner: "![[buzz-aldrin-and-the-us-flag-on-the-moon_9460188482_o.jpg]]"
banner_y: 0.272
---

# Test if

En Java, las estructuras condicionales, como el condicional "if", se utilizan para tomar decisiones en función de ciertas condiciones. El condicional "if" evalúa una expresión booleana y ejecuta un bloque de código si la expresión es verdadera. 

La sintaxis general del condicional "if" en Java es la siguiente:

```java
if (condición) {
    // Bloque de código a ejecutar si la condición es verdadera
}
```

Aquí hay algunos puntos clave a tener en cuenta:

- **Condición**: La condición es una expresión booleana que se evalúa como verdadera o falsa. Puede ser cualquier expresión que produzca un resultado booleano, como una comparación (`==`, `!=`, `<`, `>`, `<=`, `>=`), una expresión lógica (`&&`, `||`), o incluso una llamada a un método que devuelva un valor booleano.

- **Bloque de código**: El bloque de código se ejecuta solo si la condición especificada es verdadera. El bloque de código se define utilizando llaves `{}` y puede contener una o varias sentencias Java. Si la condición es falsa, el bloque de código se omitirá y la ejecución continuará con el siguiente bloque de código después del condicional "if".

- **Estructuras anidadas**: Puedes anidar múltiples condicionales "if" dentro de otros condicionales "if" para realizar evaluaciones más complejas. Esto se conoce como condicionales "if" anidados.

- **Estructuras alternativas**: Además del condicional "if" simple, también se pueden utilizar las estructuras "if-else" y "if-else if-else" para proporcionar alternativas en caso de que la condición no sea verdadera. El bloque de código después de "else" se ejecutará si la condición en el "if" anterior es falsa.

Ejemplo para ilustrar cómo se utiliza el condicional "if" en Java:

```java
int edad = 20;

if (edad >= 18) {
    System.out.println("Eres mayor de edad");
} else {
    System.out.println("Eres menor de edad");
}
```

En este ejemplo, se evalúa la condición `edad >= 18`. Si es verdadera, se imprimirá "Eres mayor de edad". Si es falsa, se imprimirá "Eres menor de edad".

Los condicionales "if" son una herramienta esencial para controlar el flujo de ejecución de un programa en base a condiciones específicas. Puedes utilizarlos para tomar decisiones y ejecutar diferentes bloques de código según el resultado de las evaluaciones condicionales.

# Booleanos

En Java, el tipo de dato `boolean` se utiliza para representar valores de verdad, es decir, valores que pueden ser `true` (verdadero) o `false` (falso). Detalles importantes sobre los booleanos en Java:

- **Valores posibles**: El tipo `boolean` solo tiene dos valores posibles: `true` y `false`. Estos valores se utilizan para expresar el resultado de una condición lógica, donde `true` representa que la condición es verdadera y `false` representa que la condición es falsa.

- **Operaciones lógicas**: Los booleanos se utilizan comúnmente en operaciones lógicas. En Java, existen tres operadores lógicos principales:
  - `&&` (AND lógico): Retorna `true` si ambos operandos son `true`, de lo contrario, retorna `false`.
  - `||` (OR lógico): Retorna `true` si al menos uno de los operandos es `true`, de lo contrario, retorna `false`.
  - `!` (NOT lógico): Invierte el valor de un booleano. Si el operando es `true`, retorna `false`; si el operando es `false`, retorna `true`.

- **Resultados de comparaciones**: Al realizar comparaciones en Java, el resultado de una comparación puede ser un valor booleano. Por ejemplo, al comparar dos valores numéricos utilizando operadores de comparación (`<`, `>`, `<=`, `>=`, `==`, `!=`), el resultado será un valor booleano que indica si la comparación es verdadera o falsa.

- **Condicionales y bucles**: Los booleanos son fundamentales en las estructuras de control como los condicionales (`if`, `else if`, `else`) y los bucles (`while`, `do-while`, `for`). Las expresiones booleanas se evalúan para determinar qué bloque de código se ejecutará o si se repetirá la ejecución de un bucle.

Ejemplo que muestra cómo se utilizan los booleanos en Java:

```java
boolean esMayorDeEdad = true;
boolean tieneLicencia = false;

if (esMayorDeEdad && tieneLicencia) {
    System.out.println("Puede conducir un automóvil.");
} else {
    System.out.println("No puede conducir un automóvil.");
}
```

En este ejemplo, se utilizan dos variables booleanas `esMayorDeEdad` y `tieneLicencia` para evaluar si una persona puede conducir un automóvil. Si ambas variables son `true` (es decir, la persona es mayor de edad y tiene licencia), se imprimirá "Puede conducir un automóvil". De lo contrario, se imprimirá "No puede conducir un automóvil".

Los booleanos son fundamentales para la toma de decisiones y el control de flujo en la programación. Permiten evaluar condiciones lógicas y determinar qué acciones se deben realizar en función de los resultados de esas evaluaciones.

#  Para saber más: el comando switch

Vimos cómo hacer pruebas con **`if`**, pero ¿si necesitamos hacer varias pruebas? Un ejemplo, tenemos una variable **`mes`** que necesitamos probar su número e imprimir su mes correspondiente. Entonces, ¿vamos a hacer 12 **`if`** s?

Una alternativa al if/else es el **`switch`**, de cambio, que es una estructura de control de flujo que permite ejecutar diferentes acciones basadas en el valor de una expresión. Es una forma más simplificada y legible de escribir varios bloques if/else encadenados.

Funciona de la siguiente manera (sintaxe del switch):

```java
switch (variableASerProbada) {
    case opción1:
        comando (s) si se ha elegido la opción 1
        break;
    case option2:
        comando (s) si se ha elegido la opción 2
        break;
    case option3:
        comando (s) si se ha elegido la opción 3
        break;
    default:
        comando (s) si ninguna de las opciones anteriores ha sido elegida
}
```

El código que se ejecutará, que en nuestro caso será la impresión del nombre del mes, será el código donde se cumple la condición:

```java
public class TestMes {

    public static void main (String [] args) {

        int mes = 10;

        switch (mes) {
            case 1:
                System.out.println ("El mes es enero");
                break;
            case 2:
                System.out.println ("El mes es febrero");
                break;
            case 3:
                System.out.println ("El mes es marzo");
                break;
            case 4:
                System.out.println ("El mes es abril");
                break;
            case 5:
                System.out.println ("El mes es mayo");
                break;
            case 6:
                System.out.println ("El mes es junio");
                break;
            case 7:
                System.out.println ("El mes es julio");
                break;
            case 8:
                System.out.println ("El mes es agosto");
                break;
            case 9:
                System.out.println ("El mes es septiembre");
                break;
            case 10:
                System.out.println ("El mes es octubre");
                break;
            case 11:
                System.out.println ("El mes es noviembre");
                break;
            case 12:
                System.out.println ("El mes es diciembre");
                break;
            default:
                System.out.println ("Mes inválido");
                break;
        }
    }
}
```

El **`break`** interrumpirá la ejecución del caso que lo contiene, de modo que los demás no se ejecutarán y, si no se aceptan condiciones, se ejecutará el código **`default`**. Por ejemplo:

```java
public class TestMes {

    public static void main (String[] args) {

        int mes = 13;

        switch (mes) {
            case 1:
                System.out.println ("El mes es enero");
                break;
            case 2:
                System.out.println ("El mes es febrero");
                break;
            case 3:
                System.out.println ("El mes es marzo");
                break;
            case 4:
                System.out.println ("El mes es abril");
                break;
            case 5:
                System.out.println ("El mes es mayo");
                break;
            case 6:
                System.out.println ("El mes es junio");
                break;
            case 7:
                System.out.println ("El mes es julio");
                break;
            case 8:
                System.out.println ("El mes es agosto");
                break;
            case 9:
                System.out.println ("El mes es septiembre");
                break;
            case 10:
                System.out.println ("El mes es octubre");
                break;
            case 11:
                System.out.println ("El mes es noviembre");
                break;
            case 12:
                System.out.println ("El mes es diciembre");
                break;
            default:
                System.out.println ("Mes inválido");
                break;
        }
    }
}
```

La impresión será **Mes** inválido. Entonces, el **`switch`** es una solución para los **`if`s** encadenados.

**Ventajas del switch case:**
En resumen, el switch case hace que el código sea más fácil de entender y más legible en comparación con el if/else, especialmente cuando hay múltiples condiciones posibles.

## Preguntas
+ A continuación, se presentan declaraciones sobre operaciones lógicas en el lenguaje Java. ==¿Cuáles son ciertas?==
	1. El operador lógico AND está representado por los caracteres `&&` y el OR por `||`.
	2. Los operadores lógicos deben tener una expresión booleana en los lados izquierdo y derecho. Por ejemplo:
		```java
		if (edad > 18 && edad < 65) {
		
		}
		```
	    Observa que tenemos dos expresiones booleanas, a la izquierda y a la derecha del operador lógico `&&`.

+ En esta ocasión, Juan realizó una implementación para calcular el salario de un empleado en caso de ascenso. Hizo la siguiente implementación:
	```java
	public class TestSalario {
	
	    public static void main(String[] args) {
	
	        boolean fuePromovido = true;
	
	        if (fuePromovido) {
	            double salario = 4200.0;
	        } else {
	            double salario = 3800.0;
	        }
	
	        System.out.println(salario);
	    }
	}
	```
	==¿Cuál será el resultado de la compilación / ejecución?==
	El código ni siquiera se compila, porque fuera del bloque `if` / `else` la variable `salario` ya no existe. La variable de salario solo es visible dentro del bloque `if` / `else`.
---
**Ejercicio sobre el uso de condicionales en: [[Ejercicios 1]]**
