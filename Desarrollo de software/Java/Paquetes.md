---
banner_icon: 📦
banner: "![[buzz-aldrin-on-the-moon_9460192910_o.jpg]]"
banner_y: 0.1
---

# Paquetes

En Java, los paquetes ==son una forma de organizar y estructurar clases y otros tipos de componentes en grupos lógicos y jerárquicos.== Los paquetes ayudan a evitar conflictos de nombres entre clases y a mantener el código más ordenado y modular. Un paquete puede contener clases, interfaces, enumeraciones y subpaquetes.

Aquí hay algunas características y ventajas de los paquetes en Java:

1. **Organización y estructura**: Los paquetes permiten organizar y estructurar las clases y otros componentes de un programa en unidades lógicas y coherentes. Esto facilita la navegación y el mantenimiento del código a medida que el proyecto crece.

2. **Evitar conflictos de nombres**: Java utiliza un sistema de resolución de nombres basado en paquetes. Esto significa que dos clases con el mismo nombre pueden coexistir siempre que pertenezcan a paquetes diferentes. Los paquetes evitan colisiones de nombres en el espacio de nombres global.

3. **Encapsulación y control de acceso**: Los miembros (métodos, campos, clases anidadas) de una clase pueden tener diferentes niveles de acceso (public, protected, default y private). Los paquetes también tienen un nivel de acceso llamado "default" o "package-private". Esto permite controlar qué elementos son visibles fuera del paquete y cuáles son solo accesibles dentro del mismo.

4. **Modularidad y reutilización**: Los paquetes promueven la modularidad y la reutilización del código. Puedes agrupar clases relacionadas en un paquete y reutilizar ese paquete en otros proyectos. Esto es especialmente útil en proyectos grandes y complejos.

5. **Nomenclatura de paquetes**: La nomenclatura de los paquetes sigue una estructura de directorios invertida, donde los componentes del paquete se separan por puntos. Por ejemplo, si tienes un paquete llamado `com.miempresa.proyecto`, las clases en ese paquete estarán ubicadas en una estructura de directorios similar en el sistema de archivos.

6. **Importación de clases**: Cuando deseas utilizar una clase de otro paquete en tu código, debes importarla utilizando la palabra clave `import`. Esto evita tener que escribir el nombre completo de la clase cada vez que la utilices.

Los paquetes son una parte fundamental de la organización y estructura en Java. Al usar paquetes de manera efectiva, puedes mantener un código limpio, modular y fácil de entender, además de evitar conflictos de nombres y promover la reutilización del código.


### Full Qualified Name

El **Full Qualified Name** (FQN) en Java se refiere al nombre completo y único de una clase, que incluye tanto el nombre del paquete al que pertenece la clase como el nombre de la clase en sí. El FQN es una forma de identificar de manera unívoca una clase en todo el espacio de nombres de Java, independientemente de la estructura de paquetes.

El FQN sigue la estructura de nombres de paquetes invertida y se escribe en la forma `paquete.clase`. Por ejemplo, si tienes una clase llamada `MiClase` en el paquete `com.miempresa.miprograma`, el FQN de esa clase sería `com.miempresa.miprograma.MiClase`.

El uso del FQN es común en situaciones donde puede haber ambigüedad en los nombres de clases debido a clases con nombres similares en diferentes paquetes. Al usar el FQN, puedes referirte a una clase de manera precisa y evitar cualquier posible confusión.

Por ejemplo, si hay dos clases con el mismo nombre `Util` en diferentes paquetes `com.empresa1` y `com.empresa2`, puedes utilizar el FQN para referirte a cada una de ellas de manera específica:

```java
com.empresa1.Util util1 = new com.empresa1.Util();
com.empresa2.Util util2 = new com.empresa2.Util();
```

En general, el FQN es una forma segura y precisa de referirse a clases en Java, especialmente cuando necesitas trabajar con clases de diferentes paquetes que tienen nombres similares. Sin embargo, en la mayoría de los casos, el uso de importaciones de clases adecuadas hace que sea más cómodo y legible trabajar con clases sin la necesidad de utilizar el FQN en todo momento.


### Declaración de un Paquete:

La declaración de un paquete se realiza al comienzo de un archivo fuente Java utilizando la palabra clave `package`. La declaración del paquete debe ser la primera línea de código en el archivo. Por ejemplo:
```java
package com.miempresa.miprograma;

public class MiClase {
    // Contenido de la clase
}
```

En este ejemplo, la clase `MiClase` pertenece al paquete `com.miempresa.miprograma`.


#### Importación de Clases:

La importación de clases te permite utilizar clases de otros paquetes en tu código sin tener que usar el **Full Qualified Name** (FQN) en todas partes. Puedes importar clases específicas, todas las clases de un paquete o incluso tipos específicos dentro de una clase.

