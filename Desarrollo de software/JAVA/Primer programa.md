---
banner_icon: 📝
banner: "![[the-eagle-nebula_9467314848_o.jpg]]"
banner_y: 0.696
---

# ¿Que son la JVM, JRE y JDK?

- La **JVM** (Java Virtual Machine) es una máquina virtual que interpreta y ejecuta el bytecode Java. Proporciona un entorno de ejecución independiente de la plataforma y es responsable de cargar, verificar y ejecutar el código Java. La JVM se encarga de la gestión de memoria, la ejecución del programa y la optimización del código. Es el componente clave para ejecutar aplicaciones Java en diferentes sistemas operativos y arquitecturas de hardware.

- El **JRE** (Java Runtime Environment) es un conjunto de herramientas y bibliotecas que incluye la JVM, junto con otros componentes necesarios para la ejecución de aplicaciones Java. Proporciona un entorno de tiempo de ejecución completo para ejecutar aplicaciones Java, pero no incluye herramientas de desarrollo como compiladores y depuradores. El JRE es utilizado por los usuarios finales que solo necesitan ejecutar aplicaciones Java y no están involucrados en el desarrollo de software.

	==JRE = JVM + Librerías==

- El **JDK** (Java Development Kit) es un paquete completo para el desarrollo de aplicaciones Java. Incluye el JRE, la JVM y una serie de herramientas de desarrollo, como el compilador de Java (javac), el depurador (jdb) y otras utilidades. El JDK se utiliza por los desarrolladores de software para escribir, compilar, depurar y ejecutar aplicaciones Java. Proporciona todas las herramientas necesarias para el desarrollo y es esencial para crear nuevas aplicaciones en Java.

	==JDK = JRE + Herramientas de desarrollo==

Es importante resaltar que no se puede descargar la JVM individualmente. Siempre tendremos que descargar el JRE que tiene la JVM y el conjunto de librerías. 

En resumen, la JVM es responsable de ejecutar el bytecode Java, el JRE proporciona un entorno de ejecución para las aplicaciones Java y el JDK es un conjunto completo de herramientas para el desarrollo de aplicaciones Java, que incluye el JRE y herramientas de desarrollo adicionales.

![[JDK.png]]

# Configurar Java

### <mark class="hltr-green">Linux</mark>

En la terminal, ejecutamos el siguiente comando para actualizar la lista de paquetes disponibles para descargar en los repositorios del sistema:

```bash
sudo apt update
```

![img](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/linux1.png)

Una vez hecho esto, instalaremos la versión 17 del JDK mediante el siguiente comando:

```bash
sudo apt install openjdk-17-jdk
```

![img linux2](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/linux2.png)

De esta manera, el sistema descargará e instalará el paquete OpenJDK 17 JDK, lo que permitirá al usuario comenzar a desarrollar aplicaciones Java en Linux. Después de finalizar este proceso de instalación, ahora necesitamos configurar la variable de entorno JAVA_HOME, que se utiliza para indicar la ruta de instalación del JDK. Esto es necesario para utilizar los recursos del JDK, como javac.

Para ello, ejecutamos el comando sudo update-alternatives --config java, que mostrará la ruta donde se instaló el JDK.

![img](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/linux3.png)

Ahora, copiamos esta ruta hasta /bin, por ejemplo: /usr/lib/jvm/java-17-openjdk-amd64/bin, y en tu terminal escribe el comando: export JAVA_HOME= seguido de la ruta que copiaste de la instalación del JDK, sin dejar espacios.

Por ejemplo:

```bash
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64/bin
```

![img](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/linux4.png)

Presionamos la tecla "enter" y listo, el JDK está instalado y configurado. Para probarlo, escribe los siguientes comandos en la terminal:

```bash
javac -version
java -version
```

![Img linux5.png](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/linux5.png)

### <mark class="hltr-green">Mac</mark>

1) Para instalar en Mac, puedes acceder al sitio web de Oracle ([Java Downloads | Oracle](https://www.oracle.com/java/technologies/downloads/)) o buscar en el navegador "Java Download Oracle" y acceder al primer enlace.

2) Ahora, necesitamos elegir la versión de Java.

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/1e3.png)

3) Selecciona Mac como sistema operativo y realiza la descarga.

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/2.png)

### Windows

