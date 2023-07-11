---
banner_icon: ⛲
banner: "![[grail_29250978540_o.jpg]]"
banner_y: 0.584
---

# Funciones

En Python, una función es un bloque de código que se puede llamar desde cualquier lugar del programa y que realiza una tarea específica. Para definir una función, se utiliza la palabra clave **`def`**, seguida del nombre de la función y los parámetros entre paréntesis. El cuerpo de la función va indentado.
Por ejemplo, la siguiente función suma dos números y devuelve el resultado:
```python
def suma(a, b):
	resultado = a + b
	return resultado
```

En este ejemplo, **`suma`** es el nombre de la función y **`a`** y **`b`** son los parámetros. El cuerpo de la función suma **`a`** y **`b`** y devuelve el resultado.

==Los parámetros son valores que se pasan a una función al llamarla.== En el ejemplo anterior, **`a`** y **`b`** son los parámetros que se pasan a la función **`suma`**. Cuando se llama a una función, se pueden pasar valores para los parámetros entre paréntesis. Por ejemplo:
```python
resultado = suma(2, 3)
print(resultado) # imprime 5
```

En este ejemplo, se llama a la función **`suma`** con los argumentos **`2`** y **`3`**. ==Los argumentos son los valores reales que se pasan a la función.== En este caso, **`2`** y **`3`** son los argumentos que se pasan a la función **`suma`** como los valores de **`a`** y **`b`**, respectivamente.

Las funciones pueden tener múltiples parámetros y múltiples argumentos. Los parámetros se separan por comas en la definición de la función, y los argumentos se separan por comas al llamar a la función.
Ejemplo para diferenciar los parámetros de los argumentos:
![[partes_funciones.png | 600]]

Además, en Python, se pueden definir funciones con parámetros opcionales. Para hacer esto, se asigna un valor predeterminado al parámetro en la definición de la función. Si el argumento no se pasa al llamar a la función, el valor predeterminado se utiliza en su lugar. Por ejemplo:
```python
def saludar(nombre, saludo='Hola'):
	print(f'{saludo}, {nombre}!')

saludar('Juan') # imprime 'Hola, Juan!'
saludar('María', 'Buenos días') # imprime 'Buenos días, María!'
```

En este ejemplo, la función **`saludar`** tiene un parámetro **`saludo`** opcional con un valor predeterminado de **`'Hola'`**. Si se llama a la función con un solo argumento (**`saludar('Juan')`**), el valor predeterminado se utiliza para **`saludo`**. Si se llama a la función con dos argumentos (**`saludar('María', 'Buenos días')`**), se utiliza el segundo argumento como el valor de **`saludo`**.

En resumen, en Python, una función es un bloque de código que realiza una tarea específica. Los parámetros son valores que se pasan a la función al llamarla, y los argumentos son los valores reales que se pasan. Las funciones pueden tener múltiples parámetros y argumentos, y se pueden definir con parámetros opcionales que tienen valores predeterminados.


## Argumentos nombrados

Los argumentos nombrados son una forma de pasar argumentos a una función en Python mediante su nombre en lugar de su posición. En lugar de pasar los argumentos en el orden en que aparecen en la definición de la función, se pueden pasar los argumntos utilizando su nombre correspondiente seguido de un signo igual (**`=`**).
Por ejemplo, considera la siguiente función que toma tres argumentos: **`a`**, **`b`**, y **`c`**:
```python
def foo(a, b, c):
	print(f'a={a}, b={b}, c={c}')
```

Podemos llamar a la función **`foo`** de las siguientes formas:
```python
foo(1, 2, 3)  # a=1, b=2, c=3
foo(a=1, b=2, c=3)  # a=1, b=2, c=3
foo(b=2, c=3, a=1)  # a=1, b=2, c=3
```

En la primera llamada, los argumentos se pasan por posición, por lo que **`1`** se asigna a **`a`**, **`2`** a **`b`**, y **`3`** a **`c`**. En la segunda llamada, los argumentos se pasan mediante su nombre correspondiente, y en la tercera llamada, los argumentos se pasan en un orden diferente al de la definición de la función, pero Python utiliza el nombre de cada argumento para asignar los valores correctamente.

El uso de argumentos nombrados puede hacer que el código sea más fácil de leer y entender, especialmente cuando se tiene una función con muchos argumentos. También puede ser útil cuando se quiere omitir argumentos opcionales y pasar solo aquellos que son necesarios.


## Xargs

"Xargs" es una abreviatura de ***"extended arguments"*** (argumentos extendidos) y se refiere a un parámetro especial que se puede utilizar en la definición de una función en Python. El parámetro **`*args`** permite a una función aceptar cualquier número de argumentos posicionales (es decir, argumentos que se pasan por posición en lugar de por nombre) que se le pasen. El asterisco (**`*`**) antes de **`args`** indica a Python que este parámetro puede aceptar múltiples argumentos y que deben ser agrupados en una tupla.
Por ejemplo, considera la siguiente función que toma un número variable de argumentos y los suma:
```python
def suma(*args):
	total = 0
	for arg in args:
		total += arg
	return tota
```

