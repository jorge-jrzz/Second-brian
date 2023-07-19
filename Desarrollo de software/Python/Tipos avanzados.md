---
banner_icon: 🏙️
banner: "![[lunar-rover_29798990354_o.jpg]]"
banner_y: 0.38
---

# Tipos avanzados

## Listas

Las listas son una estructura de dato que nos permiten almacenar una colección ordenada de elementos. ==Los elementos en una lista pueden ser de cualquier tipo==, y pueden ser modificados, agregados o eliminados en cualquier momento.
Para crear una lista en Python, simplemente utilizamos corchetes y separamos los elementos con comas. Por ejemplo:
```python
mi_lista = [1, 2, 3, 4, 5]
```

Opciones que tenemos con las listas son las siguientes:

###### Crear una lista con un rango de números:
Para crear una lista con un rango de números en Python, puedes utilizar la función `range()` junto con el constructor de lista. Por ejemplo, si quieres crear una lista de números del 1 al 10, puedes hacer lo siguiente:
```python
numeros = list(range(1, 11))
```

Esto creará una lista llamada `numeros` que contiene los números del 1 al 10. La función `range()` acepta dos argumentos: el primer número del rango y el número final del rango, pero el último número del rango no está incluido en la lista.

###### Concatenación de listas:
Para concatenar dos listas en Python, puedes utilizar el operador "+". Por ejemplo, si tienes dos listas "lista1" y "lista2", puedes concatenarlas de la siguiente manera:
```python
lista3 = lista1 + lista2
```

Esto creará una nueva lista llamada "lista3" que contiene los elementos de "lista1" seguidos por los elementos de "lista2".

###### Crear una lista con elementos repetidos:
Para crear una lista con elementos repetidos en Python, puedes multiplicar un elemento por el número de veces que deseas repetirlo. Por ejemplo, si deseas crear una lista con 10 ceros, puedes hacer lo siguiente:
```python
ceros = [0] * 10
```

Esto creará una lista llamada "ceros" que contiene 10 ceros. Puedes cambiar el número 10 para crear una lista con cualquier cantidad de elementos repetidos que necesites.


### Manipulación de listas

##### Indexing

El indexing (indexación) en Python se utiliza para acceder a elementos individuales dentro de una secuencia, como una lista, una cadena o una tupla, utilizando su posición o índice. 
- En Python, los índices comienzan desde 0. Esto significa que el primer elemento de una secuencia tiene un índice de 0, el segundo elemento tiene un índice de 1, y así sucesivamente.
- Puedes acceder a un elemento individual utilizando corchetes `[]` y especificando el índice del elemento que deseas obtener.

**Ejemplos:**

1. Acceder a un elemento de una lista:
	```python
	lista = [10, 20, 30, 40, 50]
	elemento = lista[2]  # Accede al tercer elemento, 30
	```
	En este caso, `elemento` contendrá el valor 30, que es el elemento con índice 2 en la lista.

2. Acceder a un carácter de una cadena:
	```python
	cadena = "Python"
	caracter = cadena[1]  # Accede al segundo carácter, 'y'
	```
	Aquí, `caracter` contendrá el carácter 'y', que es el elemento con índice 1 en la cadena.

3. Acceder a un elemento de una tupla:
	```python
	tupla = (100, 200, 300)
	elemento = tupla[0]  # Accede al primer elemento, 100
	```
	En este caso, `elemento` contendrá el valor 100, que es el primer elemento de la tupla.

Es importante tener en cuenta que los índices deben estar dentro del rango válido para la secuencia. Si intentas acceder a un índice fuera de rango, se producirá un error de índice fuera de rango (`IndexError`).

##### Slicing

En Python, el slicing es una técnica que ==permite extraer partes de una secuencia==, como una lista, una cadena o una tupla. La sintaxis general del slicing es la siguiente:
```python
secuencia[inicio:fin:paso]
```

- `inicio` representa el índice donde comienza el slice. Si se omite, por defecto se toma el primer elemento de la secuencia.
- `fin` representa el índice donde termina el slice. Este índice no se incluye en el resultado. Si se omite, por defecto se toma el último elemento de la secuencia.
- `paso` es un valor opcional que indica el incremento entre los índices del slice. Si se omite, por defecto se toma un paso de 1.