- **Importar una Clase Específica**:
	```java
	import com.otraempresa.otropaquete.ClaseEspecifica;
	
	public class MiClase {
	    ClaseEspecifica instancia = new ClaseEspecifica();
	}
	```

- **Importar Todas las Clases de un Paquete**:
	```java
	import com.otraempresa.otropaquete.*;
	
	public class MiClase {
	    Clase1 instancia1 = new Clase1();
	    Clase2 instancia2 = new Clase2();
	    // ...
	}
	```

- **Importar Tipos Específicos dentro de una Clase**:
	```java
	import java.util.List;
	import java.util.ArrayList;
	
	public class MiClase {
	    List<String> lista = new ArrayList<>();
	}
	```

Recuerda que el uso de `*` para importar todas las clases de un paquete puede aumentar la ambigüedad en el código, por lo que es recomendable importar solo las clases necesarias.

En resumen, declarar paquetes y realizar importaciones de clases son esenciales para organizar y usar eficientemente las clases en Java. Utiliza estas herramientas para evitar conflictos de nombres, mejorar la legibilidad y la organización del código, y facilitar el uso de clases y componentes de otros paquetes en tu proyecto.


## Modificadores de Acceso en Java

En Java, los modificadores de acceso determinan la visibilidad y accesibilidad de clases, métodos, variables y otros miembros dentro del mismo paquete o en paquetes externos. Hay cuatro modificadores de acceso principales:

1. **public**: Los miembros declarados como `public` son accesibles desde cualquier lugar, ya sea dentro de la misma clase, dentro de otras clases del mismo paquete o en clases de paquetes externos. Es el nivel de acceso más alto.
	```java
	package com.miempresa.miproyecto;
	
	public class ClaseA {
	    public int variablePublica = 10;
	
	    public void metodoPublico() {
	        System.out.println("Método público");
	    }
	}
	```

2. **protected**: Los miembros declarados como `protected` son accesibles dentro de la misma clase, dentro de otras clases del mismo paquete y en clases derivadas (subclases) de cualquier paquete. Este modificador también es útil para el concepto de herencia.
	```java
	package com.miempresa.miproyecto;
	
	public class ClaseB {
	    protected int variableProtegida = 20;
	
	    protected void metodoProtegido() {
	        System.out.println("Método protegido");
	    }
	}
	```

3. **default (package-private)**: Si no se especifica ningún modificador de acceso (también conocido como "package-private"), el miembro es accesible solo dentro del mismo paquete.
	```java
	package com.miempresa.miproyecto;
	
	class ClaseC {
	    int variableDefault = 30;
	
	    void metodoDefault() {
	        System.out.println("Método default");
	    }
	}
	```

4. **private**: Los miembros declarados como `private` son accesibles solo dentro de la misma clase. No se pueden acceder desde otras clases, ni siquiera dentro del mismo paquete.
	```java
	package com.miempresa.miproyecto;
	
	public class ClaseD {
	    private int variablePrivada = 40;
	
	    private void metodoPrivado() {
	        System.out.println("Método privado");
	    }
	}
	```

En resumen, ==los modificadores de acceso en Java determinan cómo se acceden y se comparten los miembros de una clase.== Cada modificador tiene un alcance específico para la visibilidad de los miembros, lo que permite controlar el acceso a las partes internas de las clases. Es importante elegir el modificador de acceso adecuado según los requisitos de diseño y la seguridad de tu programa.
También mencionar que los modificadores pueden ser usados en la definición de la clase, atributo, constructor y método.


## Java ARchive

Los archivos JAR (Java ARchive) ==son archivos comprimidos que contienen clases de Java, recursos y metadatos, organizados de manera estructurada.== Los archivos JAR son una forma común de empaquetar y distribuir bibliotecas, aplicaciones y componentes en el mundo de Java. Son especialmente útiles para compartir y distribuir conjuntos de clases y recursos de manera eficiente.


#### Estructura de un Archivo JAR:

Un archivo JAR es un archivo comprimido en formato ZIP que sigue una estructura específica. Puede contener:

1. **Clases y paquetes**: Los archivos JAR pueden contener clases Java organizadas en paquetes. Esto facilita la distribución de bibliotecas o aplicaciones que constan de varias clases.
2. **Recursos**: Los recursos como imágenes, archivos de configuración y archivos de propiedades pueden estar incluidos en un archivo JAR.
3. **Metadatos**: Los archivos JAR pueden contener archivos de metadatos, como el archivo `MANIFEST.MF`, que contiene información sobre el archivo JAR y puede especificar detalles como la clase principal para ejecutar.


#### Ventajas de los Archivos JAR:

1. **Empaquetamiento eficiente**: Los archivos JAR permiten comprimir y empaquetar clases y recursos en un solo archivo, lo que facilita su distribución y reducción del tamaño.
2. **Gestión de dependencias**: Los archivos JAR son ampliamente utilizados para distribuir bibliotecas y componentes que otros proyectos pueden utilizar. Esto ayuda a gestionar las dependencias y garantizar que las clases requeridas estén disponibles.
3. **Distribución portátil**: Los archivos JAR se pueden ejecutar en diferentes plataformas, siempre que exista una máquina virtual de Java (JVM) compatible.
4. **Integración con herramientas**: Muchas herramientas de desarrollo y entornos de ejecución de Java están diseñados para trabajar con archivos JAR, lo que simplifica la compilación, la distribución y la ejecución de aplicaciones.

#### Creación de Archivos JAR:

Puedes crear un archivo JAR utilizando la herramienta `jar` proporcionada con el JDK de Java. Para crear un archivo JAR, sigue estos pasos:

1. **Compila tus clases**: Asegúrate de tener las clases y recursos que deseas incluir en el archivo JAR compilados y listos.
2. **Crea el archivo JAR**: Utiliza el comando `jar` para crear el archivo JAR. Por ejemplo:
   ```sh
   jar cf miarchivo.jar clase1.class clase2.class recurso1.png
   ```

   Esto creará un archivo JAR llamado `miarchivo.jar` que contiene `clase1.class`, `clase2.class` y `recurso1.png`.
3. **Agrega metadatos (opcional)**: Si deseas especificar información adicional, como la clase principal para ejecutar, puedes crear un archivo `MANIFEST.MF` y agregarlo al archivo JAR.


##### Eclipse

1. En Eclipse, haciendo clic derecho en el _proyect_, seleccione la opción **export**. Se mostrarán varias opciones de exportación, seleccione las que están dentro del grupo **java** y dentro de ella la opción **JAR File** haga clic en _"NEXT"_. Veamos el siguiente paso a seguir.
2. En el proyecto , seleccione solo la carpeta _src_. También desmarque los archivos .classpath y .project. Asegúrese de que solo esté marcada la opción "**Export generated class files and resources**". En "Jar File", seleccione una carpeta de fácil acceso en la que se guardará el archivo jar que vamos a crear. Haga clic en _Finish_ y, si se muestra alguna advertencia, ignórela por completo.
3. Verifique la existencia del archivo jar creado.
4. Con el botón derecho en el nuevo proyecto, elija New -> Folder. Para el nombre del folder, elija ***libs***.
5. Copie el jar exportado en la carpeta libs recién creada.
6. Copiar el archivo jar en un proyecto no es suficiente, debe estar en el _class path_. Haga clic con el botón derecho en el archivo jar dentro de la carpeta libs y elija la opción _add to build path_. Vea si seleccionó la opción "_Package Explorer_". Si tiene la opción _Navigator_ seleccionada, no aparecerá _Build Path_


### Uso de Archivos JAR

Para usar un archivo JAR en tu aplicación, generalmente necesitas agregarlo al classpath o incluirlo como una dependencia en un sistema de construcción como Maven o Gradle. Luego, puedes importar y utilizar las clases y recursos del archivo JAR en tu código Java.

En resumen, los archivos JAR son una forma conveniente de empaquetar y distribuir clases, recursos y metadatos en el mundo de Java. Son ampliamente utilizados para compartir bibliotecas y aplicaciones, lo que facilita la gestión de dependencias y la portabilidad entre diferentes entornos de desarrollo y ejecución.


## Maven

Java es una plataforma de desarrollo completa que destaca por su gran cantidad de proyectos de código abierto (_open source_). Para la mayoría de problemas en el día a día del desarrollador ya existen librerías para solucionar. Es decir, si te gustaría conectarte con una base de datos, o trabajar en desarrollo web, en el área de ciencia de datos, creación de servicios o Android, ya existen librerías para esto, muchas veces más de una.

Existe la necesidad de organizar, centralizar y versionar los JARs de esas librerías y administrar las dependencias entre ellos. Para solucionar esto, se crearon herramientas específicas y en el mundo Java se destacó **Maven**. Maven organiza los JARs (código compilado, código fuente y documentación) en un repositorio central que es público y se puede buscar:

[mvnrepository.com](https://mvnrepository.com/)

Allí puede ver e incluso descargar los archivos JARs, pero lo mejor es que la herramienta Maven puede hacer esto por usted.

Nota: si es un usuario de Linux, Maven es muy similar a los administradores de _apt_ o _rpm_. En MacOS existe _brew_ con el mismo propósito. En el mundo .Net tenemos _nuget_ y la plataforma node.js usa _npm_. La gestión de dependencias es un problema cotidiano para el desarrollador, y cada sistema o plataforma tiene su propia solución.


---

+ #librerias
+ #IDE 
+ #encapsulamiento 
