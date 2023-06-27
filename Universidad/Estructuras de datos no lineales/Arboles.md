
## <mark class="hltr-red">Concepto de Árbol</mark>

Un árbol es una **estructura de datos no lineal** **que se utiliza para representar una jerarquía** o estructura de datos similar a un árbol. Está compuesto por nodos y bordes (enlaces), donde cada nodo representa un valor y cada borde representa una relación entre los nodos. El nodo superior se conoce como la raíz del árbol y los nodos inferiores se conocen como nodos secundarios o hijos.

La representación de las estructuras de árbol se basa en nodos y enlaces. Un nodo representa un elemento o valor en la estructura, y puede tener cero o varios hijos, que son otros nodos conectados mediante enlaces. El nodo superior, que no tiene padre, se llama la raíz del árbol.

Cada nodo, excepto la raíz, tiene exactamente un padre, y los nodos con el mismo padre se llaman hermanos. Los nodos que no tienen hijos se llaman hojas. El nivel de un nodo se refiere a la distancia desde la raíz. El nivel de la raíz es cero, y cada nivel adicional corresponde a un paso hacia abajo en el árbol. La profundidad del árbol es el nivel máximo de cualquier nodo en el árbol.

Los árboles se utilizan comúnmente en programación para almacenar y organizar datos jerárquicos, como en la estructura de directorios de un sistema de archivos, en la organización de datos en una base de datos o en la construcción de árboles de decisión en el aprendizaje automático. Existen varios tipos de árboles, como árboles binarios, árboles de búsqueda binarios, árboles AVL, árboles rojos-negros, entre otros. Cada tipo de árbol se utiliza para diferentes fines y tiene diferentes características que lo hacen más adecuado para ciertas situaciones.

### <mark class="hltr-orange">Maneras de representar un árbol</mark>

![[rep_grefica.png]]

![[rep_venn.png]]

![[rep_parentesis.png]]

![[rep_dewey.png]]

![[rep_identacion.png]]

## <mark class="hltr-red">Características</mark>

- Uno de los nodos se distingue de los demás, la raíz.
- Todo árbol que no es vacío tiene un único nodo raíz.
- Un nodo X es descendiente directo de un nodo Y, si el nodo X es apuntado por Y.
    - Se dice que X es hijo de Y.
- Un nodo X es antecesor directo de un Nodo Y, si el nodo X apunta al nodo Y.
    - Se dice que X es padre de Y.
- Todos los nodos descendientes directos (hijos) de un mismo nodo – padre – son hermanos.
- Todo nodo que no tiene ramificaciones (hijos) es terminal u hoja.
- Todo nodo que no es raíz, ni hoja se conoce como **interior**.
- Un árbol con n nodos debe tener **N-1 aristas**.
- Grado es el número de descendientes directos de un nodo determinado.
- **Grado del árbol** es el máximo grado de todos los nodos del árbol.
- Nivel o profundidad es el número de arcos que deben ser recorridos para llegar a un determinado nodo desde la raíz
    - la raíz tiene nivel 0.
- La altura de un nodo es el número de arcos que deben ser recorridos para llegar del nodo hasta la hoja más profunda.
- Altura del árbol es el máximo número de niveles de todos los nodos del árbol o la altura de la raíz.

![[ejemplo_1.png]]

![[ejemplo_2.png]]

![[ejemplo_3.png]]

- I, E, J, K, G y L son nodos terminales u hojas.
- B, D, F y H son nodos interiores.

![[ejemplo_4.png]]

![[ejemplo_5.png]]

## <mark class="hltr-red">Longitudes</mark>

### <mark class="hltr-yellow">Longitud de camino</mark>

![[longitud_camino.png]]

### <mark class="hltr-yellow">Longitud de camino interno</mark>

![[camino_interno.png]]

**LCI = 1 * 1  +  2 * 2  +  5 * 3  +  4 * 4  =  36**

### <mark class="hltr-yellow">Media de la longitud de camino interno</mark>

Simboliza el número de decisiones que se deben tomar en promedio para llegar a un determinado nodo partiendo desde la raíz.

- 𝐿𝐶𝐼𝑀=𝐿𝐶𝐼/𝑛

### <mark class="hltr-yellow">Longitud de camino externo</mark>

Tiene dos conceptos asociados: 

- Árbol extendido:
  - Es aquel que el numero de hijos de cada nodo es igual al grado del árbol. Si algún nodo no cumple esa condición se pueden incorporar nodos especiales. 

- Nodo especial:
  - Tienen el propósito de rellenar remas vacías o nulas, no tienen descendientes y se representan en forma de cuadrado. 

**************Ejemplo**************

![[camino_externo.png]]

**NOTA:** El grado del árbol es de 3 (porque b tiene 3 hijos), entonces todos los nodos se rellenan con nodos especiales para que cada uno tenga 3 hijos.  

![[camino_externo_formula.png]]

**LCE = 1 ∗ 2  +  1 ∗ 3  +  11 ∗ 4  +  12 ∗ 5**