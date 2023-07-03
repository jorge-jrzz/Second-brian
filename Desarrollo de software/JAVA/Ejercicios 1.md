## Condicionales

### Cálculo del valor con descuento

María es propietaria de una tienda de ropa y le gustaría crear un programa que calcule el valor final del producto después de aplicar un descuento que ofrecería a sus clientes.

- Si el valor de la compra está entre $100.0 y $199.99, el descuento es del 10%.
- Si el valor de la compra está entre $200.0 y $299.99, el descuento es del 15%.
- Para compras superiores a $300.0, el descuento es del 20%.

Para comenzar, María escribió el siguiente esquema de clase:

```java
public class TestDescuento {

    public static void main(String[] args) {

        double valorCompra = 250.0;
        // ifs aqui

    }
}
```

Ahora, ¡ayuda a María a implementar todas las reglas usando condicionales!

A continuación, la implementación del instructor:

```java
public class TestDescuento {

    public static void main(String[] args) {

        double valorCompra = 250.0;
        double descuento = 0.0;

        if (valorCompra >= 100.0 && valorCompra < 200.0) {
            descuento = 10.0;
        } else if (valorCompra >= 200.0 && valorCompra < 300.0) {
            descuento = 15.0;
        } else if (valorCompra >= 300.0) {
            descuento = 20.0;
        }

        double valorFinal = valorCompra - (valorCompra * (descuento / 100));

        System.out.println("Valor de la compra: $" + valorCompra);
        System.out.println("Descuento: " + descuento + "%");
        System.out.println("Valor final: $" + valorFinal);
    }
}
```

A continuación mi implementación:
```java
public class TestDescuento {
	public static void main(String[] args) {
		double valorCompra = 250.0;
		if (valorCompra >= 100.0 && valorCompra <= 199.99)
			System.out.println("El descuento es del 10%");
		} else if (valorCompra >= 200.0 && valorCompra <= 299.99) {
			System.out.println("El descuento es del 15%");
		} else if (valorCompra >= 300.0) {
			System.out.println("El descuento es del 20%");
		} else {
			System.out.println("No hay descuento");
		}
	}
}
```

---
## Bucles

### Múltiplos de 3

**Usa un bucle `for` para imprimir todos los múltiplos de 3, entre 1 y 100.**

Consejo: Hay dos formas tradicionales de resolver este problema. Una es hacer el `for` y usar el `número% 3` para encontrar el residuo de dividir un número entre 3 (el operador `%` se llama módulo). Si el residuo es cero, es divisible por 3. Como en:

```java
if (numero% 3 == 0) {
    // hacer algo
}
```

Otro enfoque es hacer un bucle ligeramente diferente, que salta directamente a través de múltiplos de tres. ¡Hay otros enfoques, elige el tuyo e impleméntalo en una nueva clase!

A continuación, la implementación del instructor:
```java 
class MultiplosDeTresHastaCien {

    public static void main (String[] args) {
        for (int i = 3; i < 100; i += 3 ){
            System.out.println(i);
        }
    }

}
```

A continuación mi implementación:
```java
class MultiplosDeTresHastaCien {

    public static void main (String[] args) {
        for (int i = 1; i < 100; i++ ){
            if (i % 3 == 0)    {
                System.out.println(i);
            }
        }
    }

}
```

### Factorial

¿Recuerdas el factorial? ¿No? No hay problema, sigue las reglas:

- El factorial de 0 es 1.
- El factorial de 1 es (0!) * 1 = 1.
- El factorial de 2 es (1!) * 2 = 2
- El factorial de 3 es (2!) * 3 = 6
- El factorial de 4 es (3!) * 4 = 24
- El factorial de un número n es n * n-1 * n-2 ... hasta n = 1.

O sea:

- El factorial de 4! = 1 x 2 x 3 x 4 = 24
- El factorial de 6! = 1 x 2 x 3 x 4 x 5 x 6 = 720

Ahora crea una nueva clase, escribe un _for_ que comience una variable `n` (número actual) como `1` y `factorial` (resultado total) como `1`. ¡Haz su ciclo entre 1 y 10 y calcula el resultado!

A continuación, la implementación del instructor:
```java
class Factorial {

    public static void main(String[] args) {
        int factorial = 1;
        for (int i = 1; i < 11; i++) {
            factorial *= i;
            System.out.println("Factorial de " + i + " = " + factorial);
        }
    }

}
```

El factorial siempre es el producto de números enteros consecutivos de 1 hasta el propio número con el que estamos trabajando. Ejemplo: Factorial de 4 = 4 x 3 x 2 x 1 = 24. Es igual a decir que factorial de 4 = 4 x 3! = 24. Usando esta última lógica podemos resolver algunos problemas, pues vamos usando el número que tenemos multiplicado por el factorial del número anterior.

A continuación mi implementación:
```java
public class factorial {
	public static void main(String[] args) {
		System.out.println("Factorial del 1 al 100");
		int factorial = 1;
		for (int numero = 0; numero <= 10; numero++) {
			if (numero != 0) {
				for (int mul = 1; mul <= numero; mul++) {
					factorial *= mul;
				}
			}
			System.out.println("Factorial de " + numero + ": " + factorial);
			factorial = 1;
		}
	}
}
```