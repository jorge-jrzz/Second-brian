---
banner_icon: 🎛️
banner: "![[false-color-lunar-image_9460965180_o.jpg]]"
banner_y: 0.416
---

# Control de Flujo 

## Comparadores

Los comparadores son operadores en Python que se utilizan para comparar dos valores y devolver un valor booleano (**`True`** o **`False`**) que indica si la comparación es verdadera o falsa. En Python, los comparadores se usan principalmente para evaluar condiciones en declaraciones **`if`** y **`while`** y otros bucles.
Los comparadores más comunes en Python son:
1. **`==`** : Compara si dos valores son iguales.
2. **`!=`** : Compara si dos valores son diferentes.
3. **`<`** : Compara si un valor es menor que otro.
4. **`>`** : Compara si un valor es mayor que otro.
5. **`<=`** : Compara si un valor es menor o igual a otro.
6. **`>=`** : Compara si un valor es mayor o igual a otro


## Estructuras if, if-else y elif

En Python, las estructuras de control de flujo **`if`**, **`else`** y **`elif`** se utilizan para tomar decisiones en función de una o varias condiciones. Estas estructuras permiten que el programa ejecute diferentes bloques de código según si una condición se cumple o no.
La estructura básica de una declaración **`if`** en Python es la siguiente:
```python
if condicion: 
        # bloque de codigo a ejecutar si la condicion es verdadera
```

Si la condición es verdadera, el bloque de código dentro del **`if`** se ejecutará. Si la condición es falsa, el bloque de código se saltará y se continuará con el resto del programa.

La estructura **`else`** se utiliza para ejecutar un bloque de código alternativo si la condición en el **`if`** es falsa. La estructura básica de una declaración **`if`** con **`else`** es la siguiente:
```python
if condicion: 
        # bloque de codigo a ejecutar si la condicion es verdadera 

else: 
        # bloque de codigo a ejecutar si la condicion es falsa
```

Si la condición es verdadera, se ejecutará el primer bloque de código. Si la condición es falsa, se ejecutará el bloque de código después del **`else`**.

La estructura **`elif`** se utiliza para probar múltiples condiciones en orden. La estructura básica de una declaración **`if`** con múltiples **`elif`** es la siguiente:
```python
if condicion1: 
        # bloque de codigo a ejecutar si la condicion1 es verdadera 
elif condicion2: 
        # bloque de codigo a ejecutar si la condicion2 es verdadera 
elif condicion3: 
        # bloque de codigo a ejecutar si la condicion3 es verdadera 
else: 
        # bloque de codigo a ejecutar si ninguna de las condiciones es verdadera
```

En este ejemplo, se probarán las condiciones en orden. Si la primera condición es verdadera, se ejecutará el primer bloque de código. Si la primera condición es falsa, se probará la siguiente condición y así sucesivamente hasta que se encuentre una condición verdadera o se alcance el **`else`** final.

Es importante tener en cuenta que la **indentación** es muy importante en Python y se utiliza para indicar qué código está dentro de un bloque **`if`**, **`else`** o **`elif`**.


### Operador ternario

El operador ternario es una forma abreviada de escribir una declaración **`if`** en una sola línea. En Python, se utiliza el operador ternario **`if`**-**`else`** para asignar un valor a una variable basado en una condición.
La sintaxis del operador ternario es la siguiente:
```text
valor_si_cierto if condicion else valor_si_falso
```

Donde:
- **`valor_si_cierto`** es el valor que se asignará a la variable si la condición es verdadera.
- **`condicion`** es la condición que se evaluará.
- **`valor_si_falso`** es el valor que se asignará a la variable si la condición es falsa.

Por ejemplo, si queremos asignar a la variable **`x`** el valor de 1 si **`y`** es mayor que 0, y el valor de 0 si **`y`** es menor o igual que 0, podemos usar el operador ternario de la siguiente manera:
```python
x = 1 if y > 0 else 0
```

