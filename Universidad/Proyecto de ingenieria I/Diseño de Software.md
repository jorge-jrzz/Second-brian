### Concepto

El diseño es el primer paso de la fase de desarrollo de cualquier producto o sistema de ingeniería; y puede definirse como: 

> El proceso de aplicar distintas técnicas y principios con el propósito de definir un dispositivo, proceso o sistema con los suficientes detalles como para permitir su realización.

### <mark class="hltr-red">Diseño en el contexto de la ingeniería de software</mark>

- #### <mark class="hltr-orange">Diseño de datos.</mark>
    Transforma el modelo del campo de información (las clases creadas durante el análisis), en las estructuras de datos que se van a requerir para implementar el software.
    Se refiere al proceso de definir la estructura y organización de los datos que serán utilizados en una aplicación de software. Esto implica la identificación de las entidades relevantes, sus atributos y las relaciones entre ellas, así como la definición de las reglas de negocio que gobiernan la manipulación de esos datos.
    ![[diseño_datos.png]]

- #### <mark class="hltr-orange">Diseño arquitectónico.</mark>
    Se refiere al proceso de definir la estructura general y los componentes de un sistema de software, así como sus interacciones y relaciones. El diseño arquitectónico es crucial en la creación de sistemas de software que sean escalables, mantenibles, seguros y que cumplan con los requisitos del negocio.
    
    Define las relaciones entre los principales elementos de la estructura del software, estilos y patrones de diseño de la arquitectura.
    ![[diseño_arquitectonico.png]]
    El diseño arquitectónico se realiza mediante herramientas y técnicas específicas, como el modelado de arquitectura, la documentación y el prototipado. El modelado de arquitectura implica la creación de diagramas que representan la estructura y relaciones entre los componentes del sistema, mientras que la documentación permite que otros desarrolladores comprendan el diseño y la lógica detrás del sistema. El prototipado, por su parte, ayuda a validar y refinar el diseño antes de la implementación.
  
- #### <mark class="hltr-orange">Diseño de la interfaz.</mark>
    Describe la forma en la que el software se comunica con los sistemas que interactúan con el y con los humanos que lo utilizan. 
    ![[diseño_interfaz.png]]
    El diseño de interfaz se enfoca en la creación de una experiencia de usuario atractiva, fácil de usar y eficiente. Esto incluye decisiones sobre la disposición de los elementos en la pantalla, el uso de colores y tipografía, la navegación y la interacción con el usuario.

- #### <mark class="hltr-orange">Diseño en el nivel de componente.</mark>
    Transforma los elementos estructurales de la arquitectura del software en una descripción de sus componentes en cuanto procedimiento.
    ![[diseño_componente.png]]
    El diseño a nivel de componente se enfoca en la creación de componentes reutilizables y escalables. Esto incluye decisiones sobre cómo dividir la funcionalidad en diferentes componentes, cómo definir las interfaces de los componentes y cómo gestionar las dependencias entre ellos. 
    Esto ayuda a garantizar una arquitectura de software bien estructurada, fácil de mantener y evolucionar a medida que se agregan nuevas funcionalidades o se realizan cambios en los requisitos.


### <mark class="hltr-red">Diseño y calidad de software</mark>
- El diseño deberá implementar todos los requisitos explícitos del modelo de análisis, y deberán ajustarse a todos los requisitos implícitos que desea el cliente;
- El diseño deberá ser una guía legible y comprensible para aquellos que generan código y para aquellos que comprueban y consecuentemente, dan soporte al software.
- El diseño deberá proporcionar una imagen completa del software, enfrentándose a los dominios de comportamiento, funcionales y de datos desde una perspectiva de implementación.

### <mark class="hltr-red">Atributos de calidad</mark>

![[atributos_calidad.png]]

- ##### <mark class="hltr-yellow">Funcionalidad.</mark>
    La funcionalidad mide el conjunto de características y capacidades que tiene el producto de software, la generalidad de las funciones que se entregan y  la seguridad general del sistema.
    
- ##### <mark class="hltr-yellow">Usabilidad.</mark>
    La usabilidad se refiere más que todo a las operaciones que tiene que ver con los factores humanos, la estética coherencia y documentación del software.
    Se enfoca en crear productos que sean fáciles de usar y que satisfagan las necesidades y expectativas de los usuarios.
    En resumen, la usabilidad es un aspecto fundamental del diseño de software que se enfoca en crear productos fáciles de usar y satisfacer las necesidades y expectativas de los usuarios. La usabilidad se compone de varios aspectos y se logra mediante la aplicación de principios de diseño centrados en el usuario, la realización de pruebas de usabilidad y la iteración continua del diseño en función de los resultados de las pruebas.
    
- ##### <mark class="hltr-yellow">Fiabilidad.</mark>
    La fiabilidad , por su parte, data sobre la precisión y el tiempo medio de fallos que puede presentar el software durante su desarrollo y después de haberse comercializado.
    
    Es un aspecto crítico del diseño de software que se enfoca en garantizar que el sistema o producto sea confiable y consistente en su funcionamiento. La fiabilidad se logra mediante técnicas y herramientas específicas de diseño, como el diseño de redundancia, la gestión de errores y el monitoreo y diagnóstico de fallos, y se puede medir mediante pruebas de estrés y pruebas de carga.
    
