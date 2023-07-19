---
banner_icon: 🚔
banner: "![[lunar-rover_29798990354_o.jpg]]"
banner_y: 0.384
---

# Polimorfismo

## Introducción

El polimorfismo es un concepto fundamental en la Programación Orientada a Objetos (POO) que permite tratar objetos de diferentes clases de manera uniforme a través de una interfaz común. Es una de las características clave de la POO que promueve la flexibilidad, la reutilización de código y el diseño modular.
==En términos simples, el polimorfismo implica la capacidad de un objeto de adoptar muchas formas diferentes. Esto significa que un objeto puede ser referenciado como su tipo base (clase padre) o como uno de sus tipos derivados (clases hijas)==. Al hacerlo, se puede utilizar una referencia de tipo base para acceder a los métodos y atributos comunes a todas las clases en la jerarquía de herencia, y también aprovechar el comportamiento específico de cada clase hija.

El polimorfismo se basa en dos conceptos clave:

1. **Herencia**: La herencia permite que una clase hija herede los atributos y métodos de su clase padre. Esto crea una relación de tipo generalización/especialización entre las clases, donde la clase hija es un tipo más específico de la clase padre. El polimorfismo aprovecha esta relación para tratar objetos de diferentes clases hijas como objetos de la clase padre, lo que facilita la flexibilidad en el diseño y el uso de la jerarquía de clases.
2. **Sobreescritura de métodos**: La sobreescritura de métodos permite que una clase hija redefina un método heredado de la clase padre para proporcionar una implementación específica de la clase hija. Esto significa que se puede tener el mismo método con la misma firma en diferentes clases de una jerarquía de herencia, pero con comportamientos diferentes. Al utilizar polimorfismo, se puede llamar al método de una clase hija a través de una referencia de tipo base, y la implementación correcta del método se ejecutará automáticamente en tiempo de ejecución.

El polimorfismo se beneficia de la capacidad de Java para enlazar dinámicamente los métodos en tiempo de ejecución, lo que permite determinar qué implementación de un método se debe utilizar en función del tipo real del objeto en tiempo de ejecución.
Los beneficios del polimorfismo incluyen la reutilización de código, la simplificación del diseño y la legibilidad del código, y la capacidad de extender y mantener fácilmente el código. Además, el polimorfismo facilita la implementación de patrones de diseño como el patrón de diseño de fábrica, el patrón de diseño de estrategia y el patrón de diseño de observador.

En resumen, el polimorfismo es una característica poderosa de la POO que permite tratar objetos de diferentes clases de manera uniforme a través de una interfaz común. Proporciona flexibilidad en el diseño, reutilización de código y modularidad. Aprovechando la herencia y la sobreescritura de métodos, el polimorfismo facilita el desarrollo de software más flexible, escalable y mantenible.

##### Ejemplo
Supongamos que tenemos una clase `Animal` como clase padre, y dos clases hijas: `Perro` y `Gato`. La clase `Animal` tiene un método llamado `hacerSonido()`, mientras que las clases `Perro` y `Gato` sobrescriben este método para proporcionar su propio sonido específico.
```java
// Clase padre
public class Animal {
    public void hacerSonido() {
        System.out.println("Animal hace un sonido");
    }
}

// Clase hija Perro
public class Perro extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("Guau guau!");
    }
}

// Clase hija Gato
public class Gato extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("Miau miau!");
    }
}
```

Ahora, en el código principal, podemos crear una lista de objetos `Animal` que incluya tanto objetos `Perro` como objetos `Gato`. Utilizando el polimorfismo, podemos tratar estos objetos de diferentes clases hijas como si fueran objetos de la clase padre:
```java
public class Main {
    public static void main(String[] args) {
        Animal animal1 = new Perro();
        Animal animal2 = new Gato();

        animal1.hacerSonido(); // Salida: Guau guau!
        animal2.hacerSonido(); // Salida: Miau miau!
    }
}
```

En este ejemplo, creamos dos objetos: `animal1` es una instancia de la clase `Perro` y `animal2` es una instancia de la clase `Gato`. Ambos objetos son referenciados a través de una variable de tipo `Animal`, lo que demuestra el polimorfismo.

Cuando llamamos al método `hacerSonido()` en `animal1` y `animal2`, Java automáticamente seleccionará la implementación correcta del método en tiempo de ejecución. Esto es posible gracias a la sobreescritura de métodos en las clases hijas. A pesar de que la variable `animal1` se refiere a un objeto `Perro` y la variable `animal2` se refiere a un objeto `Gato`, ambos objetos son tratados como objetos de la clase padre `Animal` y el método `hacerSonido()` correspondiente a cada clase hija es ejecutado.
Este es un ejemplo básico de cómo el polimorfismo permite que objetos de diferentes clases hijas sean tratados de manera uniforme a través de una interfaz común proporcionada por la clase padre. El polimorfismo es una característica poderosa que facilita el diseño flexible y modular de programas en Java.

---

* #polimorfismo