1) Para instalar en Windows, puedes acceder al sitio web de Oracle([Java Downloads | Oracle](https://www.oracle.com/java/technologies/downloads/)) o buscar en el navegador "Java Download Oracle" y acceder al primer enlace.

2) Ahora, necesitamos elegir la versión de Java. En este curso utilizaremos Java 17 LTS, que es la versión de soporte a largo plazo más reciente para la plataforma Java SE.

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/1e3.png)

3) Selecciona Windows como sistema operativo y realiza la descarga.

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/4.png)

4) Una vez descargado, ejecuta el instalador y continúa con la instalación.

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/5.png)

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/6.png)

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/7.png)

5) Después de la instalación, vamos a probar nuestro Java. Para hacer esto, utilizaremos la ventana de comandos. Prueba los siguientes comandos y verifica si todo ha salido como se esperaba

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/8.png)

Configuración de **la variable PATH en Windows**:

1) Ve al panel de control y busca "Sistema", luego haz clic en "Configuración avanzada del sistema".

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/img1.png)

2) En la pestaña "Avanzado", haz clic en "Variables de entorno".

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/img2.png)

3) Ahora se abrirá una nueva ventana en la parte inferior de la pantalla, selecciona la variable de entorno llamada "Path" y haz clic en "Editar".

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/img3.png)

4) En esta nueva ventana, haz clic en el botón "Nuevo" y en la línea que se ha seleccionado, coloca la ruta hacia el directorio "bin" dentro de la carpeta "jdk", que se encuentra dentro de la carpeta "Java".

![](https://caelum-online-public.s3.amazonaws.com/1736-java/Imagens+JDK/img4.png)

5) Una vez hecho esto, cierra la ventana de comandos y ábrela nuevamente. Prueba los siguientes comandos:

```bash
java -version
javac -version
```

# Primer programa en Java

1) El comando utilizado para imprimir algo en la pantalla es `System.out.println`, pero no será suficiente para que el programa lo compile. Hasta ahora tenemos:
	```java
	System.out.println("Hola mundo");
	```

2) Para compilar nuestro código, primero envuélvelo con una clase, así:
	```java
	public class Programa {
	    System.out.println("Hola mundo");
	}
	```

3) Nuestro programa aún no compila, para que funcione, se coloca el método ==main==, no te preocupes por el método `Main` ahora, durante el curso veremos los detalles y entenderemos este método. Tendremos un código como este:

	```java
	public class Programa {
	
	    public static void main(String[] args){
	        System.out.println("Hola mundo");
	    }
	
	}
	```

4) Después de hacer esto, se guarda el archivo como `Programa.java` en algún directorio. ¡El nombre debe ser exactamente el mismo que el nombre de la clase creada, incluyendo letras mayúsculas y minúsculas! Recuerda que Java es case-sensitive, distingue entre mayúsculas y minúsculas.

5) Ahora, compila el código usando el compilador Java de Oracle, llamado `javac`. Esto nos dará el bytecode:
	```bash
	javac Programa.java
	```

6) Después de compilar, podemos ver que el bytecode se generó con el mismo nombre, pero con .class al final.

7) Ejecuta el programa ya compilado escribiendo:
	```bash
	java Programa
	```

Cuando escribimos solo Java, estamos invocando la máquina virtual para interpretar nuestro programa.

Después de eso, tendremos la frase `Hola mundo`.

# ¿Cómo funcionan las versiones en Java?

Java es un lenguaje de programación que se actualiza periódicamente por Oracle, la empresa responsable de su desarrollo. Cada nueva versión de Java trae consigo nuevas características, mejoras de rendimiento, correcciones de errores y actualizaciones de seguridad. Estas versiones se numeran, siguiendo un patrón específico.

Cuando se lanza una nueva versión, puede incluir nuevas bibliotecas, clases, métodos y otros recursos que los desarrolladores pueden utilizar para crear aplicaciones Java más eficientes y con menos errores.

Aquí hay algunos ejemplos de algunas de las principales versiones de Java y sus características:

**Java 8**: Introdujo la programación funcional, incluyendo la interfaz java.util.function, que permite el uso de expresiones lambda. Además, se agregó una nueva API de fecha y hora que proporciona una forma más simple y segura de manejar fechas y horas.