Algunos ejemplos pueden ayudar a entender mejor cómo funciona el slicing:
1. Obtener una porción de una lista:
	```python
	lista = [1, 2, 3, 4, 5, 6, 7, 8, 9]
	porcion = lista[2:6]  # [3, 4, 5, 6]
	```
	En este caso, `porcion` contendrá los elementos de la lista desde el índice 2 hasta el índice 5 (el índice 6 se excluye).

2. Extraer una subcadena de una cadena:
	```python
	cadena = "Python es genial"
	subcadena = cadena[7:9]  # "es"
	```
	Aquí, `subcadena` contendrá los caracteres desde el índice 7 hasta el índice 8 de la cadena.

3. Invertir una cadena utilizando un paso negativo:
	```python
	cadena = "Hola"
	invertida = cadena[::-1]  # "aloH"
	```
	Al especificar un paso de -1, el slicing recorre la cadena en orden inverso, obteniendo así una nueva cadena invertida.


#### Desempaquetado de listas

El desempaquetado de listas en Python es una técnica que nos permite asignar los elementos de una lista a variables individuales de manera eficiente y concisa. Esto puede ser útil cuando tenemos una lista con muchos elementos y queremos asignarlos a variables de forma rápida.
La sintaxis básica del desempaquetado de listas es la siguiente:
```python
lista = [1, 2, 3]
a, b, c = lista
```

En este ejemplo, hemos creado una lista llamada "lista" con los valores 1, 2 y 3. Luego, hemos creado tres variables llamadas "a", "b" y "c" y los hemos asignado a los elementos de la lista utilizando la sintaxis de desempaquetado de listas.
Después de la ejecución de este código, la variable "a" tendrá asignado el valor 1, la variable "b" tendrá asignado el valor 2 y la variable "c" tendrá asignado el valor 3.

* También se puede desempaquetar las listas asignándola a múltiples variables (como lo que se realizo anteriormente) y a objetos iterables :
	```python
	primero, *otros, ultimo = numeros
	print(primero, ultimo, otros)
	```

	En este ejemplo, se utilizó una lista que contienen números que van del 1 al 9, y se le asigna la variable `primero` a valor 1 de la lista, después al objeto iterable `otros` se le asigna una sublista con los números que van del 2 al 8, esto porque el valor 9 de la lista se le es asignado a la variable `ultimo`. La salida del código anterior será:
	```BASH
	1 9 [2, 3, 4, 5, 6, 7, 8]
	```

- El desempaquetado de listas también se puede utilizar en conjunción con la función "zip" para iterar a través de varias listas simultáneamente. Por ejemplo:
	```python
	nombres = ['Juan', 'María', 'Pedro']
	edades = [25, 30, 35]
	for nombre, edad in zip(nombres, edades):
		print(nombre, edad)
	```

	En este ejemplo, hemos creado dos listas llamadas "nombres" y "edades". Luego, hemos utilizado la función "zip" para iterar a través de ambas listas simultáneamente y hemos asignado cada elemento de las listas a una variable individual ("nombre" y "edad"). La salida del código anterior será:
	```BASH
	Juan 25
	María 30
	Pedro 35
	```


#### Iteraración de listas

La función **`enumerate`** en Python es una función incorporada que se utiliza para iterar sobre una secuencia (como una lista, tupla o cadena) y generar una tupla que contiene un índice y el valor correspondiente de la secuencia en cada iteración.
La sintaxis básica de la función **`enumerate`** es la siguiente:
```python
enumerate(iterable, start=0)
```

Donde **`iterable`** es la secuencia que se va a iterar y **`start`** es el índice inicial que se va a utilizar. Por defecto, el índice inicial es 0.
Más informacion sobre los iterables en la seccion \"for-else" de la siguiente pagina: [[Control de flujo en py]].

Veamos un ejemplo para entender mejor cómo funciona esta función:
```python
frutas = ['manzana', 'pera', 'naranja', 'plátano']
for indice, fruta in enumerate(frutas):
	print(indice, fruta)
```

