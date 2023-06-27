---
banner_icon: ⛰️
banner_y: 0.268
banner: "![[sts-1-launch_4858568740_o.jpg]]"
---

# Alojamiento de memoria en C

Las variables declaradas como “Globales” dentro del programa se almacenan en posiciones fijas de la memoria, dicha sección es mejor conocida como “Segmento de Datos” del programa. Al ser variables globales sabemos que pueden ser utilizadas por todas las funciones o procedimientos que conforman al programa. Las variables “static” (parecidas a las globales) también se almacenan en posiciones fijas de la memoria, pero solo están disponibles en el módulo o funciones en que están declaradas, también quedan alojadas en el “segmento de datos”. Las variables locales se almacenan en la pila (stack) y existen únicamente mientras están activas las funciones en donde están declaradas. Todas estas variables tienen la característica común de que se definen cuando se compila el programa. Por lo tanto el compilador reserva (define) espacio para almacenar valores de los tipos de datos declarados. En resumen todas estas variables hacen uso de lo que llamaremos <mark class="hltr-red">MEMORIA ESTÁTICA</mark>, de un tamaño especifico y definido en el momento de la compilación.

Pero no siempre se conoce con antelación el espacio que necesitarán algunas variables dentro de nuestro programa y para ello es necesario utilizar la <mark class="hltr-red">MEMORIA DINÁMICA</mark>, que asigna espacios de memoria en el momento de la ejecución en el “montículo” o “montón” (heap). Mediante funciones especiales como: ***malloc(), realloc(), calloc() y free()***. Que asignan y liberan la memoria de una zona denominada “almacén libre”.
Es importante mencionar que todas estas funciones están contenidas dentro de las librerías
**<stdlib.h> y <malloc.h>**

![[estatica_vs_dinamica.png| 650]]

## <mark class="hltr-purple">Punteros en C</mark>

Un puntero es una dirección de memoria, en este caso es la dirección de una variable.

Un puntero es una variable como cualquier otra, por lo tanto cuenta con los atributos como, Nombre, dirección, tipo y valor.

Los apuntadores tienen ciertas reglas: 

- El tipo del apuntador y del valor al que apunta debe ser el mismo.
- Una variable puntero contiene o almacena una dirección que apunta a otra posición en memoria.
- En esa posición se almacenan los datos a los que apunta el puntero.
- Un puntero apunta a una variable de memoria.
- Siempre que aparezca un * en la definición de una variable, es porque se trata de una variable puntero.
- También requieren ser inicializados antes de utilizarlos.
- *El * antes de la variable puntero nos dice “el contenido de”*
- El usar un puntero para obtener al valor al que apunta se conoce como “Indirección el puntero” o “desreferenciar el puntero”.
- Existe el puntero “NULL” (nulo) que no apunta a ninguna parte. Sirve para identificar una
dirección no valida. Se puede definir Null como: #define NULL o (#undef NULL).
- Para el punto anterior se ocupan las librerías: stdio.h, stdlib.h, string.h y stddef.h
- Un puntero genérico es laque al que no se le asigna un tipo de dato especifico. void
Por ejemplo:
void * puntero

![[punteros.png | 650]]

### Función `malloc()`

La función `malloc()` se utiliza para asignar memoria dinámicamente durante el tiempo de ejecución de un programa en C. Su prototipo es el siguiente:

```c
void *malloc(size_t size);
```

La función `malloc()` reserva un bloque de memoria contigua de tamaño `size` bytes y devuelve un puntero al inicio de ese bloque. El tipo de retorno es `void *`, lo que significa que se puede asignar el puntero devuelto a cualquier tipo de puntero en C.

Aquí hay un ejemplo de cómo se puede usar `malloc()` para asignar un bloque de memoria para un arreglo de enteros:

```c
int *arr;
int n = 10;
arr = (int *)malloc(n * sizeof(int));
```

En este ejemplo, se asigna un bloque de memoria para 10 enteros utilizando `malloc()`. La expresión `(int *)` se utiliza para realizar una conversión de tipo explícita, ya que `malloc()` devuelve un puntero genérico `void *`, y aquí se espera un puntero a `int`. La cantidad total de memoria asignada se calcula multiplicando el número de elementos (`n`) por el tamaño de cada elemento (`sizeof(int)`).

Es importante tener en cuenta que la memoria asignada por `malloc()` no está inicializada. Por lo tanto, es posible que los valores almacenados en esa memoria sean basura o indeterminados. Si se requiere que la memoria asignada esté inicializada a un valor predeterminado, se puede utilizar la función `calloc()` en lugar de `malloc()`.

### Función `realloc()`

La función `realloc()` se utiliza para cambiar el tamaño de un bloque de memoria previamente asignado. Su prototipo es el siguiente:

```c
void *realloc(void *ptr, size_t size);
```

La función `realloc()` toma un puntero existente (`ptr`) que apunta a un bloque de memoria previamente asignado y cambia su tamaño a `size` bytes. Devuelve un puntero al inicio del bloque de memoria modificado. Si el tamaño aumenta, el contenido anterior se mantiene y se agregan bytes adicionales al final del bloque. Si el tamaño disminuye, los bytes adicionales al final se liberan.

Aquí hay un ejemplo de cómo se puede usar `realloc()` para cambiar el tamaño de un arreglo dinámico:

```c
int *arr;
int n = 10;
arr = (int *)malloc(n * sizeof(int));

// Cambiar el tamaño del arreglo a 20 enteros
n = 20;
arr = (int *)realloc(arr, n * sizeof(int));
```

En este ejemplo, se asigna inicialmente un bloque de memoria para 10 enteros utilizando `malloc()`. Luego, se utiliza `realloc()` para cambiar el tamaño del bloque a 20 enteros. El puntero devuelto por `realloc()` se asigna nuevamente a `arr`.

Es importante tener en cuenta que la función `realloc()` puede devolver un nuevo puntero si se asigna un bloque de memoria completamente nuevo debido a la falta de espacio contiguo para expandir el bloque existente. Por lo tanto, es una buena práctica asignar el resultado de `realloc()` a un nuevo puntero y verificar si se realizó correctamente antes de descartar el puntero original.