- ##### <mark class="hltr-yellow">Rendimiento.</mark>
    Hace mención sobre la velocidad, la eficiencia, el consumo de los recursos y el tiempo de respuesta que presenta el software en su funcionamiento e interacción con el usuario.
    ![[rendimiento.png]]
    
- ##### <mark class="hltr-yellow">Capacidad de mantenimiento.</mark>
También conocida como capacidad de soporte técnico, implicado como la mayor tarea que debe realizar las empresas creadoras de software, implican la extensibilidad, adaptabilidad, capacidad de instalación, localización y portabilidad del producto final de software.
<br> 

### <mark class="hltr-red">Fundamentos del diseño</mark>

- ##### <mark class="hltr-yellow">Abstracción.</mark>
    Es una descripción de especificación que enfatiza algunos de los detalles o propiedades de algo. La abstracción consiste en captar las características esenciales de un objeto, así como su comportamiento.
    
    Es un proceso mediante el cual se identifican los aspectos relevantes de un problema ignorando los detalles; es un caso especial del principio de separación de intereses en el cual se separan los aspectos importantes de los detalles de menor importancia.
    
    - Una abstracción de **datos** es una determinada colección de datos que describen un objeto.
    - Una abstracción **procedimental** es una determinada secuencia de instrucciones que tienen una función limitada y específica.
    
    En resumen, la abstracción se refiere a la capacidad de representar la complejidad de un sistema o problema de manera simplificada, enfocándose en los aspectos esenciales y omitiendo los detalles innecesarios o irrelevantes. La abstracción se utiliza en el diseño de software para simplificar la complejidad del sistema y enfocarse en los aspectos importantes del problema, y se puede aplicar mediante diferentes técnicas, como la definición de capas, clases y objetos en la programación orientada a objetos.
    
- ##### <mark class="hltr-yellow">Refinamiento.</mark>
    El refinamiento sucesivo es una primera estrategia de diseño descendente. Desarrolla una jerarquía descomponiendo una declaración macroscópica de una función de una forma sucesiva, hasta que llega a las sentencias del lenguaje de programación.
    
    Es un proceso iterativo que comienza con una descripción general del problema y avanza hacia detalles más específicos y detallados a medida que se adquiere una comprensión más profunda del problema y se definen las soluciones. El proceso de refinamiento implica la definición de diferentes niveles de abstracción, donde cada nivel representa un nivel de detalle mayor y una mayor especificidad.
    ![[refinamiento.png]]
    
- ##### <mark class="hltr-yellow">Modularidad.</mark>
    El software se divide en componentes con nombres y ubicaciones determinados, que se denominan módulos y que se integran para satisfacer los requisitos del problema.
    ![[modularidad.png]]
    
- ##### <mark class="hltr-yellow">Arquitectura de software.</mark>    
    En su forma más simple, la arquitectura es la estructura jerárquica de los componentes del
    programa (módulos), la manera en que los componentes interactúan y la estructura de datos que van a utilizar los componentes.
    ![[arquitectura_software.png]]
    
- ##### <mark class="hltr-yellow">Jerarquía de control.</mark>
    Representa la organización (frecuentemente jerárquica) de los componentes del programa (módulos) e implica una jerarquía de control.
    ![[jerarquia_control.png]]
    
- ##### <mark class="hltr-yellow">División estructural.</mark>
    Si el estilo arquitectónico de un sistema es jerárquico, la estructura del programa se puede dividir tanto horizontal como verticalmente.
    ![[division_estructural.png]]
    Al dividirla de forma vertical podemos ver que cada sección representara una función del software y al dividirla de forma horizontal podremos observar que cada sección nos muestra un nivel de trabajo de el software, mostrando en la parte superior los módulos que toman decisiones y en la parte inferior los módulos que realizan transacciones.
    
    En resumen, la división estructural se basa en la idea de que un sistema complejo se puede dividir en partes más pequeñas, llamadas módulos, que son más fáciles de entender y manejar. Cada módulo representa una parte del sistema que realiza una función específica y tiene una interfaz claramente definida con otros módulos.
    
- ##### <mark class="hltr-yellow">Estructura de datos.</mark>
    Las estructuras de datos nos muestran la manera lógica y congruente como se relacionan los datos. La forma como se organiza la información que será almacenada y procesada por el software influye en la arquitectura del mismo.
    
    En programación las estructuras de datos representan agrupaciones complejas de datos simples, como lo son las pilas, las colas, los arboles o las listas; pero por sobre todas estas la forma de organización de datos mas usadas por los sistemas son las bases de datos, aunque no sean consideradas en si mismo una estructura de datos.
    ![[estructura_datos.png]]
<br> 

### <mark class="hltr-red">Diseño modular efectivo</mark>

La independencia funcional se adquiere desarrollando módulos con una función clara y con pocas relaciones con otros módulos.

Un módulo cohesivo lleva a cabo una sola tarea dentro de un procedimiento de software, lo cual requiere poca interacción con los procedimientos que se llevan a cabo en otras partes de un programa.

El acoplamiento es una medida de interconexión entre módulos dentro de una estructura de software. El acoplamiento depende de la complejidad de interconexión entre los módulos

Mas información sobre la [[Descomposición modular]].