La salida de este código sería la siguiente:
```BASH
0 manzana
1 pera
2 naranja
3 plátano
```

En este ejemplo, se utiliza la función **`enumerate`** para recorrer la lista de frutas y en cada iteración se genera una tupla que contiene el índice de la fruta y el valor de la fruta correspondiente. Estas tuplas se almacenan en las variables **`indice`** y **`fruta`**, respectivamente. En cada iteración, se imprime el índice y el valor de la fruta.

La función **`enumerate`** es muy útil cuando se necesita recorrer una secuencia y, al mismo tiempo, se necesita conocer el índice de cada elemento. En lugar de tener que mantener un contador manualmente, se puede utilizar esta función para generar automáticamente los índices en cada iteración.


#### Búsqueda elementos en listas

En Python, existen varias formas de buscar elementos en una lista. A continuación, se presentan algunas de las opciones más comunes:

1. ==Búsqueda secuencial==: Es la forma más sencilla de buscar un elemento en una lista. Consiste en recorrer la lista elemento por elemento hasta encontrar el valor deseado. Aquí te presento un ejemplo:
	```python
	lista = [2, 4, 6, 8, 10]
	buscado = 8
	for i in lista:
		if i == buscado:
			print("El elemento", buscado, "está en la lista.")
			break
		else:
			print("El elemento", buscado, "no está en la lista.")
	```

2. ==Utilizando el método `index()`==: La clase list en Python ofrece el método **`index()`** para buscar el índice de un elemento en una lista. Si el elemento no está en la lista, se genera una excepción **`ValueError`**. A continuación, un ejemplo:
	```python
	lista = [2, 4, 6, 8, 10]
	buscado = 8
	try:
		indice = lista.index(buscado)
		print("El elemento", buscado, "está en la posición", indice)
	except ValueError:
		print("El elemento", buscado, "no está en la lista.")
	```

3. ==Utilizando la función `in`==: La expresión **`in`** se utiliza para verificar si un elemento está presente en una lista. Retorna un valor booleano (**`True`** si el elemento está en la lista, **`False`** si no está en la lista). Aquí te presento un ejemplo:
	```python
	lista = [2, 4, 6, 8, 10]
	buscado = 8
	if buscado in lista:
		print("El elemento", buscado, "está en la lista.")
	else:
		print("El elemento", buscado, "no está en la lista.")
	```

En general, la búsqueda secuencial es la forma más sencilla y directa de buscar elementos en una lista, pero puede resultar lenta si la lista es muy grande. Si se espera tener que buscar elementos con frecuencia, puede ser conveniente utilizar un diccionario o un conjunto en lugar de una lista. Estas estructuras de datos son más eficientes para búsquedas, pero requieren que los elementos sean únicos.


#### Agregando y eliminando elementos de una lista

Para eliminar o agregar elementos a una lista en Python, existen varias funciones y métodos útiles que se pueden utilizar.

Para **eliminar elementos** de una lista en Python, se pueden utilizar los siguientes métodos
- **`remove(elemento)`**: elimina el primer elemento de la lista que coincide con el valor del argumento "elemento". Si el elemento no está presente en la lista, se generará un error ValueError.
- **`pop([índice])`**: elimina y devuelve el elemento en la posición especificada por "índice". Si no se proporciona un índice, se eliminará y se devolverá el último elemento de la lista.
- **`del lista[índice]`**: elimina el elemento en la posición especificada por "índice". También se puede utilizar para eliminar un rango de elementos de la lista utilizando la sintaxis **`del lista[índice_inicio:índice_fin]`**.

Para **agregar elementos** a una lista en Python, se pueden utilizar los siguientes métodos
- **`append(elemento)`**: agrega un elemento al final de la lista.
- **`extend(iterable)`**: agrega los elementos de un iterable (por ejemplo, otra lista) al final de la lista.
- **`insert(índice, elemento)`**: inserta un elemento en la posición especificada por "índice". Los elementos existentes se desplazan hacia la derecha para dejar espacio para el nuevo elemento.

