
---
banner_icon: 🤖
banner: "![[viking-2-image-of-mars-utopian-plain_7651153704_o.jpg]]"
banner_y: 0.38
---

# Java Virtual Machine

La **JVM** (Java Virtual Machine) es una parte fundamental del entorno de ejecución de Java. Es una máquina virtual que interpreta y ejecuta el código Java compilado, conocido como bytecode. Proporciona un entorno de ejecución independiente de la plataforma, lo que significa que el mismo bytecode Java se puede ejecutar en diferentes sistemas operativos y arquitecturas de hardware sin necesidad de realizar cambios en el código fuente.

Cuando se compila un programa Java, el compilador genera un archivo con extensión `.class` que contiene el bytecode Java. Este bytecode no se ejecuta directamente en el sistema operativo, sino que se carga y se ejecuta en la JVM. La JVM actúa como una capa de abstracción entre el código Java y el sistema subyacente.

Cuando se inicia un programa Java, se crea una instancia de la JVM en la máquina donde se va a ejecutar. La JVM carga y verifica el bytecode, realiza la gestión de memoria, realiza la optimización del código, y proporciona otros servicios necesarios para la ejecución del programa. Esto permite que el código Java se ejecute de manera eficiente y segura.

La JVM se compone de varios componentes, incluyendo:

1. **Class Loader**: Es responsable de cargar las clases en tiempo de ejecución. Se encarga de buscar, cargar y vincular las clases necesarias para ejecutar el programa.

2. **Runtime Data Area**: Es el área de memoria donde se almacenan datos durante la ejecución del programa. Se divide en varias secciones, como el método de área, el área de pila, el área de montón, etc.

3. **Execution Engine**: Es el motor de ejecución de la JVM. Interpreta y ejecuta el bytecode Java. Puede utilizar diferentes enfoques para mejorar el rendimiento, como la compilación just-in-time (JIT), que traduce partes del bytecode en código nativo para una ejecución más rápida.

4. **Garbage Collector**: Es responsable de administrar la memoria y liberar los objetos que ya no son utilizados. Detecta los objetos que no tienen referencias válidas y los elimina automáticamente, liberando así la memoria ocupada por esos objetos.

En resumen, la JVM proporciona un entorno de ejecución seguro y portátil para los programas Java. Permite escribir código Java una vez y ejecutarlo en diferentes plataformas sin preocuparse por los detalles específicos del sistema operativo o la arquitectura de hardware. La JVM se encarga de la gestión de memoria, la carga de clases y la ejecución del bytecode Java, lo que hace posible el funcionamiento del lenguaje Java en una amplia variedad de dispositivos y sistemas operativos.

![[JVM.png| 600]]

Ejemplo del funcionamiento de la JAva Virtual Machine:
![[Example_JVM.png| 650]]
La JVM admite una gran cantidad de lenguajes de programación, como Kotlin, Groovy, Scala y Clojure, junto con JRuby y Jython; mas información relacionada con Jython: [[Introducción]].

![[Lenguajes_JVM.png| 650]]

### Historia

La **JVM** (Java Virtual Machine) fue desarrollada por primera vez por Sun Microsystems (ahora Oracle Corporation) en la década de 1990 como parte del lenguaje de programación Java. Fue creada con el objetivo de proporcionar una plataforma de ejecución portátil y segura para las aplicaciones Java.
El diseño de la JVM se basó en gran medida en la máquina virtual P-Code propuesta para el lenguaje de programación Pascal en la década de 1970. James Gosling, Mike Sheridan y Patrick Naughton lideraron el equipo de desarrollo de la JVM en Sun Microsystems, y su trabajo sentó las bases para la tecnología que ha evolucionado desde entonces.
La versión inicial de la JVM fue lanzada junto con la primera versión pública de Java en 1995. Desde entonces, la JVM ha evolucionado y ha sido objeto de varias mejoras y actualizaciones. Oracle Corporation ha sido el principal responsable del desarrollo y mantenimiento de la JVM desde que adquirió Sun Microsystems en 2010.
A lo largo de los años, se han introducido mejoras significativas en la JVM, como el uso de la compilación just-in-time (JIT), que mejora el rendimiento al traducir partes del bytecode en código nativo en tiempo de ejecución. También se han realizado mejoras en la gestión de memoria, el recolector de basura y la optimización del código.
Además, la JVM ha sido adoptada por otras implementaciones y proyectos relacionados con Java, como OpenJDK y la comunidad Java. Esto ha permitido una mayor colaboración y desarrollo de la JVM, con contribuciones y mejoras de diferentes partes interesadas.

En resumen, la JVM ha sido una parte integral del ecosistema de Java desde sus primeros días y ha sido clave para el éxito y la popularidad del lenguaje. Ha evolucionado a lo largo de los años para brindar un entorno de ejecución eficiente, seguro y portátil para las aplicaciones Java en una amplia variedad de plataformas y sistemas operativos.

### Preguntas:

+ ==¿Cuál es el mayor beneficio de la máquina virtual de Java (JVM)?==
	Ejecutar el código independientemente del sistema operativo, en el mundo Java siempre tendremos el mismo archivo "ejecutable" (Bytecode) que será ejecutado por la máquina virtual de Java (JVM) independientemente del sistema operativo estemos usando. De esta forma, no es necesario reescribir el código o adaptarlo a cada sistema operativo. ¡Tenemos un único ejecutable para todas las plataformas!

+ ==¿Cuál es la diferencia entre archivos ejecutables de Windows (.exe) y archivos ejecutables de Java (Bytecode)?==
	1. Los ejecutables de Windows pueden correr directamente en el sistema operativo, los de Java necesitan de la máquina virtual. Los programas escritos en Java necesitan de la máquina virtual para ser ejecutados.
	2. Los archivos ejecutables de Java son portátiles, los de Windows no. Recuerda que la palabra "portátil" se refiere a que el mismo archivo puede ser ejecutado en varios sistemas operativos (Windows, Linux, Mac, etc.).

---

- #JVM