---
banner_icon: 🐭
banner: "![[earth-and-moon-as-viewed-by-mariner-10_5052129491_o.jpg]]"
banner_y: 0.472
---

# Descomposición modular

### <mark class="hltr-red">Capacidad de empleo de componentes modulares</mark>
Si un método de diseño proporciona un mecanismo sistemático para descomponer el problema en subproblemas, reducirá la complejidad de todo el problema, consiguiendo de esta manera una solución modular efectiva.

Si un método de diseño permite ensamblar los componentes de diseño (reusables) existentes en un sistema nuevo, producirá una solución modular que no inventa nada ya inventado. 

![[componentes_modulares.png | 650]]
Si un modulo se puede comprender como una unidad autónoma (sin referencias a otros módulos) será mas difícil de construir y de cambiar. 

### <mark class="hltr-red">Continuidad modular</mark>
Si pequeños cambios en los requisitos de sistemas provocan cambios en los módulos individuales, en vez de cambios generalizados en el sistema, se minimizara el impacto de los efectos secundarios de los cambios. 

### <mark class="hltr-red">Protección modular</mark>
Si dentro de un módulo se produce una condición aberrante y sus efectos se limitan a ese módulo, se minimizará el impacto de los efectos secundarios inducidos por los errores.

### <mark class="hltr-red">Conceptos</mark>
Se puede decir que un módulo es un fragmento de un sistema de Software que se puede elaborar con relativa independencia de los demás y llega a descomponer el problema en subproblemas. 

![[divide_y_venceras.png | 650]]

La experiencia acumulada permite establecer que una descomposición modular debe poseer ciertas cualidades mínimas para que se pueda considerar suficientemente válida. Estas cualidades son:

- #### <mark class="hltr-red">Independencia funcional</mark>
	Para que un módulo posea independencia funcional **debe realizar una función concreta** o un conjunto de funciones afines, sin apenas ninguna relación con el resto de los módulos del sistema.

	Una mayor independencia redunda en una mayor facilidad de mantenimiento o sustitución de un módulo por otro y aumenta la posibilidad de reutilización del módulo.

	Para medir de una forma relativa la independencia funcional que hay entre varios módulos se utilizan fundamentalmente dos criterios: acoplamiento y cohesión.
	
	![[independencia_funcional.png | 650]]

	- ##### <mark class="hltr-pink">Acoplamiento</mark>
		El grado de acoplamiento entre módulos es una medida de la interrelación que existe entre ellos. Tipo de cohesión y complejidad de la interface. Para medir el grado de acoplamiento entre módulos se utiliza la siguiente escala:
		- <mark class="hltr-orange">Acoplamiento por contenido</mark>: Tiene lugar cuando desde un módulo se pueden cambiar los datos locales e incluso el código de otro módulo. Este tipo de acoplamiento fuerte sólo se puede lograr empleando un lenguaje ensamblador o de muy bajo nivel, resulta imposible el mantenimiento así como el entendimiento y depuración de un sistema con este tipo de acoplamiento.
		- <mark class="hltr-orange">Acoplamiento común</mark>: En este se emplea una zona común de datos a la que tienen acceso varios o todos los módulos del sistema. El empleo de este acoplamiento exige que todos los módulos estén de acuerdo en la estructura de la zona común y cualquier cambio adoptado por alguno de ellos afectará al resto, al igual que el anterior la depuración y mantenimiento resulta muy difícil.
		- <mark class="hltr-orange">Acoplamiento externo</mark>: En éste la zona común está constituida por algún dispositivo externo, al que están ligados todos los módulos, aunque éste es inevitable siempre se deben buscar descomposiciones en que los dispositivos externos acepten al mínimo número de módulos.
		- <mark class="hltr-orange">Acoplamiento de control</mark>: En este tipo de acoplamiento una señal o dato de control es lo que se pasa de un modulo a otro, con este tipo de acoplamiento dentro de un mismo modulo se pueden tratar distintas situaciones, en general este acoplamiento se utiliza para solicitar o anular servicios adicionales a un determinado módulo. En este caso, una señal (s) o dato de control que se pasa de un módulo (A) a otro (B) es lo que determina la línea de ejecución que se debe seguir dentro de este último (B).
			
			![[acoplamiento_control.png | 450]]
		- <mark class="hltr-orange">Acoplamiento débil</mark>: Se produce sólo a través del intercambio de aquellos datos que un módulo necesita de otro. Si el intercambio se realiza estrictamente con los únicos datos que se necesitan tenemos un acoplamiento de Datos. Este es el mejor tipo posible de acoplamiento. 
		<br>
		
	- ##### <mark class="hltr-pink">Cohesión</mark>
		Éste es complementario al anterior ya que además de buscar un acoplamiento débil entre los módulos es necesario conseguir que el contenido de cada módulo sea coherente. La escala para medir la cohesión de un módulo es:
		  - **Cohesión coincidental**: Esta se produce cuando las actividades de los elementos del módulo no están relacionadas entre sí (caso peor). Algunos de los ejemplos de cohesión coincidente son el módulo para funciones diversas, el uso de registros de clientes, la visualización de registros de clientes, el cálculo de ventas totales, la lectura del registro de transacciones, etc.
		  - **Cohesión lógica**: se da cuando las partes de un módulo se agrupan porque están categorizadas lógicamente para hacer lo mismo aunque sean diferentes por naturaleza.
		  - **Cohesión temporal**: cuando en un módulo los elementos están envueltos en actividades que están relacionadas por el tiempo (se desarrollan conforme al tiempo). Normalmente cada una de estas actividades responde a una tarea diferente.
		  - **Cohesión de comunicación**: Es aquella que se produce cuando todos los elementos de un módulo operan con el mismo conjunto de datos de entrada o producen el mismo conjunto de datos de salida.
		![[cohesion_comunicacion.png | 550]]
		  - **Cohesión secuencial**: Se produce cuando todos los elementos de un módulo trabajan de manera secuencial (la salida de un elemento es la entrada del siguiente de manera sucesiva).
		  - **Cohesión funcional**: En este cada módulo se encarga de realizar una función concreta y específica, esta técnica por lo tanto tiene por objeto que todos los módulos tengan una cohesión funcional. Son los módulos más reutilizables ya que solo es necesario conocer la función que cumplen.
		  - **Cohesión abstraccional**: Con la técnica de diseño basado en abstracciones un módulo con cohesión funcional será una abstracción funcional. Esta cohesión se logra cuando se diseña un módulo como TDA con la técnica especificada anteriormente o como una clase de objetos con la técnica orientada a objetos.

