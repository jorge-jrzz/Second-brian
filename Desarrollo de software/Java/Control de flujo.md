---
banner_icon: 🔘
banner: "![[in-the-shadow-of-saturn_17125224860_o.jpg]]"
banner_y: 0.492
---

# Ciclos

En Java, los ciclos (también conocidos como bucles) se utilizan para repetir un bloque de código varias veces. Hay varias estructuras de ciclo disponibles en Java:

1. **Ciclo `for`**: El ciclo `for` se utiliza cuando conocemos la cantidad exacta de veces que queremos repetir un bloque de código. Tiene una estructura definida que incluye una variable de control, una condición y una expresión de actualización. Ejemplo:

   ```java
   for (int i = 0; i < 5; i++) {
       System.out.println(i);
   }
   ```

   En este ejemplo, el ciclo `for` se repetirá 5 veces, imprimiendo los valores de `i` desde 0 hasta 4.

2. **Ciclo `while`**: El ciclo `while` se utiliza cuando queremos repetir un bloque de código mientras se cumpla una condición. La condición se evalúa antes de cada iteración. Ejemplo:

   ```java
   int i = 0;
   while (i < 5) {
       System.out.println(i);
       i++;
   }
   ```

   En este ejemplo, el ciclo `while` imprimirá los valores de `i` desde 0 hasta 4 mientras la condición `i < 5` sea verdadera.

3. **Ciclo `do-while`**: El ciclo `do-while` es similar al ciclo `while`, pero la condición se evalúa después de cada iteración. Esto garantiza que el bloque de código se ejecute al menos una vez, incluso si la condición inicialmente es falsa. Ejemplo:

   ```java
   int i = 0;
   do {
       System.out.println(i);
       i++;
   } while (i < 5);
   ```

   En este ejemplo, el ciclo `do-while` imprimirá los valores de `i` desde 0 hasta 4, al igual que el ciclo `while`.

Estas estructuras de ciclo permiten controlar el flujo de ejecución de un programa y repetir un bloque de código de manera eficiente. Es importante tener cuidado al utilizar ciclos para evitar ciclos infinitos y asegurarse de que las condiciones se actualicen correctamente para evitar bucles infinitos.

Además de estos ciclos principales, Java también proporciona las palabras clave `break` y `continue` para controlar el flujo dentro de los ciclos. `break` se utiliza para salir de un ciclo prematuramente, mientras que `continue` se utiliza para omitir la ejecución restante de una iteración y pasar a la siguiente iteración del ciclo. Estas palabras clave brindan mayor flexibilidad en el control de ciclos según las necesidades del programa.

## Bucles anidados

1. **Bucle `for` anidado**:
```java
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
        System.out.println("Valor de i: " + i + ", Valor de j: " + j);
    }
}
```
En este ejemplo, hay un bucle `for` anidado dentro de otro bucle `for`. Imprimirá la combinación de valores de `i` y `j` para cada iteración de ambos bucles, generando la siguiente salida:
```bash
Valor de i: 1, Valor de j: 1
Valor de i: 1, Valor de j: 2
Valor de i: 1, Valor de j: 3
Valor de i: 2, Valor de j: 1
Valor de i: 2, Valor de j: 2
Valor de i: 2, Valor de j: 3
Valor de i: 3, Valor de j: 1
Valor de i: 3, Valor de j: 2
Valor de i: 3, Valor de j: 3
```

2. **Bucle `while` anidado**:
```java
int i = 1;
while (i <= 3) {
    int j = 1;
    while (j <= 3) {
        System.out.println("Valor de i: " + i + ", Valor de j: " + j);
        j++;
    }
    i++;
}
```
En este ejemplo, se utilizan dos bucles `while` anidados. Imprimirá la combinación de valores de `i` y `j` para cada iteración de ambos bucles, generando la misma salida que el ejemplo anterior.

Los bucles anidados son útiles cuando se necesitan ejecutar iteraciones en múltiples dimensiones o realizar tareas repetitivas más complejas. Es importante tener en cuenta el diseño y la lógica del programa al utilizar bucles anidados para evitar un código confuso o ineficiente.

## Preguntas
- ==Afirmaciones con respecto al while==
	1. En la expresión condicional `while` es posible usar cualquier operador de comparación: `<` (menor), `>` (mayor), `<=` (menor o igual), `>=` (mayor o igual), `==` (igual a) y `!=` (diferente de)) y cualquier operador lógico (`&&` (and), `||` (or)). Todos los operadores lógicos y de comparación son válidos en la expresión condicional `while`. ¡Úsalos sabiamente!
	2. El while siempre necesitará una expresión condicional que definirá cuándo se debe romper el ciclo. Recuerda, esta expresión condicional deberá ingresarse entre los paréntesis del `while` y podrás usar cualquiera de los operadores de comparación y operadores lógicos aprendidos en el capítulo 6.

- Clarice tiene dudas sobre cómo funciona el `break` cuando se usa dentro de bucles anidados. ==Describe exactamente cómo funciona este comando en estas situaciones.==
	Para la ejecución del bucle más interno que contiene el comando `break` y continúa ejecutando los bucles más externos. El `descanso` solo interrumpirá el ciclo de repetición más interno que lo contiene.
---
**Ejercicio sobre el control de flujo en: [[Ejercicios 1]]**