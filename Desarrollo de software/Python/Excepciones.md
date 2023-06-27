## <mark class="hltr-red">Introduccion</mark>

En Python, las excepciones son eventos que ocurren durante la ejecución de un programa y que interrumpen el flujo normal de ejecución. Cuando ocurre una excepción, se genera un objeto de excepción que puede ser capturado y manejado por el programa.

La gestión de excepciones es una forma de manejar errores y situaciones excepcionales de manera controlada. En lugar de que un error cause la terminación abrupta del programa, las excepciones permiten al programador detectar y responder a los errores de manera adecuada.

La sintaxis básica para manejar excepciones en Python es el bloque `try-except`. El código problemático se coloca dentro del bloque `try`, y si ocurre una excepción, se captura en el bloque `except` correspondiente. De esta manera, se puede proporcionar un manejo específico para diferentes tipos de excepciones.

Aquí tienes un ejemplo simple de cómo usar el bloque `try-except`:

```python
try:
	n1 = int(input("Ingresa primer numero: "))

except Exception as e:
	print(type(e))
```

En este ejemplo, la parte `except` se ejecutará si se produce una excepción dentro del bloque `try`. En este caso, se captura cualquier excepción que ocurra y se almacena en la variable `e` (por conbencion, tambien se puede utilizar `ex`). La palabra clave `Exception` en la declaración `except` indica que se capturará cualquier excepción de tipo genérico.
Dentro del bloque `except`, se imprime el tipo de excepción utilizando la función `type()`. Esto proporcionará información sobre el tipo específico de excepción que se ha producido.
Por ejemplo, si el usuario ingresa un valor no numérico, como una cadena de texto, al solicitar el primer número, se generará una excepción de tipo `ValueError`. El bloque `except` capturará esa excepción y se imprimirá el tipo de excepción (`<class 'ValueError'>`) en la salida.

La captura de excepciones permite manejar errores de manera controlada y proporcionar un comportamiento específico cuando se producen. Al capturar excepciones y manejarlas de manera adecuada, se evita que el programa se detenga inesperadamente y se pueden proporcionar mensajes de error o acciones personalizadas según el tipo de excepción.

Las excepciones en Python son una herramienta poderosa para manejar errores y situaciones excepcionales de manera controlada. Al utilizar bloques `try-except` adecuados, se puede capturar y manejar excepciones de forma específica, lo que permite que el programa continúe ejecutándose sin interrupciones inesperadas.
<br> 
## <mark class="hltr-red">Tipos de excepciones</mark>

Existen varios tipos de excepciones integradas que se utilizan para representar diferentes tipos de errores y situaciones excepcionales. Estos tipos de excepciones se utilizan para capturar y manejar errores específicos de manera adecuada. Algunos de los tipos de excepciones más comunes son:

1. `TypeError`: Se genera cuando se realiza una operación en un objeto de un tipo incorrecto.
2. `ValueError`: Se genera cuando se pasa un argumento con un valor incorrecto a una función o método.
3. `ZeroDivisionError`: Se genera cuando se intenta dividir un número por cero.
4. `IndexError`: Se genera cuando se intenta acceder a un índice inválido en una secuencia, como una lista o una cadena.
5. `KeyError`: Se genera cuando se intenta acceder a una clave inexistente en un diccionario.
6. `FileNotFoundError`: Se genera cuando se intenta abrir un archivo que no existe.
7. `ImportError`: Se genera cuando se produce un error al importar un módulo.
8. `NameError`: Se genera cuando se utiliza un nombre no definido en el ámbito actual.

Un ejemplo de comu utilizar los diferentes tipos de excepciones es la siguiente: 

```Python
try:
	n1 = int(input("Ingresa primer numero: "))
	linea_de_codigo_sin_sentido

except ValueError as e: 
	print("Ingrese un valor que corresponda")

except NameError as e:
	print("Ocurrio un error")
```

Estos son solo algunos ejemplos de tipos de excepciones en Python. Sin embargo, la biblioteca estándar de Python proporciona muchos más tipos de excepciones para manejar diferentes escenarios y errores específicos.

Es importante conocer los diferentes tipos de excepciones para poder capturar y manejar los errores de manera adecuada. Esto permite proporcionar mensajes de error personalizados, tomar acciones específicas según el tipo de excepción y evitar que el programa se detenga inesperadamente.