Ejemplos de cómo usar estos métodos:
```python
# Creamos una lista
mi_lista = [1, 2, 3, 4, 5]

# Eliminamos el elemento con valor 3
mi_lista.remove(3)

# Eliminamos el último elemento de la lista
mi_lista.pop()

# Eliminamos el elemento en la posición 1
del mi_lista[1]

# Agregamos el elemento 6 al final de la lista
mi_lista.append(6)

# Agregamos los elementos 7, 8 y 9 al final de la lista
mi_lista.extend([7, 8, 9])

# Insertamos el elemento 0 en la primera posición de la lista
mi_lista.insert(0, 0)
```

Después de estos cambios, la lista resultante sería: 
```BASH
[0, 2, 4, 5, 6, 7, 8, 9]
```


#### Ordenamiento de listas

En Python, las listas se pueden ordenar fácilmente utilizando la función **`sorted()`** o el método **`sort()`**.

- La función **`sorted()`** devuelve una nueva lista ordenada a partir de la lista original, sin modificar la lista original. Por ejemplo:
	```python
	# Creamos una lista desordenada
	mi_lista = [5, 2, 8, 1, 3]
	
	# Ordenamos la lista usando la función sorted()
	mi_lista_ordenada = sorted(mi_lista)
	
	# Imprimimos la lista original y la lista ordenada
	print(mi_lista)  # [5, 2, 8, 1, 3]
	print(mi_lista_ordenada)  # [1, 2, 3, 5, 8]
	```

- El método **`sort()`**, por otro lado, ordena la lista original en su lugar, es decir, modifica la lista original sin crear una nueva. Por ejemplo:
	```python
	# Creamos una lista desordenada
	mi_lista = [5, 2, 8, 1, 3]
	
	# Ordenamos la lista usando el método sort()
	mi_lista.sort()
	
	# Imprimimos la lista original (que ahora está ordenada)
	print(mi_lista)  # [1, 2, 3, 5, 8]
	```

Ambos métodos pueden aceptar argumentos opcionales que especifican la dirección de la ordenación (**`reverse=True`** para ordenar en orden descendente) y la función de clave (**`key`**) para personalizar el criterio de ordenación.
Por ejemplo, para ordenar una lista de cadenas por su longitud, se puede especificar la función de clave como **`len`**:
```python
# Creamos una lista de cadenas
mi_lista = ['python', 'es', 'un', 'lenguaje', 'genial']

# Ordenamos la lista por longitud de cadena
mi_lista_ordenada = sorted(mi_lista, key=len)

# Imprimimos la lista original y la lista ordenada
print(mi_lista)  # ['python', 'es', 'un', 'lenguaje', 'genial']
print(mi_lista_ordenada)  # ['es', 'un', 'python', 'genial', 'lenguaje']
```

En resumen, para ordenar una lista en Python, puedes usar la función **`sorted()`** para crear una nueva lista ordenada o el método **`sort()`** para ordenar la lista original en su lugar. Ambos métodos aceptan argumentos opcionales para personalizar la dirección de la ordenación y el criterio de ordenación.


### Listas de comprensión

Las listas de comprensión son una forma concisa y elegante de crear listas en Python. Permiten crear una lista nueva utilizando una sintaxis compacta y fácil de leer en una sola línea de código.
La sintaxis básica de una lista de comprensión es la siguiente:
```python
nueva_lista = [expresion for elemento in iterable if condicion]
```

Donde `expresion` es la expresión que se evalúa y agrega a la nueva lista, `elemento` es la variable que representa cada elemento del iterable, `iterable` es una secuencia o colección de elementos que se recorren, y `condicion` es una expresión booleana opcional que filtra los elementos que se agregan a la nueva lista.

Por ejemplo, para crear una lista de los cuadrados de los números del 1 al 5, se puede utilizar una lista de comprensión de la siguiente manera:
```python
cuadrados = [x**2 for x in range(1, 6)]
```

Esto crea una nueva lista llamada `cuadrados` que contiene los valores ```[1, 4, 9, 16, 25]```.

Las listas de comprensión también se pueden utilizar para filtrar elementos de una lista existente. Por ejemplo, para crear una nueva lista que contenga solo los números pares de una lista existente, se puede utilizar la siguiente lista de comprensión:
```python
numeros_pares = [x for x in mi_lista if x % 2 == 0]
```