**Java 11**: Introdujo el sistema de módulos de Java, que ayuda a simplificar la creación y mantenimiento de aplicaciones complejas. Además, se agregó la clase HttpClient, que admite comunicaciones HTTP/2.

**Java 15**: Agregó características como la palabra clave sealed, que permite que las clases restrinjan qué otras clases pueden extenderlas o implementarlas, y también agregó mejoras a la API Records, que ayuda a simplificar la creación de clases de datos inmutables.

**Java 17**: introduce nuevas características y mejoras, como patrones de coincidencia que mejoran la sintaxis al trabajar con estructuras de datos complejas. Además, se mejoran el rendimiento del recolector de basura para reducir la latencia en las aplicaciones Java. También se agregan funcionalidades a los registros, que son clases inmutables y compactas utilizadas para representar datos, incluyendo la capacidad de definir registros locales dentro de métodos. Otra adición importante son las nuevas clases y métodos en el paquete java.util para trabajar con estructuras de datos persistentes, lo que permite realizar cambios en los datos sin modificar las estructuras originales. Por último, se agrega soporte para CGroups en la API de Java, lo que permite una mejor administración de recursos en entornos de contenedores.

Al actualizar a una nueva versión de Java, es importante tener en cuenta la compatibilidad con versiones anteriores. A veces, se eliminan o modifican características o funcionalidades en una nueva versión, lo que puede afectar el código existente. Por esta razón, es importante probar su código al actualizar a una nueva versión de Java.

Además, es posible que coexistan diferentes versiones de Java en un sistema, lo que permite que las aplicaciones se ejecuten en versiones específicas de la JVM (Java Virtual Machine) para garantizar la compatibilidad con el código existente.

## Preguntas

+ ==¿Cuál de las siguientes afirmaciones son correctas acerca de JRE y JDK?==

	1. El JDK es el ambiente para ejecutar aplicaciones Java y además posee varias herramientas de desarrollo. El JDK son las herramientas de desarrollo (como el compilador) y también tiene el JRE incluido.
	2. EL JRE es el ambiente para ejecutar una aplicación Java. Si solo queremos ejecutar una aplicación Java, el JRE (Java Runtime Environment) es suficiente.

+ Ana está comenzando a desarrollar en Java y ya aprendió que la entrada de una aplicación es siempre la función (o método) `main`. Sin embargo, ella no recuerda cual era la definición correcta (palabras reservadas y parámetros) de aquella función/método.

	```java
	class Programa {
	
	    ??? main ??? {
	        System.out.println("¿Puedes ayudar a Ana?");
	    }
	
	}
	```

	==¿Cuál es la definición correcta?==
    
    ```java
    public static void main(String[] args)
    ```
    
    ¡Correcto! Aún no sabemos que significan todas esas palabras, pero tranquilo, va a quedar claro después. En este momento, solo nos basta saber que la entrada de una aplicación Java es siempre la función/método `public static void main(String[] args)`

+ Lea las siguientes afirmaciones sobre compilación y ejecución de código Java:

	1. Durante la compilación ocurre una verificación sintáctica del código fuente.
	2. En la compilación y ejecución pueden aparecer errores.
	3. La JVM ejecuta Bytecode.
	4. El compilador genera Bytecode en caso el código fuente no presente ningún error sintáctico.
	==¿Cuál o cuáles de esas afirmaciones son verdaderas?==
	Todas son verdaderas.

+ Pedro esta trabajando por primera vez con el sistema operativo Linux, pero está sorprendido, pues el computador no tiene interfaz gráfica, (solo funciona con línea de comandos).
	Ahora, él necesita compilar y ejecutar código Java en esa línea de comandos, pero olvidó los comandos.

	Archivo `Programa.java`:
	
	```java
	class Programa {
	
	    public static void main(String[] args) {
	        System.out.println("Funcionooo!!!");
	    }
	
	}
	```

	==¿Qué comandos debe usar para compilar y ejecutar ese código Java?==
    
    ```bash
    javac Programa.java
    java Programa
    ```
    
    Nota que se pasa la extensión del archivo (`.java`) para el comando `javac`:
    ```bash
    javac Programa.java
    ```
    
    Y para llamar a la JVM usamos solo el nombre de la clase (sin extensión):
    ```bash
    java Programa
    ```