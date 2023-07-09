---
banner_icon: ☣️
banner: "![[hubble-space-telescope-and-earth-limb_9461026706_o.jpg]]"
banner_y: 0.504
---

# Tipos básicos

## <mark class="hltr-cyan">Strings</mark>

Sabemos que una variables de tipo String se puede inicializar o definir con las dobles comillas o con las simples comillas:
```python
String_simple = 'comillas simples'
String_doble = "comillas dobles"
```

Pero si queremos una variables que contenga mas caracteres, lo podemos hacer con loas “dobles triples comillas”
```python
descripcion = """
Ultimate Python,
Este curso contemplta todos los detalles
que necesitas para conseguir un trabajo
como programador de Python
"""
```

### Formato de Strings

```python
nombre = "Jorge"
apellido = "Juarez"
nombre_completo = nombre + " " + apellido
print(nombre_completo)
```

Esta forma de de concatenar cadenas de texto no es la mas “elegante”, por lo que se prefiere el formateo de los strings.
Esto se puede realizar de las siguientes formas:

1. Utilizando el método **`format()`**:
	Este método utiliza llaves **`{}`** como marcadores de posición en la cadena. Luego, se puede utilizar el método **`format()`** para reemplazar esos marcadores de posición con valores específicos. Por ejemplo:
	```python
	name = "Juan"
	age = 30
	print("Hola, mi nombre es {} y tengo {} años.".format(name, age))
	```

2. Utilizando literales de cadena f-strings:
	Este método utiliza la letra "f" antes de la cadena para indicar que es un literal de cadena f. Luego, se pueden utilizar llaves **`{}`** con expresiones dentro de ellas como marcadores de posición. Por ejemplo:
	```python
	name = "Maria"
	age = 25
	print(f"Hola, mi nombre es {name} y tengo {age} años.")
	```

3. Utilizando el operador **`%`**:
	Este método utiliza el operador **`%`** como un marcador de posición en la cadena. Luego, se puede utilizar el operador **`%`** para reemplazar esos marcadores de posición con valores específicos. Por ejemplo:
	```python
	name = "Pedro"
	age = 35
	print("Hola, mi nombre es %s y tengo %d años." % (name, age))
	```

Estos son algunos de los métodos más comunes para formatear cadenas en Python. Es importante recordar que cada método tiene sus propias convenciones y reglas para el formateo de cadenas, por lo que se recomienda revisar la documentación oficial de Python para obtener más información sobre cada uno de ellos.

### Métodos de Strings

1. **`len()`**: Este método retorna la longitud del string, es decir, la cantidad de caracteres que contiene.
	Nos permite poder obtener la longitud (de caracteres) que tiene un string en particular.
	Para nosotros poder llamar a esta función, tenemos que hacerlo como con cualquier otra función que nosotros llamemos en Python.
	Eso nosotros lo hacemos con un abre paréntesis redondo y dentro de esto tenemos que indicarle cuál es el string del cual nosotros queremos obtener su longitud.
	Entonces el argumento (==los argumentos son los valores que nosotros le pasamos a una función==) de Len es la variable de un string, o directamente una cadena de texto.
	```python
	len(descripcion)
	```

	Solo tenemos que ponerlo dentro de la función print() para visualizar el resultado:
	```python
	print(len(descripcion))
	 ```
	 
	 En otros lenguajes de programación como lo es C, las cadenas de texto son arreglos de caracteres (char) por lo que esta funcion (len()) funciona tomando esto en cuenta, también podemos acceder a caracteres específicos de una cadena especificada:
	 ```python
	 print(len(nombre_curso))  # Longitud de la cadena.
	 print(nombre_curso[0])  # Caracteres en la posición 0.
	 print(nombre_curso[0:8])  # Caracteres de la posición 0 a la 8.
	 
	 # Caracteres de la posición 9 hasta la ultima posición.
	 print(nombre_curso[9:])
	 
	 # Caracteres de la primera posición hasta la octava posición.
	 print(nombre_curso[:8])
	 
	 # Caracteres de la posición 0 hasta la ultima posición.
	 print(nombre_curso[:])
	 ```
	 Cuando no se especifica la posición de la cadena, Python toma las posiciones por default, que son 0, o la ultima posición; más información sobre el slicing en :[[Tipos avanzados]].
