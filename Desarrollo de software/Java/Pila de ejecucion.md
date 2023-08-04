---
banner_icon: 🥇
banner: "![[cernan-driving-the-rover_9457449367_o.jpg]]"
banner_y: 0.312
---

# Pila de ejecución

La pila de ejecución es una estructura de datos que se utiliza para almacenar información sobre las llamadas a funciones en un programa en ejecución. La pila se organiza como una pila, con la función actual en la parte superior de la pila y las funciones llamadas por la función actual en la parte inferior de la pila.

Cuando una función se llama, su dirección se almacena en la parte superior de la pila. Cuando la función finaliza, su dirección se elimina de la parte superior de la pila. La función en la parte inferior de la pila entonces se reanuda.

La pila de ejecución se utiliza para mantener el estado de las funciones en ejecución. Esto incluye la dirección de la función, los parámetros de la función y los valores de retorno de la función.

La pila de ejecución también se utiliza para implementar el control de flujo de un programa. Cuando una función llama a otra función, la dirección de la función actual se almacena en la pila y la dirección de la función llamada se carga en la pila. Cuando la función llamada finaliza, su dirección se elimina de la pila y la dirección de la función actual se carga en la pila. Esto permite que el programa se ejecute en orden secuencial, incluso cuando se llaman funciones.

La pila de ejecución es una parte importante de cualquier programa en ejecución. Permite que los programas llamen a funciones y manejen el estado de las funciones en ejecución.

A continuación un ejemplo sobre el funcionamiento de la pila de ejecución en Java: 
```java
public class Flujo {

        public static void main(String[] args) {
            System.out.println("Inicio del main");
            metodo1();
            System.out.println("Fin del main");
        }

        private static void metodo1() {
            System.out.println("Inicio del metodo1");
            metodo2();
            System.out.println("Fin del metodo1");
        }

        private static void metodo2() {
            System.out.println("Inicio del metodo2");
            for(int i = 1; i <= 5; i++) {
                System.out.println(i);
            }
            System.out.println("Fin del metodo2");
        }
}
```

El código anterior se puede representar gráficamente la pila de ejecución en de la siguiente manera: 

![[ejemplo_pila_ejecucion.png | 550]]