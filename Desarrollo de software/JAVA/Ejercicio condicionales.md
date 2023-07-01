## Cálculo del valor con descuento

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
