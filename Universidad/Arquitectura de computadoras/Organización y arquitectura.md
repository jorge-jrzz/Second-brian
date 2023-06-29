---
banner_icon: 📝
banner: "![[ladee_8981695928_o.jpg]]"
banner_y: 0.324
---

# Organización y arquitectura de computadoras.

La organización y arquitectura de computadoras es el estudio de los principios fundamentales que gobiernan el diseño de sistemas de computadoras. Esta disciplina abarca desde los componentes básicos de una computadora hasta la interconexión de subsistemas y el rendimiento general del sistema. 

## Estructura Básica de una Computadora

Una computadora típica consta de los siguientes componentes principales:

1. **Unidad Central de Procesamiento (CPU)**: Es el cerebro de la computadora y se encarga de ejecutar instrucciones. La CPU contiene la **Unidad de Control** (que interpreta y coordina las operaciones del sistema) y la **Unidad de Procesamiento** (que realiza las operaciones aritméticas y lógicas).

2. **Memoria Principal**: Es el almacenamiento de acceso aleatorio (RAM) utilizado para almacenar datos e instrucciones que la CPU necesita para realizar operaciones. La memoria principal es volátil y se borra cuando se apaga la computadora.

3. **Dispositivos de Entrada**: Permiten a los usuarios ingresar datos o comandos a la computadora. Algunos ejemplos comunes incluyen el teclado, el mouse y los sensores de entrada.

4. **Dispositivos de Salida**: Muestran los resultados del procesamiento de la computadora. Ejemplos de dispositivos de salida son el monitor, la impresora y los altavoces.

5. **Dispositivos de Almacenamiento**: Se utilizan para almacenar datos a largo plazo. Esto incluye discos duros, unidades de estado sólido (SSD) y dispositivos de almacenamiento externos como unidades USB.

## Diferencia entre arquitectura y organización.

#### Arquitectura de computadoras: 
La arquitectura de computadoras se refiere al diseño conceptual y estructural de un sistema informático, incluyendo la forma en que los diferentes componentes interactúan entre sí y cómo se organizan para realizar tareas específicas. Esto incluye aspectos como el conjunto de instrucciones (instruction set), la estructura y organización de la memoria, la jerarquía de almacenamiento, el modelo de ejecución y la interconexión de los componentes principales, como la unidad central de procesamiento (CPU), la memoria, los dispositivos de entrada y salida, entre otros. La arquitectura de computadoras establece las bases para el funcionamiento de los sistemas informáticos y determina su capacidad de procesamiento, rendimiento, eficiencia energética, entre otros aspectos.

#### Organización de computadoras:
La organización de computadoras se refiere a la forma en que se implementa la arquitectura de un sistema informático. Se ocupa de los detalles prácticos de cómo se construye y se interconecta físicamente el hardware para ejecutar las operaciones definidas en la arquitectura. Esto incluye aspectos como la selección de componentes específicos, la elección de tecnologías de interconexión, el diseño de circuitos electrónicos, el esquema de direccionamiento de memoria, la gestión de interrupciones y otros aspectos relacionados con la implementación física del sistema informático. La organización de computadoras se centra en traducir los conceptos abstractos de la arquitectura en una implementación tangible y funcional.

En resumen, ==la arquitectura de computadoras se refiere a la estructura y diseño conceptual de un sistema informático, mientras que la organización de computadoras se enfoca en la implementación física y práctica de esa arquitectura.==

## Arquitectura de Von Neumann

La arquitectura de Von Neumann es un modelo fundamental para el diseño de computadoras. Sus características principales son:

- **Unidad de Control**: Coordina las operaciones de la computadora, interpreta instrucciones y controla el flujo de datos entre la memoria y la unidad de procesamiento.

- **Unidad de Procesamiento**: Realiza operaciones aritméticas y lógicas utilizando los datos de la memoria.

- **Memoria**: Almacena tanto datos como instrucciones en una estructura de acceso aleatorio. La memoria se divide en celdas numeradas, y cada celda tiene una dirección única.

- **Unidad de Entrada/Salida**: Se comunica con dispositivos de entrada/salida para transferir datos entre la computadora y el mundo exterior.

La arquitectura de Von Neumann permite que<mark class="hltr-yellow"> las instrucciones y los datos se almacenen en la misma memoria y se procesen de forma secuencial.</mark> Esto significa que las instrucciones se ejecutan una tras otra, lo que proporciona una base para el funcionamiento de las computadoras modernas.

## Arquitectura Harvard

La arquitectura Harvard es un modelo alternativo a la arquitectura de Von Neumann. A diferencia de esta última, la arquitectura Harvard <mark class="hltr-yellow">utiliza buses de datos y memoria separados para las instrucciones y los datos.</mark> Sus características principales son:

- **Memoria de Programa**: Almacena las instrucciones del programa en una memoria separada llamada **Memoria de Instrucciones**. Esta memoria es de solo lectura y permite un acceso rápido y eficiente a las instrucciones.

- **Memoria de Datos**: Almacena los datos utilizados por el programa en una memoria separada llamada **Memoria de Datos**. Esta memoria puede ser de lectura y escritura, y permite el almacenamiento y la recuperación de datos.

- **Unidad de Control**: Coordina la ejecución del programa y controla el flujo de instrucciones desde la Memoria de Instrucciones hacia la Unidad de Procesamiento.

- **Unidad de Procesamiento**: Realiza las operaciones aritméticas y lógicas utilizando los datos provenientes de la Memoria de Datos. A diferencia de la arquitectura de Von Neumann, la arquitectura Harvard puede realizar simultáneamente una operación de lectura de instrucción y una operación de lectura/escritura de datos.

- **Buses Separados**: La arquitectura Harvard utiliza buses separados para el transporte de datos e instrucciones. Esto permite un acceso paralelo a la memoria de instrucciones y a la memoria de datos, lo que puede mejorar el rendimiento en determinadas situaciones.

La principal ventaja de la arquitectura Harvard radica en su capacidad para ejecutar instrucciones y acceder a datos simultáneamente, lo que puede aumentar la velocidad de procesamiento en comparación con la arquitectura de Von Neumann. Sin embargo, esta ventaja se ve limitada por la necesidad de mantener dos memorias separadas, lo que puede aumentar el costo y la complejidad del sistema.

Es importante destacar que tanto la arquitectura de Von Neumann como la arquitectura Harvard han sido ampliamente utilizadas en el diseño de computadoras y cada una tiene sus propias ventajas y desventajas. La elección entre ellas depende de los requisitos y restricciones específicas del sistema a diseñar.

