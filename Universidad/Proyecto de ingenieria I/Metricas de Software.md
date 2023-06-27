---
banner_icon: ☔
banner: "![[ed-white-performs-first-us-spacewalk_9449352803_o.jpg]]"
banner_y: 0.544
---

# Métricas de Software

| Métrica                        | Descripción                                                                                                                                                                                                                         |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Métricas basadas en el código  | Estas métricas se centran en evaluar diferentes aspectos del código fuente, como líneas de código, complejidad ciclomática, acoplamiento y cohesión. Ofrecen información sobre la calidad, complejidad y mantenibilidad del código. |
| Métricas basadas en tokens     | Estas métricas analizan los elementos individuales del código fuente, como palabras clave, identificadores y operadores. Proporcionan información sobre la complejidad, tamaño y legibilidad del código.                            |
| Métricas basadas en la función | Estas métricas se enfocan en las características y propiedades de las funciones o métodos dentro del código. Evalúan aspectos como la longitud de la función, complejidad ciclomática, acoplamiento y cohesión de la función.       |

---

Las métricas son sistemas de medición que sirven para cuantificar y evaluar aspectos de un negocio, por ejemplo, tendencias, comportamientos y resultados. Son capaces de medir y evaluar el desempeño de cualquier acción y mostrar si las estrategias están contribuyendo o no a los resultados de una empresa.

### <mark class="hltr-orange">Métricas basadas en código</mark>
Las métricas basadas en el código son medidas cuantitativas utilizadas para evaluar diferentes aspectos del código fuente de un software. Estas métricas proporcionan información sobre la calidad, complejidad, mantenibilidad y otros atributos del código.

Algunas de las métricas basadas en el código comunes son:

1. Líneas de código (LOC): Es la cantidad total de líneas de código en un archivo, módulo o proyecto. Esta métrica puede indicar la complejidad y el tamaño del código.

2. Complejidad ciclomática: Mide la complejidad estructural de un programa y se basa en el número de caminos independientes a través del código. Una complejidad ciclomática alta puede indicar mayor dificultad para entender y mantener el código.

3. Acoplamiento: Mide el grado de dependencia entre diferentes módulos o componentes del software. Un alto acoplamiento puede indicar una estructura menos modular y más dependiente.

4. Cohesión: Mide la relación y la fortaleza de la funcionalidad compartida entre las partes de un módulo o componente. Una alta cohesión indica una estructura más modular y centrada en una única responsabilidad.

5. Índice de mantenibilidad: Es una métrica que evalúa la facilidad con la que se puede mantener el código en el futuro. Puede estar basado en una combinación de otras métricas, como complejidad, duplicación de código, acoplamiento, entre otros.

6. Duplicación de código: Mide la cantidad de código duplicado en un proyecto. La duplicación excesiva puede dificultar el mantenimiento y aumentar la probabilidad de errores.

Estas son solo algunas de las métricas basadas en el código utilizadas comúnmente. La elección de las métricas adecuadas depende del contexto del proyecto y de los objetivos que se deseen lograr al evaluar el código. Es importante utilizar estas métricas como una guía complementaria para identificar áreas de mejora y seguir buenas prácticas de desarrollo de software.

### <mark class="hltr-orange">Métricas basadas en tokens</mark>
Las métricas basadas en tokens son un tipo de métricas de software que se centran en el análisis de los elementos individuales del código fuente, como palabras clave, identificadores, operadores y otros tokens que conforman el lenguaje de programación utilizado.

Estas métricas se calculan contando la cantidad de tokens en el código y proporcionan información adicional sobre la complejidad, el tamaño y la legibilidad del código. Algunas métricas basadas en tokens comunes incluyen:

1. Longitud media del identificador: Mide el promedio de la longitud de los identificadores utilizados en el código. Identificadores largos pueden dificultar la comprensión del código y la legibilidad.

2. Número de palabras clave: Cuenta la cantidad de palabras clave utilizadas en el código. Un número elevado de palabras clave puede indicar una mayor complejidad o un mal diseño.

3. Número de operadores: Cuenta la cantidad de operadores utilizados en el código. Un alto número de operadores puede indicar una mayor complejidad y potencialmente un código más difícil de entender.

4. Densidad de comentarios: Calcula el porcentaje de tokens que son comentarios en relación con el total de tokens. Una alta densidad de comentarios puede indicar un código bien documentado y más fácil de entender.

![[metrica_token.png | 500]]

Estas métricas basadas en tokens proporcionan una visión más detallada de la estructura y características del código fuente. Pueden ayudar a identificar patrones de diseño, problemas de legibilidad y complejidad, así como también pueden ser utilizadas para comparar diferentes versiones del código o para establecer estándares de codificación en un equipo.

Es importante destacar que las métricas basadas en tokens no son una medida absoluta de la calidad del código y deben usarse en conjunto con otras métricas y buenas prácticas de desarrollo de software para obtener una evaluación más completa.

### <mark class="hltr-orange">Métricas basadas en la función</mark>
El cálculo de los puntos de función es una técnica utilizada en la ingeniería de software para medir el tamaño funcional de un sistema de información. Fue propuesta por Allan Albrecht en la década de 1970 como una alternativa a las métricas tradicionales basadas en líneas de código. Los puntos de función se centran en la funcionalidad proporcionada por el software más que en su implementación específica.