2. **`lower()`**: Este método retorna una copia del string en minúsculas.
3. **`upper()`**: Este método retorna una copia del string en mayúsculas.
4. **`capitalize()`**: Este método retorna una copia del string con la primera letra en mayúscula.
5. **`strip()`**: Este método retorna una copia del string sin los espacios en blanco al principio y al final.
6. **`replace()`**: Este método reemplaza una subcadena por otra en el string.
7. **`split()`**: Este método separa el string en subcadenas utilizando un separador (por defecto, el separador es el espacio en blanco) y retorna una lista con las subcadenas.
8. **`join()`**: Se utiliza para unir los elementos de una secuencia en una sola cadena. Toma una secuencia (como una lista, una tupla o un generador) y devuelve una cadena que contiene todos los elementos de la secuencia concatenados.
	La sintaxis básica del método `.join()` es la siguiente:
	```python
	cadena_separador.join(secuencia)
	```
	- `cadena_separador`: Es una cadena que se utiliza como separador para unir los elementos de la secuencia. Este separador se coloca entre cada par de elementos adyacentes en la cadena resultante. Por ejemplo, si el separador es una coma ",", los elementos estarán separados por comas en la cadena resultante.
	- `secuencia`: Es la secuencia de elementos que se van a unir en una cadena. Puede ser una lista, una tupla u otro tipo de secuencia iterable.
	Ejemplos:
	```python
	# Ejemplo 1
	lista = ['Hola', 'mundo', 'Python']
	cadena_resultante = ' '.join(lista)
	print(cadena_resultante)
	# Salida: Hola mundo Python
	
	# Ejemplo 2
	tupla = ('apple', 'banana', 'cherry')
	cadena_resultante = '-'.join(tupla)
	print(cadena_resultante)
	# Salida: apple-banana-cherry
	
	# Ejemplo 3
	generador = (str(x) for x in range(5))
	cadena_resultante = '+'.join(generador)
	print(cadena_resultante)
	# Salida: 0+1+2+3+4
	```

1. **`startswith()`**: Este método retorna **`True`** si el string comienza con la subcadena especificada como argumento.
2. **`endswith()`**: Este método retorna **`True`** si el string termina con la subcadena especificada como argumento.
3. **`find()`**: Este método retorna la posición de la primera ocurrencia de la subcadena especificada como argumento en el string, o `-1` si no se encuentra.
4. **`count()`**: Este método retorna la cantidad de veces que aparece la subcadena especificada como argumento en el string.
5.  **`title()`**: Este método retorna una copia del string con la primera letra de cada palabra en mayúscula y el resto en minúscula.
6. **`in`**: Este operador se utiliza para verificar si una subcadena está presente en un string. Retorna **`True`** si la subcadena se encuentra en el string y **`False`** en caso contrario.
7. **`not in`**: Este operador se utiliza para verificar si una subcadena no está presente en un string. Retorna **`True`** si la subcadena **no** se encuentra en el string y **`False`** en caso contrario.

Ejemplo:
```python
animal = "  chanCHito feLiz  "
print(animal.upper())  # Cambia todos los caracteres a mayuscula.
print(animal.lower())  # Cambia todos los caracteres a minusculas.
# Pone el primer caracteres en mayuscula y todos los demas en minuscula
print(animal.capitalize())

print(animal.strip())  # Elimina los espacios del princiopio y del final.
print(animal.rstrip())  # Elimina los espacios del lado derecho.
print(animal.lstrip())  # Elimina los espacios del lado izquierdo.
print(animal.strip().capitalize())  # se pueden encadenar los metodos.

print(animal.title())  # Canbi la primeta letra de cada palabra a mayuscula.
# Regresa un indice si es que lo encuentra, y uno valor negativo si es que no lo encuentra.
print(animal.find("CH"))
# Reemplaza el primer argumento por el segundo
print(animal.replace("nCH", "j"))
print("nCH" in animal)  # Devuelve un valor booleano en la busqueda
print("nCH" not in animal)  # Devuelve un valor booleano en la busqueda
```