En este ejemplo, si la condición **`y > 0`** es verdadera, se asignará el valor de 1 a la variable **`x`**. Si la condición es falsa, se asignará el valor de 0.
Es importante tener en cuenta que el operador ternario puede ser útil para escribir código de forma más compacta y legible en algunos casos, pero no siempre es la mejor opción. En algunos casos, puede ser más fácil de entender y mantener el código utilizando una declaración **`if`** más larga y detallada.


## Operadores Lógicos

Los operadores lógicos son símbolos que se utilizan para combinar y comparar valores booleanos (verdadero o falso) en Python. En Python existen tres operadores lógicos principales: **`and`**, **`or`** y **`not`**.
- El operador **`and`** devuelve **`True`** si ambas condiciones son verdaderas. Si al menos una de las condiciones es falsa, el resultado será **`False`**. Por ejemplo:
```python
x = 5 
y = 10 
if x > 0 and y > 0: 
	print("Ambas condiciones son verdaderas")
```

En este ejemplo, la condición **`x > 0 and y > 0`** es verdadera porque ambas variables son mayores que cero, por lo que el mensaje "Ambas condiciones son verdaderas" se imprimirá.

- El operador **`or`** devuelve **`True`** si al menos una de las condiciones es verdadera. Si ambas condiciones son falsas, el resultado será **`False`**. Por ejemplo:
```python
x = -1 
y = 10 
if x > 0 or y > 0: 
	print("Al menos una condición es verdadera")
```

En este ejemplo, la condición **`x > 0 or y > 0`** es verdadera porque **`y`** es mayor que cero, aunque **`x`** sea menor que cero. Por lo tanto, el mensaje "Al menos una condición es verdadera" se imprimirá.

- El operador **`not`** invierte el valor de una expresión booleana. Si la expresión es verdadera, **`not`** devuelve **`False`**. Si la expresión es falsa, **`not`** devuelve **`True`**. Por ejemplo:
```python
x = 5 
if not x < 0: 
	print("x es mayor o igual a cero")
```

En este ejemplo, la expresión **`x < 0`** es falsa porque **`x`** es mayor que cero. Al aplicar el operador **`not`**, la expresión se invierte y se imprime el mensaje "x es mayor o igual a cero".

Es importante tener en cuenta que los operadores lógicos se evalúan de izquierda a derecha y tienen una prioridad. La prioridad de los operadores lógicos es **`not`** (mayor prioridad), **`and`** y **`or`** (menor prioridad). Sin embargo, se pueden utilizar paréntesis para cambiar el orden de evaluación.

#### Corto circuito
Los operadores de cortocircuito (también conocidos como operadores booleanos de circuito corto) son operadores lógicos en Python que se utilizan para evaluar expresiones booleanas de manera más eficiente.
En Python, los operadores de cortocircuito son **`and`** y **`or`**. Cuando se evalúa una expresión booleana que contiene uno de estos operadores, Python evalúa la expresión de izquierda a derecha y detiene la evaluación tan pronto como se determina el resultado final.

- El operador **`and`** cortocircuita cuando la primera expresión es falsa. Si la primera expresión es falsa, el resultado final de la expresión booleana será siempre falso, por lo que Python no evalúa la segunda expresión. Por ejemplo:
```python
x = 5 
y = 10 
if x > 0 and y < 0: 
	print("Esta línea no se imprimirá")

```

En este ejemplo, la primera expresión **`x > 0`** es verdadera, pero la segunda expresión **`y < 0`** es falsa. Como la expresión booleana contiene el operador **`and`**, Python no evalúa la segunda expresión, ya que el resultado final de la expresión ya se ha determinado como falso.

- El operador **`or`** cortocircuita cuando la primera expresión es verdadera. Si la primera expresión es verdadera, el resultado final de la expresión booleana será siempre verdadero, por lo que Python no evalúa la segunda expresión. Por ejemplo:
```python
x = 5 
y = 10 
if x > 0 or y < 0: 
	print("Esta línea se imprimirá")
```

En este ejemplo, la primera expresión **`x > 0`** es verdadera. Como la expresión booleana contiene el operador **`or`**, Python no evalúa la segunda expresión, ya que el resultado final de la expresión ya se ha determinado como verdadero.