En este ejemplo, la expresión `x for x in mi_lista` recorre la lista original `mi_lista` y agrega cada elemento `x` a la nueva lista si cumple la condición `x % 2 == 0`, que filtra los números pares.

Las listas de comprensión pueden incluir múltiples niveles de bucles y condicionales para crear listas más complejas. Por ejemplo, supongamos que tenemos dos listas, **`lista1`** y **`lista2`**, y queremos crear una lista de todas las posibles tuplas que se pueden formar a partir de los elementos de ambas listas. Para hacer esto, podemos utilizar una lista de comprensión con dos bucles **`for`**, como se muestra a continuación.
```python
lista1 = [1, 2, 3]
lista2 = ['a', 'b', 'c']
pares = [(x, y) for x in lista1 for y in lista2]
```

En este ejemplo, la lista de comprensión **`[(x, y) for x in lista1 for y in lista2]`** define dos bucles **`for`**, uno que itera sobre los elementos de **`lista1`** y otro que itera sobre los elementos de **`lista2`**.
Para cada par de elementos (**`x`**, **`y`**) de ambas listas, se crea una tupla que contiene estos dos elementos, es decir, la expresión **`(x, y)`**. La lista resultante **`pares`** contendrá todas las posibles tuplas que se pueden formar a partir de los elementos de **`lista1`** y **`lista2`**, en este caso:
```BASH
[(1, 'a'), (1, 'b'), (1, 'c'), (2, 'a'), (2, 'b'), (2, 'c'), (3, 'a'), (3, 'b'), (3, 'c')]
```

Es importante mencionar que la lista de comprensión en este ejemplo no tiene una condición **`if`**, por lo que se crean todas las posibles tuplas que se pueden formar a partir de los elementos de ambas listas. Si se quisiera agregar una condición para filtrar algunos de los elementos, se podría hacer agregando una expresión **`if`** al final de la lista de comprensión.

En resumen, las listas de comprensión son una forma concisa y elegante de crear listas en Python utilizando una sintaxis compacta y fácil de leer. Son una herramienta útil para crear listas nuevas y filtrar elementos de listas existentes en una sola línea de código.


#### Funciones `map()` y `filter()`

Tanto **`map`** como **`filter`** son funciones de orden superior en Python que toman una función y un iterable como entrada, y producen un nuevo iterable como salida. Ambas funciones son muy útiles para procesar datos y transformarlos en otros formatos.

- La función **`map()`** aplica una función dada a cada elemento de un iterable y devuelve un nuevo iterable con los resultados. Por ejemplo, si tienes una lista de números y quieres calcular el cuadrado de cada uno de ellos, puedes hacer lo siguiente:
	```python
	numeros = [1, 2, 3, 4, 5]
	cuadrados = list(map(lambda x: x ** 2, numeros))
	print(cuadrados)
	
	# Output: [1, 4, 9, 16, 25]
	```

- La función **`filter()`** toma una función de prueba y un iterable como entrada, y devuelve un nuevo iterable que contiene solo los elementos del iterable que pasan la prueba definida por la función. Por ejemplo, si tienes una lista de números y quieres filtrar solo los números impares, puedes hacer lo siguiente:
	```python
	numeros = [1, 2, 3, 4, 5]
	impares = list(filter(lambda x: x % 2 == 1, numeros))
	print(impares)
	
	# Output: [1, 3, 5]
	```

Ambas funciones pueden ser muy útiles para procesar grandes cantidades de datos y transformarlos en formatos útiles para su posterior análisis. Sin embargo, es importante tener en cuenta que a veces pueden ser menos eficientes que otras técnicas de procesamiento de datos, como la comprensión de listas, especialmente en casos de pequeñas cantidades de datos.


## Tuplas

Las tuplas en Python son un tipo de datos ***inmutable*** que se utilizan para almacenar una colección de elementos ordenados. Las tuplas se definen usando paréntesis y los elementos se separan por comas.
A diferencia de las listas, las tuplas son inmutables, lo que significa que no se pueden modificar una vez creadas. Por esta razón, son útiles para almacenar datos que no deben ser cambiados durante el ciclo de vida de un programa.
Las tuplas también son más eficientes en términos de memoria y rendimiento que las listas, ya que ocupan menos espacio y se pueden acceder más rápidamente.