### Secuencias de escape

Son secuencias de caracteres que se utilizan en Python (y en otros lenguajes de programación) para representar caracteres especiales dentro de una cadena de caracteres. Estas secuencias comienzan con el carácter de barra invertida `\` seguido de un carácter especial.
Las sentencias de escape más utilizadas en Python:
- `\n`: Salto de línea
- `\t`: Tabulación
- ": Comilla doble
- ': Comilla simple
- `\r`: Retorno de carro
- `\b`: Retroceso
- `\f`: Avance de página
- `\v`: Tabulación vertical

---

## <mark class="hltr-cyan">Números</mark>

### Operaciones

```python
print(1 + 3)    # Suma
print(1 - 3)    # Resta
print(1 * 3)    # Multiplicacion
print(1 / 3)    # Division
print(1 // 3)   # Division, pero solo obtiene el valor entero (elimina los decimales)
print(1 % 3)    # Operacion modulo
print(2 ** 3)   # Potencia (2^3)
```

Para actualizar una variable, se puede utilizar la sintaxis de: `numero = numero + 2`, pero una forma mas elegante de hacerlo es la siguiente:
```python
numero += 2
numero -= 2
numero *= 2
numero /= 2
```

### Métodos

#### Métodos nativos de Python:
- **`abs()`**: Devuelve el valor absoluto de un número.
- **`round()`**: Redondea un número al número entero más cercano.
- **`int()`**: Convierte un número en un entero.
- **`float()`**: Convierte un número en un número de punto flotante.
- **`complex()`**: Crea un número complejo a partir de un número o dos números que representan la parte real e imaginaria.

#### Métodos del módulo `math`:
- **`math.sqrt()`**: Devuelve la raíz cuadrada de un número.
- **`math.pow()`**: Eleva un número a una potencia.
- **`math.exp()`**: Devuelve el valor de la función exponencial de un número.
- **`math.log()`**: Devuelve el logaritmo natural de un número.
- **`math.sin()`**: Devuelve el seno de un ángulo en radianes.
- **`math.cos()`**: Devuelve el coseno de un ángulo en radianes.
- **`math.tan()`**: Devuelve la tangente de un ángulo en radianes.
	
	Mas información sobre el módulo math [aquí](https://docs.python.org/3/library/math.html).

### Conversión de datos

La conversión de datos en Python es el proceso de cambiar el tipo de datos de una variable a otro tipo de datos. Esto es útil en muchas situaciones, por ejemplo, cuando se desea realizar cálculos con números en diferentes formatos, o cuando se desea utilizar valores de cadena como números.
En Python, existen varios métodos para realizar la conversión de datos entre diferentes tipos de datos. Algunos de los métodos más comunes son:
1. **`int()`**: Convierte una variable a un entero. Si la variable contiene un número de punto flotante, este método truncará el número y devolverá solo la parte entera.
2. **`float()`**: Convierte una variable a un número de punto flotante.
3. **`str()`**: Convierte una variable a una cadena de caracteres.
4. **`bool()`**: Convierte una variable a un valor booleano. En Python, cualquier valor que no sea cero o vacío se considera verdadero, mientras que el valor cero o vacío se considera falso.

Es importante tener en cuenta que la conversión de datos puede llevar a la pérdida de información si se convierte un tipo de datos a otro que no puede representar toda la información del original. Por ejemplo, si se convierte un número de punto flotante a un entero, la parte decimal se perderá. Es importante entender cómo funciona cada método de conversión y cuándo es apropiado usarlo para evitar errores y pérdida de datos.