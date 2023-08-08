---
banner_icon: 🉐
banner: "![[astronaut-charles-duke-with-lunar-rover-on-moon_9460223832_o.jpg]]"
banner_y: 0.148
---

# Tipos de archivos

Los tipos de archivos reconocidos por el sistema son **normal**, **directorio** o **especial**. No obstante, el sistema operativo utiliza muchas variaciones de estos tipos básicos.

A continuación se indican los tipos básicos de archivos existentes:

|Elemento|Descripción|
|---|---|
|**normal**|Almacena datos (texto, binario y ejecutable)|
|**directorio**|Contiene la información que se utiliza para acceder a otros archivos|
|**especial**|Define un archivo de conducto FIFO (primero en entrar, primero en salir) o un dispositivo físico|

Todos los tipos de archivos reconocidos por el sistema se enmarcan en una de estas categorías. No obstante, el sistema operativo utiliza muchas variaciones de estos tipos básicos.

#### Archivos normales

Los archivos normales son los archivos más comunes y se utilizan para contener datos. Los archivos normales están en formato de archivos de texto o de archivos binarios:

##### Archivos de texto
Los archivos de texto son archivos normales que contienen información almacenada en formato ASCII y que el usuario puede leer. Puede visualizar e imprimir dichos archivos. Las líneas de un archivo de texto no deben contener caracteres **`NUL`** y ninguna puede exceder de **`{LINE_MAX}`** bytes de longitud, incluido el carácter de nueva línea.

El término _archivo de texto_ no impide la inclusión de caracteres de control o de otros caracteres no imprimibles (diferentes de `NUL`). Por lo tanto, los programas de utilidad estándar que listan archivos de texto como entradas o como salidas o bien son capaces de procesar los caracteres especiales o bien son capaces de describir explícitamente sus limitaciones dentro de sus secciones individuales.

##### Archivos binarios
Los archivos binarios son archivos normales que contienen información que el sistema puede leer. Los archivos binarios podrían ser archivos ejecutables que indicaran al sistema que ha de realizar un trabajo. Los mandatos y los programas se almacenan en archivos binarios ejecutables. Los programas de compilación especial convierten texto ASCII en código binario.

Los archivos de texto y binarios sólo se diferencian en que los archivos de texto tienen líneas de menos de **`{LINE_MAX}`** bytes, sin ningún carácter **`NUL`**, cada una de las cuales termina con un carácter de nueva línea.


#### Archivos de directorios

Los archivos de directorio contienen la información que el sistema necesita para acceder a todos los tipos de archivos, pero los archivos de directorio no contienen los datos reales del archivo. En consecuencia, los directorios ocupan menos espacio que un archivo normal y proporcionan a la estructura de sistema de archivos flexibilidad y profundidad. Cada entrada de directorio representa un archivo o un subdirectorio. Cada entrada contiene el nombre del archivo y el número de referencia de nodo de índice (_número de i-nodo_) del archivo. El número de inodo apunta al nodo de índice exclusivo que se ha asignado al archivo. El número de inodo describe la ubicación de los datos que se asocian al archivo. Un grupo independiente de mandatos crea y controla los directorios.


#### Archivos especiales

Los archivos especiales definen dispositivos para el sistema o son archivos temporales creados por procesos. Los tipos básicos de archivos especiales son FIFO (primero en entrar, primero en salir), de bloques y de caracteres. Los archivos FIFO también se denominan _conductos_. Los conductos se crean mediante un proceso para permitir temporalmente las comunicaciones con otro proceso. Estos archivos dejan de existir cuando termina el primer proceso. Los archivos de bloque y los archivos de caracteres definen dispositivos.

Cada archivo tiene un conjunto de permisos (denominado _modalidades de acceso_) que determina quién puede leer, modificar o ejecutar el archivo.


### Archivos binarios

Los archivos binarios son tipos de archivos que contienen información en un formato que no es directamente legible por los seres humanos, ya que están compuestos por secuencias de valores numéricos, normalmente representados en código binario (0 y 1). A diferencia de los archivos de texto, que contienen caracteres legibles, los archivos binarios pueden incluir una variedad de datos, como imágenes, videos, audio, programas ejecutables, bases de datos y más.

Los archivos binarios son utilizados por las computadoras para almacenar y manipular datos en su forma más eficiente. Debido a que los archivos binarios no están limitados por la estructura y formato de los caracteres legibles, pueden representar una amplia gama de información de manera compacta y rápida. Sin embargo, debido a su naturaleza no legible para humanos, a menudo se requiere software especializado para interpretar y trabajar con archivos binarios.

Algunas diferencias clave entre los archivos binarios y las bases de datos:

1. **Estructura y Organización:**
   - *Archivos Binarios:* Los archivos binarios carecen de una estructura interna específica y están diseñados para almacenar datos de manera contigua. Cada tipo de archivo binario tiene su propia estructura particular.
   - *Bases de Datos:* Las bases de datos están organizadas de manera estructurada en tablas con filas y columnas, lo que permite una mejor organización de los datos. Esto facilita la búsqueda y manipulación de información.

2. **Flexibilidad de Consultas:**
   - *Archivos Binarios:* En general, los archivos binarios no permiten realizar consultas o búsquedas directamente en los datos. La información contenida en ellos debe ser procesada por programas específicos.
   - *Bases de Datos:* Las bases de datos permiten realizar consultas complejas utilizando lenguajes como SQL. Puedes buscar, filtrar, ordenar y combinar datos de manera eficiente.

3. **Integridad de los Datos:**
   - *Archivos Binarios:* No suelen tener mecanismos internos para garantizar la integridad de los datos. La validación y el mantenimiento de la integridad dependen de las aplicaciones que los utilizan.
   - *Bases de Datos:* Las bases de datos incluyen mecanismos de integridad como restricciones de clave primaria y foránea, lo que ayuda a mantener la coherencia y calidad de los datos.

4. **Acceso Concurrente:**
   - *Archivos Binarios:* Por lo general, no están diseñados para admitir el acceso concurrente de múltiples usuarios. Puede ser complicado compartir y editar un archivo binario simultáneamente.
   - *Bases de Datos:* Están diseñadas para admitir el acceso concurrente de múltiples usuarios. Varios usuarios pueden acceder y modificar los datos de manera simultánea sin causar conflictos.

5. **Escalabilidad:**
   - *Archivos Binarios:* Manejar grandes cantidades de datos puede volverse complicado con archivos binarios, ya que no están optimizados para escalabilidad.
   - *Bases de Datos:* Están diseñadas para manejar grandes volúmenes de datos y escalar de manera eficiente a medida que crece la cantidad de información almacenada.

6. **Seguridad y Control de Acceso:**
   - *Archivos Binarios:* Suelen carecer de funciones de seguridad avanzadas. El control de acceso a los archivos binarios debe ser gestionado externamente.
   - *Bases de Datos:* Ofrecen opciones avanzadas de seguridad, como autenticación, autorización y auditoría, para garantizar que solo las personas autorizadas tengan acceso a los datos.

En resumen, mientras que los archivos binarios son adecuados para almacenar datos simples y archivos específicos, las bases de datos proporcionan una estructura más robusta y versátil para el almacenamiento, gestión y manipulación de datos. A medida que entres en el mundo de las bases de datos, te darás cuenta de cómo ofrecen soluciones más poderosas y flexibles para gestionar la información en comparación con los archivos binarios tradicionales.
