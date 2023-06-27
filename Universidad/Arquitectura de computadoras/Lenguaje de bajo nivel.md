---
banner_icon: 🗜️
banner: "![[long-shadows-on-the-lunar-surface_9460175770_o.jpg]]"
banner_y: 0.268
---

#  Lenguaje de bajo nivel (ensamblador).

El lenguaje de bajo nivel conocido como ensamblador es un lenguaje de programación que se sitúa entre el código máquina y los lenguajes de alto nivel. En las computadoras personales, el ensamblador se utiliza para escribir programas directamente entendibles por el procesador.

## Modos de Direccionamiento

Los modos de direccionamiento en el ensamblador determinan cómo se acceden y manipulan los datos en memoria. Algunos modos comunes incluyen:

- **Inmediato**: Los datos se especifican directamente en la instrucción. Por ejemplo: `MOV AX, 10h` (mueve el valor 10h al registro AX).

- **Directo**: La dirección de memoria se especifica directamente en la instrucción. Por ejemplo: `MOV AX, [1000h]` (mueve el valor almacenado en la dirección de memoria 1000h al registro AX).

- **Indirecto**: La dirección de memoria se encuentra en un registro. Por ejemplo: `MOV AX, [BX]` (mueve el valor almacenado en la dirección apuntada por el registro BX al registro AX).

- **Relativo**: La dirección de memoria es relativa a la posición actual del programa. Por ejemplo: `JMP ETIQUETA` (realiza un salto a la etiqueta especificada).

Cada modo de direccionamiento tiene sus propias ventajas y desventajas, y se utilizan en diferentes situaciones dependiendo de los requisitos del programa.

## Instrucciones de Control de Flujo

Las instrucciones de control de flujo en el ensamblador permiten tomar decisiones y controlar el flujo de ejecución del programa. Algunas instrucciones comunes son:

- **Saltos Condicionales**: Permiten realizar un salto a una ubicación específica en función de una condición. Por ejemplo: `JZ ETIQUETA` (salta a la etiqueta si la bandera de cero está activa).

- **Saltos Incondicionales**: Realizan un salto a una ubicación específica sin ninguna condición. Por ejemplo: `JMP ETIQUETA` (realiza un salto incondicional a la etiqueta especificada).

- **Bifurcaciones**: Permiten realizar bifurcaciones condicionales en función de una condición. Por ejemplo: `CMP AX, BX` (compara los registros AX y BX) seguido de `JE ETIQUETA` (salta a la etiqueta si los registros son iguales).

Estas instrucciones de control de flujo permiten crear estructuras de control, como bucles y condiciones, en los programas escritos en ensamblador.

## Subrutinas y Paso de Parámetros

Las subrutinas en ensamblador son bloques de código que se pueden llamar desde diferentes partes del programa. Se utilizan para realizar tareas específicas y modularizar el código. El paso de parámetros a las subrutinas se realiza a través de registros o de la pila.

- **Registros**: Los parámetros se pasan a través de registros específicos. Por ejemplo: `MOV

 AX, 10h` seguido de `CALL SUBRUTINA` (llama a la subrutina y el valor de AX se puede utilizar dentro de ella).

- **Pila**: Los parámetros se empujan en la pila antes de llamar a la subrutina y se extraen dentro de la subrutina. Por ejemplo: `PUSH 10h` seguido de `CALL SUBRUTINA` (llama a la subrutina y el valor se extrae de la pila dentro de ella).

El uso de subrutinas y el paso de parámetros permiten reutilizar código y mejorar la modularidad de los programas escritos en ensamblador.

## Registros de Propósito Especial

Además de los registros generales, los microprocesadores suelen tener registros de propósito especial que tienen funciones específicas en el funcionamiento del procesador. Algunos ejemplos comunes son:

- **Registro de Estado**: Almacena banderas o indicadores de estado que reflejan el resultado de operaciones aritméticas o lógicas anteriores, como bandera de cero, de desbordamiento, de signo, etc.

- **Contador de Instrucciones**: Mantiene la dirección de memoria de la instrucción actualmente en ejecución.

- **Registro de Pila**: Almacena la dirección de memoria actual de la pila, utilizada para almacenar y recuperar datos temporalmente.

## Interrupciones

Las interrupciones son señales que pueden ser generadas por dispositivos externos o eventos internos que requieren la atención inmediata del procesador. El procesador puede suspender la ejecución actual, guardar su estado y atender la interrupción correspondiente. Algunos tipos comunes de interrupciones son:

- **Interrupciones Externas**: Generadas por dispositivos periféricos, como teclado, mouse, temporizadores, etc.

- **Interrupciones de Software**: Provocadas por instrucciones especiales en el programa para solicitar servicios del sistema operativo, como lectura de archivos, impresión, etc.

- **Interrupciones de Error**: Indican condiciones de error como división por cero, desbordamiento de capacidad, violación de acceso a memoria, etc.

## Conjunto de Instrucciones

Cada microprocesador tiene su propio conjunto de instrucciones, que determina las operaciones que puede realizar y cómo se codifican. Estas instrucciones pueden incluir operaciones aritméticas, lógicas, de transferencia de datos, de manipulación de memoria y de control de flujo. El conjunto de instrucciones puede variar entre diferentes arquitecturas de microprocesadores, como x86, ARM, MIPS, etc.

## Programación a Nivel de Bits

El lenguaje de ensamblador permite programar a un nivel muy bajo, directamente manipulando los bits y registros del procesador. Esto proporciona un control preciso sobre el hardware y permite optimizar el rendimiento en situaciones específicas. Sin embargo, también requiere un conocimiento profundo del hardware y puede ser más propenso a errores y difícil de mantener.

Es importante destacar que la programación en ensamblador se utiliza generalmente en situaciones donde se requiere un control máximo del hardware o cuando se necesita una optimización de rendimiento muy específica. En la mayoría de los casos, el uso de lenguajes de programación de alto nivel es más conveniente y legible.

## Conclusiones

El lenguaje de bajo nivel del ensamblador en computadoras personales proporciona un mayor control y precisión en la programación del hardware. Los modos de direccionamiento permiten acceder y manipular datos en memoria, las instrucciones de control de flujo controlan el flujo de ejecución del programa y las subrutinas con paso de parámetros permiten modularizar el código y reutilizarlo.