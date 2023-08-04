---
banner_icon: 💊
banner: "![[apollo-11-astronauts-visiting-the-pope_7678546440_o.jpg]]"
banner_y: 0.564
---

# enums

Los enums (enumeraciones) en Java son una forma de definir un tipo de dato especial que ==consta de un conjunto fijo de constantes con nombre==. Un enum se utiliza para representar un grupo de valores constantes relacionados, y su objetivo principal es mejorar la legibilidad y la claridad del código.

Para definir un enum en Java, se utiliza la palabra clave `enum`, seguida de los valores constantes entre llaves. Cada valor constante se define como un identificador seguido de paréntesis, y el enum se cierra con un punto y coma al final.

Veamos un ejemplo sencillo de cómo se define y utiliza un enum:

```java
public enum DiaSemana {
    LUNES,
    MARTES,
    MIERCOLES,
    JUEVES,
    VIERNES,
    SABADO,
    DOMINGO
}
```

En este ejemplo, hemos creado un enum llamado `DiaSemana`, que representa los días de la semana como constantes. Cada día de la semana es una constante del enum.

Algunas características importantes de los enums en Java son:

1. Enumeraciones como tipos: Los enums son tipos de datos en sí mismos. Pueden ser utilizados como el tipo de una variable, lo que permite definir variables que solo pueden tomar valores de las constantes definidas en el enum.
	```java
	public class EjemploEnum {
	    public static void main(String[] args) {
	        DiaSemana dia = DiaSemana.MARTES;
	        System.out.println("Hoy es " + dia);
	    }
	}
	```

2. Métodos en enums: Los enums pueden tener métodos, lo que permite agregar comportamientos específicos a cada valor constante.
	```java
	public enum EstadoCivil {
	    SOLTERO("Soltero/a"),
	    CASADO("Casado/a"),
	    DIVORCIADO("Divorciado/a"),
	    VIUDO("Viudo/a");
	
	    private final String descripcion;
	
	    EstadoCivil(String descripcion) {
	        this.descripcion = descripcion;
	    }
	
	    public String getDescripcion() {
	        return descripcion;
	    }
	}
	```

	En este ejemplo, el enum `EstadoCivil` tiene un método `getDescripcion()` que devuelve la descripción asociada a cada valor constante.

3. Comparaciones: Los enums se pueden comparar directamente utilizando el operador de igualdad (`==`), lo que los hace útiles para estructuras de control como `switch`.
	```java
	DiaSemana dia = DiaSemana.MIERCOLES;
	
	switch (dia) {
	    case LUNES:
	        // Hacer algo para el lunes
	        break;
	    case MARTES:
	        // Hacer algo para el martes
	        break;
	    // ...
	    default:
	        // Hacer algo para otros días
	}
	```

En resumen, los enums en Java son una forma de definir un conjunto fijo de constantes con nombre que representan valores relacionados. Son útiles para mejorar la legibilidad y la claridad del código, y se utilizan comúnmente para representar tipos de datos que tienen un conjunto limitado de opciones. Los enums también pueden tener métodos y se pueden utilizar en estructuras de control como `switch`. 

---

+ #constantes
+ #enums