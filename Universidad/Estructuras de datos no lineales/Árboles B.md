## Por que árboles B
+ Rara vez va a caber el contenido de un árbol binario en memoria  
+ Lo normal en estos casos es mantener el 'árbol en memoria secundaria (HDD) y cargarlo parcialmente 
+ La memoria secundaria es lenta, por lo que interesa reducir el número de accesos a memoria secundaria

## arboles B
+ Cuando el rendimiento en la velocidad del acceso a datos es un problema, los arboles B son recomendados a los árboles binarios normales.
+ Ejemplo; 
	+ Una base de datos debe funcionar lo más rápido posible.
	+ Hay que minimizar los accesos IO todo lo posible del mismo tiempo que las búsquedas debes ser rápidas. 

## Planteamiento
+ En un nodo de árbol B hay un número mayor de clases (K) y de hijos (C).

### Ventaja aparente
+ Aumenta el factor de ramificación del árbol
+ En un árbol binario, a partir de un nodo podemos pasar a dos hijos como máximo
+ En un árbol B, el numero de hijos a los que podemos viajar a partir de un nodo es mucho mayor

## Propiedades
*Mismas palabras , distintos significados*
+ La definición de un árbol B siempre ha estado sujeta a ambigüedades
+ Varios autores han intentado cambiar las definiciones a lo largo del tiempo para evitar esto 
+ 1972 (Bayer) - 1992 (Flok) - **1998 (Knut)**

### Grado
- El numero máximo de hijos que puede tener el nodo de un árbol B
- Puesto que un nodo con K claves tiene C+1 hijos:
	- Un árbol B de grado M puede tener M hijos
	- Un árbol B de grado M puede tener M - 1 claves. 

#### Numero mínimo de hijos
- Un árbol de grado M con M hijos y M - 1 claves.
- Los grados deben tener al menos M/2hijos (o M/2 - 1 claves). El redondeo siempre se hace hacia arriba (función ceil).
- Hay una excepción: la raíz, que puede tener menos hijos de lo obligado

## Operaciones
+ Búsqueda 
+ Inserción 
+ Borrado
+ Recorrido
+ ¿Este?
+ . . .
+ Dividir
	+ Ocurre cuando intentamos agregar elementos a un nodo que ya esta lleno
	+ Hace falta reestructurar el árbol o el subárbol para que se puedan insertar elementos en él
+ Reestructurar
	+ Al borrar un nodo también tenemos que tener en cuenta las propiedades de un árbol
	+ Por ejemplo, si borramos un nodo, debemos asegurarnos de que ningún nodo se encuentre debajo del limite 
	+ De ser así deberemos reestructurar de nuevo el árbol.