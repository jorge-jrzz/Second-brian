---
banner_icon: 🌔
banner: "![[skylab-19731979_8980505837_o.jpg]]"
banner_y: 0.468
---

# Instalación del IDE Eclipse

1. **Descarga Eclipse**: Ve al sitio web oficial de Eclipse en este [link](https://www.eclipse.org/downloads/) y busca la versión de Eclipse que deseas descargar. Hay diferentes versiones disponibles, como Eclipse IDE for Java Developers o Eclipse IDE for Enterprise Java Developers. Elige la versión adecuada para tus necesidades y descárgala.

2. **Elige tu plataforma**: En la página de descargas de Eclipse, asegúrate de seleccionar la versión compatible con tu sistema operativo. Eclipse está disponible para Windows, macOS y Linux. Haz clic en el enlace de descarga correspondiente a tu plataforma.

3. **Descomprime el archivo**: Una vez que la descarga haya finalizado, descomprime el archivo ZIP que has descargado en una ubicación de tu elección en tu sistema.

4. **Inicia Eclipse**: Ve a la carpeta donde has descomprimido Eclipse y busca el archivo ejecutable "eclipse" o "eclipse.exe" dependiendo de tu sistema operativo. Haz doble clic en el archivo para iniciar Eclipse.

5. **Selecciona una carpeta de trabajo**: Al iniciar Eclipse por primera vez, se te pedirá que elijas una carpeta de trabajo (workspace) donde se guardarán tus proyectos. Puedes elegir una carpeta existente o crear una nueva. Se recomienda que elijas una carpeta dedicada para tus proyectos de Eclipse.

6. **Configuración inicial**: Una vez que hayas seleccionado una carpeta de trabajo, Eclipse se abrirá y te presentará una pantalla de bienvenida. Puedes personalizar tu configuración inicial según tus preferencias o simplemente seleccionar la opción predeterminada para comenzar.

# Primeros pasos en Eclipse

1) Cuando iniciamos Eclipse, nos pedirá que seleccionemos un " workspace ", que es donde se almacenarán tus proyectos. Si deseas personalizar esto, haz clic en Examinar ... y selecciona tu carpeta. 

2) Cierra la página de Welcome y comenzaremos Eclipse de la forma en que normalmente lo encontramos.

3) Haz clic en File y coloca el cursor en la línea new y verás que Eclipse nos dará algunas opciones. Elige Java project.

4) En esta nueva ventana, nombraremos nuestro proyecto, elegiremos el nombre sintaxe-basica, recuerda verificar la versión de Java utilizada.

5) Observa que tenemos un nuevo proyecto en View `Package Explorer`, guardaremos nuestro proyecto en esta carpeta `src` que se creó.

6) En el directorio `src`, haz clic derecho, coloca el cursor en new y elige `class`.

7) En esta nueva ventana, crearemos la clase con el nombre Programa, no te preocupes por las diversas opciones que nos ofrezca Eclipse. Haz clic en finish y tendremos nuestra clase de programa.

8) Antes de colocar `System.out.println`, escribe el método main. Ten la seguridad de que entenderemos mejor el método main durante el curso. Nuestro código se verá así:

	```java
	public class Programa {
	
	    public static void main(String[] args){
	        System.out.println("Hola mundo");
	    }
	
	}
	```

9) Ten en cuenta que, durante la escritura, Eclipse intenta inferir algunas cosas, además de cerrar las comillas automáticamente.

10) Para ejecutar nuestro código, en la parte superior de Eclipse, haz clic en Run, luego en Run As y elige Java Application.

## Preguntas

+ ==Podemos programar en Java usando editores de texto e IDEs. En este contexto, tenemos las siguientes declaraciones:==
	1. Un IDE es un entorno de desarrollo integrado que centraliza en un solo lugar el compilador del lenguaje utilizado, el editor de texto, la documentación, la base de datos y todo lo que gira en torno a la creación de aplicaciones.
	3. NetBeans e Intellij son otros IDEs famosos en el mundo de Java.

+ ==¿Qué sabemos sobre el workspace (espacio de trabajo)?==
	+ Un workspace es la carpeta predeterminada que se usará para almacenar todos los proyectos creados con el IDE de Eclipse, entonces un workspace es como una carpeta para varios proyectos.
	+ Cada proyecto Eclipse está dentro de un workspace, un proyecto siempre está dentro de un espacio de trabajo.
+ ==Afirmaciones sobre Eclipse:==
	+ La salida de nuestro programa ejecutado por Eclipse se realiza a través de la view console.
	+ Ejecutamos nuestro programa en Eclipse a través del menú Run -> Run as -> Java Application. Incluso hay una tecla de acceso directo, que se muestra durante la opción que varía según su sistema operativo.
	+ Dentro de un proyecto Java, creamos una nueva clase a través de la opción de menú File -> New -> Class.
	  Si el proyecto no es un proyecto Java, la opción Clase no estará disponible, ¡mantente atento!