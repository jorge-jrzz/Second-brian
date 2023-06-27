Un árbol ordenado es aquel en el cual la distribución de las ramas sigue un cierto orden. son de gran interés los arboles ordenados de grado 2 por sus aplicaciones, estos se denominan arboles binarios.

* En un árbol binario se pueden tener como máximo dos subárboles:
  - Subárbol izquierdo.
  - Subárbol derecho.

## <mark class="hltr-purple">Definición formal</mark>

Formalmente se define un árbol binario tipo T como una estructura homogénea, resultado de la concatenación de un elemento llamado raíz con dos arboles binario disjuntos, llamados subárbol izquierdo y subárbol derecho, Un árbol binario especial es el árbol vacío.
Una de las aplicaciones de los arboles binarios podría ser los arboles de decisiones.  

![[arbol_binario_similar.png]]
<br>

## <mark class="hltr-purple">Árbol binario completo</mark>

Un árbol binario completo (ABC) se define como un árbol en el que todos los nodos, menos el último nivel, tienen dos hijos: el subárbol izquierdo y el subárbol derecho.

![[arbol_binario_completo.png]]

### <mark class="hltr-pink">Numero de nodos en un árbol completo</mark>

El numero de un árbol binario completo de altura h se puede calcular mediante la siguiente formula:
![[numero_nodos.png]]
Por ejemplo:
- Un árbol binario completo de altura 4 tendrá 31 nodos.
- Un árbol binario completo de altura 8 tendrá 511 nodos.
- Un árbol binario completo de altura 16 tendrá 131,071 nodos.

## <mark class="hltr-purple">Representación en memoria</mark>

Un nodo de un árbol binario se representa como un registro, con tres campos:

![[representacion_memoria.png]]

- Izq - Es el campo donde se almacena la dirección del subárbol izquierdo del nodo T.
- Info - Representa el campo donde se almacena la información. Puedan ser valores simples o primitivos, u otros objetos.
- Der - Es el campo donde se almacena la dirección del subárbol derecho del nodo T.

## <mark class="hltr-purple">Recorridos</mark>

Recorrer significa visitar los nodos de un árbol de forma ordenada, de modo que los nodos sólo sean visitados una vez. Existen tres formas recursivas de visitar un árbol:

#### <mark class="hltr-cyan">Preorden</mark>
  1. Visitar la raíz
  2. Recorrer el subárbol izquierdo
  3. Recorrer el subárbol derecho

#### <mark class="hltr-cyan">Inorden</mark>
  1. Recorrer el subárbol izquierdo
  2. Visitar la raíz
  3. Recorrer el subárbol derecho.

#### <mark class="hltr-cyan">Posorden</mark>
  1. Recorrer el subárbol izquierdo
  2. Recorrer el subárbol derecho.
  3. Visitar la raíz.


![[recorridos.png]]