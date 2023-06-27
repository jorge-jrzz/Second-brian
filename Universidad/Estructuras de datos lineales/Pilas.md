---
banner_icon: 🍕
banner: "![[international-space-station_15357921727_o.jpg]]"
banner_y: 0.42
---
# Pilas

Las pilas son estructuras de datos que se comportan como una lista, pero donde solo se pueden realizar inserciones y eliminaciones en un extremo llamado "tope". Este comportamiento se conoce como "Last In, First Out" (LIFO).

La implementación de una pila en C puede ser estática o dinámica. La implementación estática requiere que se defina el tamaño máximo de la pila antes de su uso, mientras que en la implementación dinámica, el tamaño se ajusta dinámicamente durante la ejecución del programa.

A continuación, se describen las funciones básicas para una implementación de pila dinámica en C:

- ### Básicas:
> - New(): Operación para crear una nueva pila.
> - Push(): Agregar o introducir un elemento por la cima actualizando el nuevo valor del tope.
> - Pop(): Elimina el elemento que se encuentra en la cima o tope y decrementa o actualiza el tope al nuevo elemento que esta en el tope.
> - isEmtpy(): Operación que da una respuesta booleana indicando el estado de la pila, dando verdadero cuando la pila está vacía y falso en caso contrario.
> - isFull(): Operación que solo es para pilas estáticas, es opuesta a isEmpty, esta operación también da una respuesta booleana dando un verdadero en caso de que la pila este llena y falso en caso contrario. Count(): Esta operación nos indica la cantidad de elementos contenidos en la pila.

- ### Complementarias:
> - Count(): Esta operación nos indica la cantidad elementos contenidos en la Pila.
> - Tipo_dato(): Esta operación como su nombre nos indica el tipo de dato que se almacena en la pila.
> - Limpiar_pila(): Esta operación quita todos los elementos de la pila y la deja vacía.
> - Cima(): Esta operación nos indica que elemento es el que se encuentra en el tope o en la cima de la pila. Siempre y cuando haya elementos, en otro caso apuntara a NULL.

```c
#include <stdio.h>
#include <stdlib.h>

// Estructura para un nodo de la pila
struct Nodo {
    int dato;
    struct Nodo *siguiente;
};

// Puntero al tope de la pila
struct Nodo *tope = NULL;

// Función para insertar un elemento en la pila
void push(int x) {
    struct Nodo *nuevo;
    nuevo = (struct Nodo *)malloc(sizeof(struct Nodo));
    nuevo->dato = x;
    nuevo->siguiente = tope;
    tope = nuevo;
}

// Función para eliminar un elemento de la pila
void pop() {
    struct Nodo *aux;
    if (tope == NULL) {
        printf("La pila está vacía\\n");
        return;
    }
    aux = tope;
    tope = tope->siguiente;
    free(aux);
}

// Función para obtener el elemento del tope de la pila
int peek() {
    if (tope == NULL) {
        printf("La pila está vacía\\n");
        return -1;
    }
    return tope->dato;
}

// Función para imprimir la pila
void imprimirPila() {
    struct Nodo *aux;
    aux = tope;
    while (aux != NULL) {
        printf("%d\\n", aux->dato);
        aux = aux->siguiente;
    }
}
```

En resumen, las pilas son estructuras de datos útiles para realizar tareas que requieren un comportamiento LIFO. La implementación en C puede ser estática o dinámica, y las funciones básicas incluyen insertar, eliminar, obtener el elemento del tope y imprimir la pila.