<br>

- ### <mark class="hltr-red">Comprensibilidad</mark>
El primer factor que facilita la comprensión de un módulo es su independencia funcional. Como se ha visto antes, con una cohesión alta y un acoplamiento débil, el módulo tiene menor dependencia del resto del sistema y por tanto será más fácil entender su funcionamiento de manera aislada. Pero además es necesario cuidar los siguientes factores:
  - ***Identificación***: Elegir adecuadamente el nombre del módulo y de los nombres de cada uno de sus elementos. Los nombres deben reflejar de manera sencilla el objetivo de la entidad que representan.
  - ***Documentación***: La labor de documentación de cada módulo y del sistema en general debe servir para facilitar la comprensión. Se deben establecer normas y convenios de documentación que evitar problemas de comprensión.
  - ***Simplicidad***: Las soluciones sencillas son siempre las mejores. Un esfuerzo fundamental del diseñador debe estar dedicado a simplificar al máximo las soluciones propuestas.
    
    ![[documentacion.png | 550]]

<br>

La independencia funcional y la comprensibilidad son dos cualidades esenciales que debe tener cualquier diseño para posibilitar su adaptabilidad.
Otros factores adicionales para facilitar la adaptabilidad son los siguientes:
  • ***Previsión***: Resulta muy complicado prever qué evolución futura tendrá un determinado sistema. Solo la experiencia previa nos podría indicar qué partes del sistema han sido más dados a cambios o adaptaciones en otros sistemas semejantes.
  • ***Accesibilidad***: Antes de abordar la nueva adaptación de un sistema, es necesario conocerlo con la suficiente profundidad. Este trabajo sólo es posible si resulta sencilla la accesibilidad a todos los documentos de especificación, diseño e implementación. 
  • ***Consistencia***: Cuando se realizan adaptaciones sucesivas, es vital mantener la consistencia entre todos los documentos de especificación, diseño e implementación para cada nueva adaptación. Existen herramientas para el “control de versiones y configuración” que permiten mantener automáticamente la consistencia en cada adaptación.