Es importante tener en cuenta que aunque los operadores de cortocircuito pueden ser más eficientes en términos de tiempo de ejecución, pueden ocultar errores en la lógica del programa si se utilizan incorrectamente. Por lo tanto, es importante tener cuidado al utilizarlos y asegurarse de que el resultado final de la expresión booleana sea el que se espera.

#### Encadenamiento
Se puede encadenar a los operadores lógicos y hacer expresiones mas cortas.
Ejemplo:
```python
edad = 22
if edad >= 15 and edad <= 60:
	print("Edad aceptada")
```

Esta expresión puede ser sustituida por la siguiente:
```python
edad = 22
if 15 <= edad <= 60:
    print("Edad aceptada")
```


## For

El bucle **`for`** es una estructura de control de flujo en Python que se utiliza para iterar sobre una secuencia de elementos. Es decir, se utiliza para recorrer una colección de elementos (como una lista, una tupla o una cadena) o cualquier objeto iterable y ejecutar un conjunto de instrucciones para cada elemento.
La sintaxis básica del bucle **`for`** en Python es la siguiente:
```python
for variable in secuencia: 
        # cuerpo del bucle
```

En esta sintaxis, **`variable`** es una variable que toma el valor de cada elemento de la secuencia en cada iteración del bucle, y **`secuencia`** es una secuencia de elementos que se va a iterar.

Por ejemplo, si queremos imprimir los elementos de una lista llamada **`mi_lista`**, podemos hacerlo de la siguiente manera utilizando un bucle **`for`**:
```python
mi_lista = [1, 2, 3, 4, 5] 
for elemento in mi_lista:
	print(elemento)
```

Este código imprimirá cada elemento de la lista **`mi_lista`** en una línea separada.

También es posible utilizar la función **`range()`** en un bucle **`for`** para iterar un número determinado de veces. Por ejemplo, si queremos imprimir los números del 1 al 10, podemos hacerlo de la siguiente manera:
```python
for i in range(1, 11): 
	print(i)
```

En este ejemplo, la función **`range(1, 11)`** devuelve una secuencia de números del 1 al 10, que se itera utilizando el bucle **`for`**.

Además, es posible utilizar las palabras clave **`break`** y **`continue`** dentro de un bucle **`for`** para modificar su comportamiento. **`break`** se utiliza para interrumpir el bucle y salir de él, mientras que **`continue`** se utiliza para saltar a la siguiente iteración sin ejecutar el resto de las instrucciones del cuerpo del bucle.


### for-else

El bucle **`for-else`** en Python se utiliza para ejecutar un conjunto de instrucciones en caso de que se haya agotado la secuencia que se está iterando en un bucle **`for`**. Es decir, el bloque de instrucciones en el **`else`** se ejecuta únicamente si el bucle **`for`** se ha ejecutado completamente, sin interrupciones ni errores.
La sintaxis del bucle **`for-else`** es la siguiente:
```python
for variable in secuencia: 
    # cuerpo del bucle 
else: 
    # bloque de instrucciones a ejecutar si el bucle for se ha ejecutado completamente
```

En este ejemplo, **`variable`** es la variable que toma el valor de cada elemento de la secuencia en cada iteración del bucle, **`secuencia`** es la secuencia que se va a iterar, y **`else`** es el bloque de instrucciones que se ejecuta después de que se agote la secuencia.
Un ejemplo de uso del bucle **`for-else`** es el siguiente:
```python
mi_lista = [1, 2, 3, 4, 5]
for elemento in mi_lista: 
	if elemento == 6: 
		break 
else: 
	print("La lista no contiene el número 6")
```

En este ejemplo, se itera sobre la lista **`mi_lista`** y se utiliza la instrucción **`break`** para salir del bucle si se encuentra el número 6 en la lista. Si se agota la lista sin encontrar el número 6, se ejecuta el bloque de instrucciones en el **`else`**, que imprime el mensaje "La lista no contiene el número 6".

