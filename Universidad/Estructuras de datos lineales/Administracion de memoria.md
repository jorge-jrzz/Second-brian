---
banner_icon: 📝
---
# Administración de memoria

En la RAM existe un “administrador de memoria”, el cual principalmente gestiona la memoria, pero también se encarga de lo siguiente:

- Conocer o identificar que memoria se está usando
- Determinar que procesos pueden cargarse
- Asignar memoria
- Liberar Memoria
- Intercambiar entre memoria principal y disco cuando no hay suficiente para todos los procesos.

Cuando un programa se carga en la memoria se convierte en procesos que serán ejecutados mediante técnicas como: 

- Partición Fija: División de la memoria libre en varias partes de igual o de distinto tamaño. Las funciones del administrador de memoria son: “Administrador de Memoria” es la parte del sistema operativo que se encarga de administrar o gestionar la memoria.
- Partición Dinámica: Particiones de memoria de tamaños variables y que se determinan de acuerdo con la cantidad que requiera cada proceso.

Operaciones principales del administrador de memoria:

- Reubicación: Trasladar procesos activos dentro y fuera de la memoria principal para maximizar el uso del procesador, ofreciendo un espacio lógico propio a cada proceso. Carga y descarga los procesos de la memoria.
- Protección: Mecanismos de protección a los procesos que se ejecutan de interferencias de otros procesos y sus direcciones
- Maximizar el rendimiento del sistema mediante la organización del flujo de información entre la memoria principal y la secundaria
- Compartición: Permitir que los procesos compartan códigos y datos, con lo que el mecanismo de protección deja que ciertos procesos de un mismo programa que comparten una tarea tengan memoria en común.
![[jerarquia_memoria.png]]

![[tecnicas_administracion.png]]

![[asignacion_memoria.png]]

Problemáticas que presentan las particiones <mark class="hltr-cyan">estáticas</mark>:

1. Un programa puede ser demasiado grande para caber en una partición, por lo tanto si el programa no se ha diseñado mediante superposición, simplemente no se ejecuta. De otro modo se alojaran en la memoria aquellos módulos que se necesiten, pero se requiere que estos módulos sean intercambiados a medida que la ejecución avanza.
2. Se malgasta el espacio interno de las particiones cuando un proceso es muy pequeño, ya que cualquier proceso por pequeño que sea ocupará una partición completa.
3. Hay fragmentación, es decir, el sistema operativo tiene la incapacidad de asignar posiciones de memoria no utilizados (interna y externa).
4. El número de particiones especificadas en el momento de la generación del sistema limita el número de procesos activos.
5. El uso de particiones actualmente ya es casi nulo solo el OS/MFT de IBM lo maneja.

![[tecnicas_administracion_dinamicas.png]]

![[primer_ajuste.png]]

![[mejor_ajuste.png]]

![[peor_ajuste.png]]

Problemáticas que presentan las particiones <mark class="hltr-cyan">dinámicas</mark>:

1. Fragmentación Externa: Debido a la entrada y salida de procesos se van generando particiones cada vez más pequeñas sin usar.
2. Compactación: Tratar de eliminar los espacios entre procesos (huecos), reubicándolos en la memoria de forma dinámica, y juntar en un solo bloque los espacios de memoria libre. 
3. La compactación no se puede hacer con tanta frecuencia.
4. El sistema se detiene mientras se hace la compactación.
5. Consume recursos del sistema.

![[particiones_dinamicas.png]]

###### <mark class="hltr-green">Compactación</mark>:
* Consiste en desplazar las particiones ocupadas para que estén juntas en la memoria.
* Solo es posible si la reubicación es dinámica (en ejecución).
* Es una solución al problema de fragmentación externa.
* Deja un solo hueco de libre de mayor tamaño.
* Es difícil encontrar la estrategia óptima para la compactación
* Consume tiempo el desplazar la memoria
* Durante la compactación no se pueden ejecutar otros procesos

![[compactacion.png]]

### <mark class="hltr-orange">Técnicas de administración de memoria:</mark>

> ##### <mark class="hltr-cyan">Asignación no contigua:</mark>
> * Paginación
> * Segmentación
> ![[paginacion.png]]
> ![[segmentacion.png]]

---

> ##### <mark class="hltr-cyan">Fragmentación:</mark>
> 1. Los segmentos son de tamaño variable.
> 2. Puede presentarse fragmentación externa.
> 3. Bloques muy pequeños para contener un segmento.
> 4. Se puede compactar usando reubicación dinámica.
> 5. Cada proceso tiene su propio segmento (Particiones variables).
> 6. Cada palabra (byte) es un segmento.
> 7. No hay fragmentación externa
> 8. Se ocupa una tabla de segmentos del tamaño de la MP.