Los puntos de función se calculan en función de los requerimientos funcionales del sistema, es decir, las funciones que el software debe proporcionar para satisfacer las necesidades del usuario. Estas funciones se agrupan en categorías llamadas "tipos de transacciones" y "tipos de archivos".

Los tipos de transacciones representan las interacciones del usuario con el sistema y se clasifican en tres categorías:

1. Entradas externas: son las funciones que requieren la entrada de datos por parte del usuario. Por ejemplo, completar un formulario en línea o ingresar información en una base de datos.

2. Salidas externas: son las funciones que generan información para el usuario. Por ejemplo, generar informes o mostrar datos en una pantalla.

3. Consultas externas: son las funciones que combinan entrada y salida de datos. Por ejemplo, buscar y mostrar información en respuesta a una consulta del usuario.

Los tipos de archivos representan los datos mantenidos por el sistema y se clasifican en dos categorías:

1. Archivos lógicos internos: son conjuntos de datos mantenidos y utilizados por el sistema. Por ejemplo, una base de datos de clientes o un registro de ventas.

2. Archivos de interfaz externa: son conjuntos de datos utilizados tanto por el sistema como por otros sistemas externos. Por ejemplo, un archivo de importación o exportación de datos.

Para calcular los puntos de función, se asigna un valor numérico a cada función en función de su complejidad. Estos valores se denominan "puntos de función no ajustados" y se suman para obtener el tamaño funcional total del sistema.

![[metrica_punto_funcion_formula.png | 400]]

Además de los puntos de función no ajustados, se aplican factores de ajuste para reflejar características específicas del sistema, como la complejidad del procesamiento lógico, la complejidad de los archivos de interfaz externa y otros factores. Estos factores de ajuste se multiplican por los puntos de función no ajustados para obtener los "puntos de función ajustados".

![[metrica_punto_funcion.png | 500]]

#### <mark class="hltr-orange">Factores de ajuste</mark>
Los factores de ajuste de valor, también conocidos como factores de ponderación o factores de ajuste de complejidad, son utilizados en el cálculo de los puntos de función para reflejar características específicas del sistema que pueden influir en su complejidad y, por lo tanto, en la cantidad de puntos de función asignados.

Existen cinco factores de ajuste de valor comúnmente utilizados:

1. Comunicación de datos: Este factor refleja la complejidad asociada con la comunicación de datos entre el software y otros sistemas externos. Se tienen en cuenta aspectos como el formato de los datos, la cantidad de datos intercambiados y la complejidad de las interfaces de comunicación.

2. Procesamiento distribuido: Este factor se aplica cuando el sistema se ejecuta en una arquitectura distribuida, es decir, cuando diferentes componentes o módulos del sistema se ejecutan en diferentes dispositivos o computadoras. La complejidad aumenta debido a la necesidad de coordinación y comunicación entre los diferentes componentes distribuidos.

3. Rendimiento: Este factor tiene en cuenta la importancia del rendimiento del sistema en términos de tiempo de respuesta y capacidad de procesamiento. Si el rendimiento es crítico para el sistema, se asignará un factor de ajuste más alto.

4. Configuración del hardware: Este factor se refiere a la complejidad asociada con la configuración del hardware requerido para el sistema. Si el sistema requiere una configuración de hardware compleja o especializada, se asignará un factor de ajuste más alto.

5. Transacciones en línea: Este factor se aplica cuando el sistema tiene una gran cantidad de transacciones en línea simultáneas. Si el sistema debe manejar muchas transacciones en tiempo real, se asignará un factor de ajuste más alto.

Cada factor de ajuste tiene un rango de valores, generalmente de 0 a 5, donde 0 representa ninguna influencia o impacto y 5 representa una influencia muy alta o un impacto significativo en la complejidad del sistema. Estos factores se multiplican entre sí y se aplican al número total de puntos de función no ajustados para obtener los puntos de función ajustados.

| Factor | Significado   |
|:------: | ------------- |
| 0      | No presente   |
| 1      | Incideltal    |
| 2      | Moderado      |
| 3      | Medio         |
| 4      | Significativo |
| 5      | Esencial              |

#### <mark class="hltr-yellow">Ejemplo</mark>:

> ![[factores_ajuste_ejemplo.png| 450]]
> 
> ![[metrica_punto_funcion_ejemplo.png | 650]]
> 
> ![[valor_factor_ajuste.png | 650]]
> 
> PFA = 50 x \[0.65 + (0.01 x 46)] = 56

Una vez calculados los puntos de función ajustados, se pueden utilizar para estimar la cantidad de esfuerzo, tiempo y recursos necesarios para desarrollar el sistema de software. También pueden ser útiles para comparar diferentes proyectos o realizar análisis de productividad.

Es importante tener en cuenta que el cálculo de los puntos de función requiere un análisis detallado de los requerimientos del sistema y una comprensión clara de la metodología y los criterios de clasificación. También es recomendable contar con personal capacitado y experiencia en esta técnica para obtener resultados precisos y confiables.