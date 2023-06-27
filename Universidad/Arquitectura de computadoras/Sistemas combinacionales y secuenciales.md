---
banner_icon: 🐬
banner: "![[atlantis-docked-to-mir_9461048636_o.jpg]]"
---

# Sistemas Combinacionales y Secuenciales

Los sistemas digitales se pueden clasificar en sistemas combinacionales y sistemas secuenciales, dependiendo de cómo se procesan y almacenan los datos.

## Sistemas Combinacionales

Los sistemas combinacionales son aquellos en los que la salida en cualquier momento depende únicamente de las entradas presentes en ese mismo instante, sin considerar ningún estado pasado. No hay elementos de almacenamiento de datos en estos sistemas.

### Unidad Aritmética Lógica (ALU)

La Unidad Aritmética Lógica (ALU) es un componente clave en un sistema combinacional. Realiza operaciones aritméticas y lógicas, como sumas, restas, multiplicaciones, operaciones booleanas (AND, OR, XOR, NOT) y desplazamientos de bits. La ALU toma las entradas, realiza las operaciones requeridas y produce la salida correspondiente.

### Unidad de Multiplicación

La Unidad de Multiplicación es un componente específico en un sistema combinacional que se utiliza para realizar operaciones de multiplicación entre dos números. Puede ser diseñada para multiplicaciones de números enteros o de punto flotante. La unidad de multiplicación toma los operandos de entrada y realiza las operaciones necesarias para producir el resultado de la multiplicación.

## Sistemas Secuenciales

Los sistemas secuenciales son aquellos en los que la salida en cualquier momento depende de las entradas presentes y de los estados anteriores del sistema. Estos sistemas utilizan elementos de almacenamiento, como biestables (flip-flops), para retener información y mantener un estado interno.

### Máquinas de Estado Algorítmico (ASM)

Las Máquinas de Estado Algorítmico (ASM) son una forma de diseño de sistemas secuenciales. Utilizan una combinación de lógica combinacional y elementos de memoria para implementar un conjunto de estados y transiciones que representan un algoritmo específico. Cada estado representa una condición o acción particular, y las transiciones entre estados determinan cómo cambia el sistema en respuesta a las entradas.

Las ASM se modelan mediante diagramas de estados, tablas de estados o diagramas de transición de estados, y se implementan utilizando elementos de memoria, como biestables, y lógica combinacional para controlar las transiciones entre estados.

### Unidad de Control

La Unidad de Control es un componente esencial en un sistema secuencial. Es responsable de controlar y coordinar las operaciones de los componentes del sistema, como la ALU, la unidad de multiplicación y otros elementos. La Unidad de Control interpreta las instrucciones del programa almacenadas en la memoria y genera las señales de control necesarias para realizar las operaciones adecuadas en cada ciclo de reloj.

La Unidad de Control se basa en un diseño de máquina de estados para gestionar las diferentes etapas de ejecución de una instrucción, como buscar, decodificar, ejecutar y almacenar resultados.

## Conclusiones

Los sistemas combinacionales y secuenciales son componentes fundamentales en el diseño de sistemas digitales. Los sistemas combinacionales se basan en la lógica combinacional y son útiles para realizar operaciones inmediatas, mientras que los sistemas secuenciales utilizan elementos de memoria y máquinas de estado para retener información y procesarla en función del estado interno del sistema.

La Unidad Aritmética Lógica (ALU) y la Unidad de Multiplicación son componentes comunes en los sistemas combinacionales, mientras que las Máquinas de Estado Algorítmico (ASM) y la Unidad de Control son características clave de los sistemas secuenciales.