Para acceder a los elementos de una tupla, se utiliza la misma sintaxis que con las listas, utilizando un índice entre corchetes. Por ejemplo:
```python
mi_tupla = (1, 2, 3, "cuatro")
print(mi_tupla[0])

# Output: 1
```

Las tuplas también se pueden utilizar para devolver múltiples valores desde una función, lo que puede ser muy útil en algunos casos:
```python
def obtener_coordenadas():
	return 1, 2

x, y = obtener_coordenadas()
print(x, y)

# Output: 1 2
```

En resumen, las tuplas son una estructura de datos útil en Python para almacenar elementos ordenados e inmutables, y son especialmente útiles en casos donde se necesita una colección de valores que no se pueden cambiar.


## Sets

Los sets en Python son una estructura de datos que se utilizan para almacenar una colección de elementos ***únicos e inmutables***. Los elementos de un set no están ordenados, lo que significa que no se pueden acceder a ellos mediante un índice.

Los sets se definen utilizando llaves **`{}`** o la función **`set()`**. Por ejemplo:
```python
mi_set = {1, 2, 3}
otro_set = set([3, 4, 5])
```

Los sets son útiles para eliminar duplicados de una lista o cualquier otra estructura iterable. También se pueden utilizar para realizar operaciones de conjunto, como la unión, intersección y diferencia de conjuntos, y los operadores son los siguientes:
```python
print(primer | segundo)  # Union
print(primer & segundo)  # Interseccion
print(primer - segundo)  # Diferencia
print(primer ^ segundo)  # Diferencia simetrica
```

En donde **`primer`** y **`segundo`** son sets.

Los sets son mutables, lo que significa que se pueden agregar y eliminar elementos utilizando los métodos **`add()`** y **`remove()`**, respectivamente.
```python
mi_set = {1, 2, 3}
mi_set.add(4)
mi_set.remove(1)
```

En resumen, los sets son una estructura de datos útil en Python para almacenar elementos únicos e inmutables y realizar operaciones de conjunto. Son mutables y se definen utilizando llaves **`{}`** o la función **`set()`**.


## Diccionarios

Los diccionarios en Python son una estructura de datos que se utilizan para almacenar pares de clave-valor. Cada elemento del diccionario se compone de una clave y un valor, y las claves deben ser únicas e inmutables.

Los diccionarios se definen utilizando llaves **`{}`** o la función **`dict()`**. Por ejemplo:
```python
mi_diccionario = {'clave1': 'valor1', 'clave2': 'valor2'}
otro_diccionario = dict(clave1='valor1', clave2='valor2')
```

Los valores en un diccionario se pueden acceder utilizando su clave. Los diccionarios son mutables, lo que significa que se pueden agregar, modificar y eliminar elementos utilizando los métodos **`update()`**, **`pop()`** y **`del()`**, respectivamente.
```python
mi_diccionario = {'clave1': 'valor1', 'clave2': 'valor2'}
mi_diccionario['clave3'] = 'valor3'
mi_diccionario.update({'clave4': 'valor4'})
del mi_diccionario['clave1']
valor2 = mi_diccionario.pop('clave2')
```

Los diccionarios son útiles para asociar información relacionada en una sola estructura de datos. Por ejemplo, se pueden utilizar para almacenar información sobre un usuario, como su nombre, edad y dirección.


### Desempaquetar diccionarios

El modo de desempaquetar los diccionarios es muy parecido a con lo hacemos con las listas, pero ahora sera con dos asteriscos, por ejemplo:
```python
punto1 = {"x": 19, "y": 22}
punto2 = {"z": 15}

nuevoPunto = {**punto1, **punto2}
print(nuevoPunto)

# Output: {'x': 19, 'y': 22, 'z': 15}
```

Otro ejemplo de desempaquetado de diccionarios con el metodo `**values()**`
```python
person = {'name': 'John', 'age': 30, 'country': 'USA'}
name, age, country = person.values()

print(name)  # Output: John
print(age)  # Output: 30
print(country)  # Output: USA
```

