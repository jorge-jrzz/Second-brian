---
banner_icon: ⚔️
banner: "![[the-mercury-7_15258556433_o.jpg]]"
banner_y: 0.18
---
# Listas enlazadas

Pueden ser estáticas cuya creación se basa en el uso de arreglos; o dinámicas lo cual requiere la manipulación de memoria y todo lo que eso implica. Existen 4 tipos de listas de acuerdo a los punteros que la conforman:

#### - Listas enlazadas simples 
#### - Listas simplemente enlazadas
#### - Listas ligadas simples
#### - Listas simplemente ligadas.

Listas enlazadas simples son aquellas que cuentan con un único puntero hacia el siguiente nodo. Más su campo de información o datos. Por comodidad en las siguientes definiciones obviaremos este campo ya que todas las listas y en general las estructuras cuentan con el. Dicho campo puede ser de cualquier tipo de dato simple o compuesto. La lista es únicamente eficiente en el recorrido simple hacia adelante, que es el único sentido permitido.

![[lista_simple.png | 600]]

### Listas doblemente enlazadas, doblemente ligadas o listas dobles

Con dos punteros uno hacia el nodo siguiente y otro hacia el nodo anterior. Listas doblemente enlazadas, doblemente ligadas o listas dobles. Eficiente en recorrido directo (hacia adelante) y recorrido inverso (hacia atrás).

![[lista_doble.png | 600]]

### Listas circular simple o lista circular simplemente

Con un único puntero hacia el nodo siguiente y el puntero del nodo final apunta al primer nodo. La lista puede ser recorrida circularmente o en anillo.

![[lista_circular.png | 600]]

### Listas circulares doblemente enlazadas

Con dos punteros, uno apuntando al nodo siguiente y otro al nodo anterior, de igual forma el puntero siguiente del ultimo nodo apunta al primer nodo y el puntero anterior del primer nodo apunta al último elemento. La lista se puede recorrer en ambos sentidos en dirección directa (hacia delante), como en dirección inversa (hacia atrás), en forma de anillo.

![[lista_circular_doble.png | 600]]