Más informacion sobre los [tipos de excepciones](https://docs.python.org/3/library/exceptions.html)
<br>
## <mark class="hltr-red">Else y finally</mark>

Además del bloque `try-except`, también podemos utilizar los bloques `else` y `finally` en conjunción con el bloque `try`. Su funcionamiento es el siguiente:

1. El bloque `else`: Este bloque se ejecuta solo si NO se produce ninguna excepción en el bloque `try`. Es decir, si no se captura ninguna excepción, el código dentro del bloque `else` se ejecutará inmediatamente después de la finalización del bloque `try`. El bloque `else` es opcional y se utiliza para definir el código que deseamos ejecutar en caso de que no se produzcan excepciones.

   Ejemplo:
   ```python
   try:
       # Código que puede generar excepciones
   except SomeException:
       # Manejo de excepción
   else:
       # Código a ejecutar si NO se producen excepciones
   ```

2. El bloque `finally`: Este bloque se ejecuta siempre, independientemente de si se produce una excepción o no en el bloque `try`. Se utiliza para definir el código que queremos que se ejecute sin importar el resultado del bloque `try`. Incluso si se captura una excepción, el bloque `finally` se ejecutará antes de que la excepción se propague o antes de que el programa finalice. El bloque `finally` es opcional y se utiliza para realizar tareas de limpieza o liberación de recursos.

   Ejemplo:
   ```python
   try:
       # Código que puede generar excepciones
   except SomeException:
       # Manejo de excepción
   finally:
       # Código que se ejecuta SIEMPRE, haya o no excepciones
   ```

En resumen, el bloque `else` se ejecuta cuando no se producen excepciones, mientras que el bloque `finally` se ejecuta siempre, independientemente de si se producen excepciones o no. Ambos bloques son opcionales y se utilizan para definir acciones específicas según el resultado del bloque `try`.
<br>
## <mark class="hltr-red">Invocación de funciones</mark>

Es posible invocar excepciones de forma explícita utilizando la declaración `raise`. Al invocar una excepción, se crea una instancia de la excepción especificada y se lanza para interrumpir el flujo normal del programa. Esto se utiliza cuando se desea señalar un error o una situación excepcional que debe ser manejada por el código que está llamando.

La sintaxis básica para invocar una excepción es la siguiente:

```python
raise TipoDeExcepcion("Mensaje de error opcional")
```

Aquí, `TipoDeExcepcion` se refiere al tipo de excepción que deseamos invocar. Puede ser una excepción integrada de Python, como `ValueError` o `TypeError`, o una excepción personalizada que hayamos definido. El mensaje de error opcional es una cadena que proporciona información adicional sobre la excepción.

Por ejemplo, para invocar una excepción `ValueError` con un mensaje de error personalizado, podemos hacer lo siguiente:

```python
raise ValueError("El valor es incorrecto. Debe ser positivo.")
```

Al invocar una excepción, se interrumpe la ejecución normal del programa y se busca un bloque `try-except` que pueda manejar esa excepción en el código circundante. Si no se encuentra un bloque `try-except` adecuado, el programa se detiene y se muestra una traza de error.

Invocar excepciones es útil para señalar errores o situaciones excepcionales específicas en nuestro código y permitir que se manejen adecuadamente en bloques `try-except`. También nos permite personalizar los mensajes de error para brindar información útil al usuario o al programador que está depurando el código.

Un pequeño ejemplo sobre invocar excepciones:
```Python
def division(n=0):
    if n == 0:
        raise ZeroDivisionError("No se puede dividir entre 0", f"{n}")
    return 5 / n
    
try:
    division()

except ZeroDivisionError as e:
    print(e)
```

Primero se define una función llamada `division()` que recibe un argumento `n` con un valor predeterminado de 0. Dentro de la función, hay una verificación condicional para verificar si `n` es igual a 0. Si es así, se lanza una excepción `ZeroDivisionError` con un mensaje de error personalizado y el valor de `n` como información adicional.

Luego, fuera de la función, se utiliza un bloque `try-except` para capturar cualquier excepción `ZeroDivisionError` que se produzca al llamar a la función `division()`. Si se captura una excepción, se asigna a la variable `e`, y luego se imprime el contenido de `e`, que mostrará el mensaje de error personalizado proporcionado al lanzar la excepción.
<br>
## <mark class="hltr-red">Excepciones personalizadas</mark>

Las excepciones personalizadas son excepciones que se definen por el programador para abordar situaciones específicas en su código. Aunque Python proporciona varias excepciones incorporadas, a veces es útil crear nuestras propias excepciones para representar errores o situaciones excepcionales personalizadas.

Para crear una excepción personalizada, normalmente se define una nueva clase que hereda de una de las clases base de excepción de Python, como `Exception` o una de sus subclases. Luego, se pueden agregar atributos y métodos adicionales a la clase para personalizarla según las necesidades del programador.

Por ejemplo, supongamos que estamos creando una aplicación de gestión de archivos y deseamos tener una excepción personalizada para manejar casos en los que se intenta acceder a un archivo que no existe. Podríamos definir nuestra propia excepción llamada `FileNotFoundError` de la siguiente manera:

```python
class FileNotFoundError(Exception):
    def __init__(self, filename):
        self.filename = filename
        super().__init__(f"El archivo '{filename}' no existe.")
```

En este ejemplo, hemos creado una clase `FileNotFoundError` que hereda de la clase base `Exception`. Hemos agregado un método `__init__()` para inicializar la excepción y un atributo `filename` para almacenar el nombre del archivo. Al llamar al constructor de la clase base utilizando `super().__init__()`, podemos proporcionar un mensaje de error personalizado.

Una vez definida la excepción personalizada, se puede utilizar de la misma manera que las excepciones incorporadas de Python. Por ejemplo, podríamos lanzar y capturar la excepción `FileNotFoundError` cuando se intente abrir un archivo inexistente en nuestro código.

Las excepciones personalizadas nos permiten tener un manejo más específico de los errores y proporcionar mensajes de error más descriptivos y significativos para ayudar en la depuración y el mantenimiento del código.