En resumen, el bucle **`for-else`** se utiliza para ejecutar un conjunto de instrucciones después de que se agote la secuencia que se está iterando en un bucle **`for`**, en caso de que no se hayan producido interrupciones ni errores durante la iteración.

> **Nota**: En los ejemplos anteriores, se trabaja con iterables. Un iterable en Python es cualquier objeto que puede ser recorrido mediante un bucle **`for`**. Un objeto es iterable si implementa el método **`__iter__()`** , que devuelve un iterador que puede recorrer los elementos del objeto. Ejemplos de iterables en Python incluyen listas, tuplas, cadenas, conjuntos y diccionarios. Los iterables son una parte fundamental del lenguaje Python y permiten una programación más concisa y expresiva.


## While

El bucle **`while`** en Python se utiliza para repetir un bloque de código mientras se cumpla una determinada condición. La sintaxis es la siguiente:
```python
while condicion:
    # cuerpo del bucle
```

En este ejemplo, **`condicion`** es la expresión booleana que se evalúa antes de cada iteración del bucle. Si la condición es verdadera, se ejecuta el cuerpo del bucle, y luego se vuelve a evaluar la condición. Este proceso se repite hasta que la condición es falsa, momento en el que el bucle termina. Un ejemplo de una simulación de un terminal con esta estructura seria la siguiente:
```python
while comando.lower() != "salir":  
	comando = input("$ ")
	print(comando)
```

Es importante tener en cuenta que si la condición del bucle **`while`** siempre es verdadera, se produce un **bucle infinito**, lo que significa que el bucle se seguirá ejecutando indefinidamente. Para evitar esto, es necesario incluir una instrucción dentro del cuerpo del bucle que modifique la condición en algún momento, de forma que eventualmente se convierta en falsa y se salga del bucle.

Una forma común de detener un bucle infinito es mediante el uso de una instrucción **`break`** dentro del cuerpo del bucle, que interrumpe la ejecución del bucle y lo saca de él en cualquier momento. También se puede utilizar una instrucción **`if`** dentro del cuerpo del bucle para verificar si se ha alcanzado cierta condición y, si es así, modificar la condición del bucle para que sea falsa y se salga del bucle.

> **Nota**: En Python como tal no existe la estructura de un do-while, pero con estas alternativas de bucles infinitos con la condición de paro dentro del cuerpo del while, se puede simular el funcionamiento de la estructura `do-while`, un ejemplo de esto seria el siguiente:
```python
while True:
	comando = input("$ ")
	print(comando)
	if comando.lower() == "salir":
		break;
```


## Loops anidados

Los bucles anidados en Python son una forma de iterar sobre múltiples colecciones de datos de manera eficiente. Básicamente, un bucle anidado es un bucle dentro de otro bucle.

La forma más común de bucles anidados es tener un bucle **`for`** externo que itera sobre una colección de elementos y un bucle **`for`** interno que itera sobre otra colección de elementos para cada elemento en el bucle externo. El cuerpo del bucle interno se ejecuta completamente una vez para cada elemento del bucle externo. Por ejemplo:
```python
for x in range(1, 4):
	for y in range(1, 3):
		print(f'({x}, {y})')
```

En este ejemplo, el bucle externo itera sobre los números del 1 al 3, y el bucle interno itera sobre los números del 1 al 2 para cada valor de **`x`**. El resultado es una salida de tuplas que combinan cada valor de **`x`** con cada valor de **`y`**.

La idea de un "**outer loop**" (bucle externo) y un "**inner loop**" (bucle interno) se utiliza a menudo en los bucles anidados. En este contexto, el bucle externo se considera el bucle "ganador" (**winner loop**) porque determina el número total de iteraciones, mientras que el bucle interno se considera el bucle "perdedor" (**loser loop**) porque se ejecuta completamente para cada iteración del bucle externo.

En resumen, los bucles anidados en Python permiten iterar sobre múltiples colecciones de datos de manera eficiente, y la idea de un "outer loop" y un "inner loop" se utiliza a menudo para describir su funcionamiento.