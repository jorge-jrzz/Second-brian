
## <mark class="hltr-green">Introducción</mark>

- Los elementos de un árbol
  - Hasta ahora no han guardado un orden
  - No sirven para buscar elementos
  ![[arbol_general.png]]

- Los árboles de búsqueda
  - Permiten ejecutar en ellos búsqueda binaria.
  - Dado un nodo:
    - Todos los nodos del sub. Izq. Tienen una clave menor que la clave de la raíz.
    - Todos los nodos del sub. Der. Tienen una clave mayor que la clave de la raíz.
    - No pueden haber valores repetidos en el árbol.
    ![[arbol_binario.png]]

## <mark class="hltr-green">Arboles binarios de búsqueda (ABB)
</mark>
  
Para todo nodo T del árbol se debe cumplir que todos los valores almacenados en el subárbol izquierdo de T sean menores o iguales a la información guardada en el nodo T. De forma similar, todos los valores almacenados en el subárbol derecho de T deben ser mayores o iguales a la información guardada en el nodo T.

![[ejemplo_abb.png]]

Estas propiedades aseguran que el árbol esté ordenado de forma que se puedan realizar búsquedas, inserciones y eliminaciones de manera eficiente. Además, permiten aplicar técnicas de ordenamiento como el recorrido Inorden, que devuelve los elementos en orden ascendente. Los árboles binarios de búsqueda se utilizan en muchas aplicaciones, como en la implementación de diccionarios, índices de búsqueda en bases de datos y algoritmos de compresión de datos.

### <mark class="hltr-cyan">Ejemplo de recorrido Inorden en un ABB</mark>

![[inorden_abb.png]]

### <mark class="hltr-cyan">Comentarios importantes</mark>

- El orden de inserción de los datos, determina la forma del ABB
- La forma del ABB determina la eficiencia del proceso de búsqueda
- entre menos altura tenga el ABB, más balanceado estará. y mas eficiente será.
- ¿Qué pasará si se si se insertar los datos de forma ordenada?  

![[abb_desbalanceado.png]]

## <mark class="hltr-green">Búsqueda de un nodo</mark>

![[busqueda_abb.png]]

## <mark class="hltr-green">Eliminación de un nodo</mark>

La operación de eliminación en un árbol binario de búsqueda es un poco más complicada que la de inserción.

Ésta consiste en eliminar un nodo sin violar los principios que definen un árbol binario de búsqueda. Se deben distinguir los siguientes casos:

- Si el elemento a eliminar es terminal o <mark class="hltr-pink">hoja</mark>.
  Simplemente se suprime redefiniendo el puntero del predecesor.
    1. Busca el Nodo Padre del nodo a borrar.
    2. Desconectarlo.
    3. Liberar el nodo.
        ![[eliminar_hoja.png]]

- Si el elemento a eliminar tiene <mark class="hltr-pink">un solo descendiente</mark>.
  Si el elemento a eliminar tiene un solo descendiente, entonces tiene que sustituirse por ese descendiente
    1. Buscar el Nodo Padre del nodo a borrar.
    2. Conectar el hijo con el padre del nodo a borrar.
    3. Liberar el nodo.

        ![[eliminar_nodo_1_hijo.png]]

- Si el elemento a eliminar<mark class="hltr-pink"> tiene dos descendientes</mark>.
  Si el elemento a eliminar tiene dos descendientes, entonces se tiene que sustituir por el nodo que se encuentra mas a al izquierda en el subárbol derecho **o** por el nodo que se encuentra mas a la derecha en el subárbol izquierdo.
    1. Localizar el nodo predecesor o sucesor del nodo a borrar.
      - EL PREDECESOR el “el mayor de los menores”.
      - EL SUCESOR es “el menor de los mayores”.
      - Para la implementación es igual de eficiente programar la búsqueda del predecesor que del sucesor.
    2. El valor del Predecesor (o Sucesor) se copia al nodo a borrar.
    3. Eliminar el nodo del Predecesor (o Sucesor según sea el caso).
    
    ![[eliminacion_2_nodos_S_P.png]]
    
    ![[eliminacion_2_nodos_Suc.png]]
    
    ![[eliminacion_2_nodos_Pred.png]]

## <mark class="hltr-green">Comparativas</mark>

![[arboles_vs_arreglos.png]]

![[arboles_vs_listas.png]]