En este ejemplo, se crea un diccionario **`person`** con tres claves **`name`**, **`age`** y **`country`**. Luego, se utiliza el operador de desempaquetamiento para asignar los valores de cada clave a las variables **`name`**, **`age`** y **`country`** respectivamente.

En resumen, el operador de desempaquetamiento en Python permite descomponer una estructura de datos en sus elementos individuales. Se utiliza con frecuencia con tuplas y listas, y se puede utilizar en combinación con el operador **`*`** para desempaquetar una parte de una estructura de datos y asignar el resto a una variable individual-


## Filas o colas

Las colas o filas, o también conocidas como queue, son una estructura de datos que se caracterizan por ser del tipo ***FIFO*** (First In, First Out), es decir, el primer elemento en ser ingresado a la cola es el primero en ser eliminado.

En Python, se puede implementar una cola utilizando la clase deque del módulo collections. Para crear una cola vacía, se puede usar la siguiente sintaxis:
```python
from collections import deque
mi_cola = deque()
```

Para agregar elementos a la cola, se utiliza el método **`append()`**, y para eliminar el primer elemento de la cola se utiliza el método **`popleft()`**. Por ejemplo:
```python
mi_cola = deque()

mi_cola.append('a')
mi_cola.append('b')
mi_cola.append('c')

print(mi_cola)  # Output: deque(['a', 'b', 'c'])

primer_elemento = mi_cola.popleft()

print(primer_elemento)  # Output: 'a'
print(mi_cola)  # Output: deque(['b', 'c'])
```

Además, al igual que con las listas, se pueden recorrer los elementos de la cola utilizando un ciclo **`for`**. Por ejemplo:

```python
mi_cola = deque(['a', 'b', 'c'])
for elemento in mi_cola:
	print(elemento)
```

Obteniendo la siguiente salida: 
```BASH
a
b
c
```


## Pilas 

Las pilas son estructuras de datos que se usan para almacenar elementos en los que el último en entrar es el primero en salir (***LIFO***). En Python, podemos implementar una pila utilizando una lista.
Para agregar elementos a la pila, utilizamos el método **`append()`** de la lista. Para eliminar el último elemento agregado a la pila, usamos el método **`pop()`**, sin especificar un índice, lo que eliminará el último elemento agregado a la lista (y por tanto el último en entrar en la pila).

Aquí hay un ejemplo de cómo crear y utilizar una pila utilizando una lista:
```python
pila = []  # Creamos una lista vacía que actuará como pila
pila.append('elemento 1')
pila.append('elemento 2')
pila.append('elemento 3')

print(pila)  # ['elemento 1', 'elemento 2', 'elemento 3']

elemento_eliminar = pila.pop()

print(elemento_eliminar)  # 'elemento 3'
print(pila)  # ['elemento 1', 'elemento 2']
```

En este ejemplo, creamos una lista vacía que actuará como pila, y luego agregamos tres elementos utilizando el método **`append()`**. Luego, eliminamos el último elemento agregado a la pila utilizando el método **`pop()`** sin argumentos.

## Expresiones Lambda

Las expresiones lambda, también conocidas como funciones lambda, son una forma concisa de definir funciones en Python. Una función lambda es una ***función anónima*** que se puede definir en una sola línea de código y que puede tomar cualquier número de argumentos, pero solo puede tener una expresión como cuerpo.
La sintaxis básica de una función lambda es la siguiente:
```python
lambda argumentos: expresión
```

Donde `argumentos` es una lista separada por comas de los argumentos que la función lambda puede tomar, y `expresión` es una única expresión que se ejecuta cuando se llama a la función lambda.
Por ejemplo, aquí hay una función lambda que toma dos argumentos y devuelve su suma:
```python
suma = lambda x, y: x + y
```

Esta función lambda es equivalente a la siguiente función definida con la sintaxis regular:
```python
def suma(x, y):
	return x + y
```

En resumen, las expresiones lambda son una forma concisa de definir funciones anónimas en Python. Se utilizan comúnmente en combinación con otras funciones para crear un código más legible y conciso.
Para más informacion sobre los diferentes tipos y usos de las funciones: [[Funciones]].