Esta función puede ser llamada con cualquier número de argumentos posicionales, y los suma todos:
```bash
>>> suma(1, 2, 3)
6

>>> suma(1, 2, 3, 4, 5)
15

>>> suma(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
55
```

En resumen, el parámetro **`*args`** ==permite a una función aceptar un número variable de argumentos posicionales, que se agrupan en una tupla (el cual es un iterable).== Los "xargs" pueden ser útiles en situaciones donde se necesita una función que pueda aceptar un número desconocido de argumentos, como por ejemplo cuando se trabaja con listas de longitud variable.


## kwargs

"Kwargs" es una abreviatura de "***keyword arguments***" (argumentos de palabra clave) y se refiere a un parámetro especial que se puede utilizar en la definición de una función en Python. El parámetro **`kwargs`** permite a una función aceptar cualquier número de argumentos de palabra clave que se le pasen. Los argumentos de palabra clave se especifican como pares **`clave=valor`**, donde la **`clave`** es una cadena que describe el argumento y el **`valor`** es el valor real que se pasará a la función
Por ejemplo, considera la siguiente función que toma argumentos posicionales y de palabra clave y los utiliza para imprimir una cadena de formato:
```python
def imprimir_datos(nombre, edad, **kwargs):
	print("Nombre:", nombre)
	print("Edad:", edad)
	for clave, valor in kwargs.items():
		print(clave + ":", valor)
```

Esta función puede ser llamada con cualquier número de argumentos posicionales y de palabra clave, y los imprime todos
```bash
>>> imprimir_datos("Juan", 30, ciudad="Madrid", trabajo="Programador")
Nombre: Juan
Edad: 30
ciudad: Madrid
trabajo: Programador
```

En resumen, el parámetro **`**kwargs`** ==permite a una función aceptar un número variable de argumentos de palabra clave, que se agrupan en un diccionario.== Los "kwargs" pueden ser útiles en situaciones donde se necesita una función que pueda aceptar argumentos de palabra clave de longitud variable, como por ejemplo cuando se trabaja con opciones de configuración de un programa.


### Alcance (global)

El alcance de una función en Python se refiere a la accesibilidad y visibilidad de las variables que se definen dentro de la función. Las variables definidas dentro de una función se conocen como variables locales y solo son accesibles dentro de esa función. Esto significa que una variable local no se puede acceder desde fuera de la función, ni siquiera desde una función que se llame desde dentro de ella. Por otro lado, las variables definidas fuera de una función se llaman variables globales y son accesibles desde cualquier lugar del código.
Es importante tener en cuenta que las variables globales pueden ser accedidas dentro de una función, pero si se intenta modificar una variable global dentro de una función, se creará una nueva variable local con el mismo nombre en su lugar. Para evitar esto, se debe utilizar la palabra clave **`global`** seguida del nombre de la variable para indicar que se está haciendo referencia a la variable global y no creando una nueva variable local; ejemplo:
```python
x = 5

def modificar_x():
	global x
	x = 10

print("Antes de llamar a la función, x es igual a", x)
modificar_x()
print("Después de llamar a la función, x es igual a", x)
```

En este ejemplo, se tiene una variable global **`x`** con un valor inicial de 5. La función **`modificar_x()`** utiliza la palabra reservada **`global`** para indicar que se está haciendo referencia a la variable global **`x`**. Luego, dentro de la función, se modifica el valor de **`x`** a 10.
Cuando se llama a la función **`modificar_x()`**, se imprime el valor de **`x`** antes y después de la llamada a la función. Antes de llamar a la función, **`x`** es igual a 5, pero después de llamar a la función, **`x`** es igual a 10. Esto demuestra que la variable global **`x`** se ha modificado desde dentro de la función utilizando la palabra reservada **`global`**.
En general, se recomienda limitar el uso de variables globales y utilizar argumentos de función para comunicarse entre funciones y compartir información. De esta manera, se evitan posibles errores y se mantiene un mejor control del alcance de las variables en el código.
En pocas palabras, trabajar con variables globales es considerado un ***mala practica.***


#### Variable `_` (guion bajo)

En Python, la variable **`_`** (guión bajo) se utiliza comúnmente para indicar un valor que no se va a utilizar más adelante en el código. También se puede utilizar como nombre de una variable temporal en algunos casos.
Por ejemplo, supongamos que se está iterando sobre una lista y solo se necesita el valor de cada elemento, pero no se va a utilizar el índice. En este caso, se puede utilizar la variable **`_`** como nombre para el índice, ya que no se va a utilizar posteriormente:
```python
mi_lista = ['a', 'b', 'c']

for _ in mi_lista:
	# Realizar alguna acción con el valor, pero no con el índice
	print('Valor:', _)
```

También se puede utilizar la variable **`_`** para almacenar el resultado de una expresión o función que no se va a utilizar posteriormente:
```python
resultado = funcion_que_devuelve_un_valor()
_ = resultado
```

En resumen, la variable **`_`** se utiliza para indicar que un valor no se va a utilizar más adelante en el código. Es una convención de Python y no afecta el comportamiento del programa.

Para saber mas sobre estructuras de control de flujo como lo es la estructura **`for`** visitar la siguiente pagina: [[Control de flujo en py]].