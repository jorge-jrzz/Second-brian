---
banner_icon: 🚗
banner: "![[lunarama_9457461481_o.jpg]]"
banner_y: 0.54
---

# Clases


## Introducción

En Python, una clase es una plantilla para crear objetos. Define una colección de atributos y métodos que se aplican a cada objeto creado a partir de ella.
Para crear una clase, se utiliza la palabra clave **`class`** seguida del nombre de la clase, y se define la clase en un bloque de código indentado debajo. Dentro de la clase se pueden definir atributos y métodos, que son funciones asociadas a la clase.
Por convención, el nombre de una clase en Python comienza con una letra mayúscula.


### Crear objetos a partir de una clase

Una vez definida una clase, se pueden crear objetos a partir de ella. Para ello, se utiliza el nombre de la clase seguido de paréntesis. Esto crea una instancia de la clase, que es un objeto único con sus propios atributos y métodos.
En Python, **`self`** es una convención para referirse a la instancia actual de una clase. En otras palabras, **`self`** es una referencia al objeto en sí mismo. La palabra clave **`self`** se utiliza como el primer parámetro en la definición de métodos de una clase, por ejemplo:
```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad   
```

En este ejemplo, **`self`** se refiere a la instancia actual de la clase **`Persona`**. El método **`__init__`** es un constructor, que se utiliza para inicializar los atributos de una instancia de la clase. **`__init__`** se llama automáticamente cada vez que se crea una nueva instancia de la clase. En este caso, el constructor toma dos parámetros: **`nombre`** y **`edad`**. La referencia **`self.nombre`** es un atributo de instancia, que se refiere al nombre de la persona, y **`self.edad`** es otro atributo de instancia que se refiere a la edad de la persona. Al llamar al constructor de esta manera:
```python
persona = Persona('Juan', 30)
```

**`self.nombre`** se establece en **`'Juan'`** y **`self.edad`** se establece en **`30`** para la instancia actual (**`persona`** en este caso).

En resumen, **`self`** se refiere a la instancia actual de una clase y se utiliza para acceder a los atributos y métodos de esa instancia. El constructor (`__init__`) se utiliza para inicializar los atributos de la instancia y se llama automáticamente cada vez que se crea una nueva instancia de la clase.


## Atributos y métodos

Los atributos son variables que pertenecen a una clase o a un objeto creado a partir de ella. Los métodos son funciones que se definen dentro de una clase y que se utilizan para manipular los atributos de la clase.

Para acceder a los atributos y métodos de un objeto, se utiliza la notación de punto. Por ejemplo:
```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def saludar(self):
        print("Hola, mi nombre es", self.nombre)

p = Persona("Juan", 30)
print(p.nombre) # imprime "Juan"
p.saludar() # imprime "Hola, mi nombre es Juan"
```

En este ejemplo, la clase **`Persona`** tiene dos atributos (**`nombre`** y **`edad`**) y un método (**`saludar`**). El método **`__init__`** se utiliza para inicializar los atributos de la clase al crear un objeto.


### Propiedades de las clases

Si se define la clase **`Coche`** de la siguiente manera:
```python
class Coche:
    ruedas = 4
```

Estamos definiendo una propiedad de clase llamada **`ruedas`** y le se le esta asignando el valor 4. ==Esta propiedad es compartida por todas las instancias== de la clase **`Coche`**, lo que significa que si creas dos objetos **`Coche`**, ambos tendrán la propiedad **`ruedas`** con el valor 4.
Se puede acceder a esta propiedad de clase directamente a través de la clase, por ejemplo:
```python
print(Coche.ruedas) # Salida: 4
```

También se puede acceder a ella a través de una instancia de la clase:
```python
mi_coche = Coche()
print(mi_coche.ruedas) # Salida: 4
```

En este caso, Python busca la propiedad **`ruedas`** en la instancia de **`mi_coche`**, pero como no existe, la busca en la clase **`Coche`** y la encuentra allí.
De igual manera, este atributo se puede actualizar, ya sea para un objeto en particular o para toda la clase:
```python
mi_coche.ruedas = 2 # El objeto mi_coche ahora tiene 2 ruedas
Coche.ruedas = 8 # Ahora todas las instancias de la clase Coche tentran 8 ruedas
```


### Métodos de clase

Los métodos de clase ==son métodos que pertenecen a la clase en sí misma en lugar de a las instancias individuales de la clase.== A diferencia de los métodos de instancia que operan en objetos específicos creados a partir de la clase, los métodos de clase actúan en la clase misma y tienen acceso a sus atributos y otros métodos.
Los métodos de clase se definen utilizando el decorador **`@classmethod`** y ==toman como primer parámetro la clase en sí misma, que generalmente se nombra== **`cls`** ==por convención.== A través del parámetro **`cls`**, los métodos de clase pueden acceder a los atributos de clase y realizar operaciones que son relevantes para la clase en su conjunto.
==Una característica común de los métodos de clase es que se utilizan para crear métodos alternativos de construcción de objetos.== Esto significa que se pueden utilizar para proporcionar formas diferentes de crear instancias de una clase, como a partir de diferentes fuentes de datos o con argumentos diferentes.
Los métodos de clase son útiles cuando se necesita realizar operaciones que no dependen de las instancias individuales de la clase, sino que están relacionadas con la clase en sí misma. Permiten organizar y encapsular la lógica relacionada con la clase y proporcionan una forma de trabajar directamente con la clase en lugar de con instancias individuales.

Ejemplo de cómo se puede definir y utilizar un método de clase en Python:
```python
class Circulo:
    pi = 3.14159

    def __init__(self, radio):
        self.radio = radio

    def area(self):
        return self.pi * (self.radio ** 2)

    @classmethod
    def diametro(cls, radio):
        return 2 * radio

# Uso de un método de clase para obtener el diámetro de un círculo
radio = 5
diametro = Circulo.diametro(radio)
print("El diámetro del círculo es:", diametro)
```

En este ejemplo, la clase **`Circulo`** tiene dos métodos: **`area`** y **`diametro`**. El método **`area`** es un método de instancia normal que calcula el área del círculo en función de su radio.
El método **`diametro`** es un método de clase que se define utilizando el decorador **`@classmethod`**. Recibe la clase como su primer parámetro, que se nombra convencionalmente como **`cls`**. En este caso, el método **`diametro`** simplemente calcula el diámetro de un círculo dado su radio, sin necesidad de una instancia de la clase.
En el ejemplo, se crea una instancia de la clase **`Circulo`** con un radio de 5. Luego, se utiliza el método de clase **`diametro`** para obtener el diámetro del círculo, pasando el radio como argumento.


## Propiedades y métodos privados

==En Python, no existe una implementación estricta de atributos o métodos privados como en otros lenguajes de programación.== Sin embargo, se sigue una convención de nomenclatura para indicar que un atributo o método se considera privado y no debe ser accedido directamente desde fuera de la clase.
La convención es utilizar un solo guion bajo al comienzo del nombre para indicar que el atributo o método es privado. Por ejemplo, **`_atributo_privado`** o **`_metodo_privado()`**. ==Esto no impide el acceso directo a ellos desde fuera de la clase, pero es una señal para los desarrolladores de que esos elementos no están destinados a ser utilizados externamente y pueden estar sujetos a cambios internos.==
Es importante tener en cuenta que Python confía en la responsabilidad del programador para respetar las convenciones y no acceder directamente a los atributos o métodos privados desde fuera de la clase. Sin embargo, aún es posible acceder a ellos si se desea. Esta flexibilidad es parte de la filosofía de Python de "Los adultos son responsables de sus acciones".
En resumen, en Python se utiliza una convención de nomenclatura para indicar que un atributo o método es privado, utilizando un solo guion bajo al comienzo del nombre. Sin embargo, no hay una restricción estricta para acceder a ellos desde fuera de la clase, y se espera que los desarrolladores respeten las convenciones y no accedan directamente a ellos.

Ahora, ya sabemos que todos los elementos dentro de una clases, por default, son "públicos", si queremos que un desarrollador _no_ modifique o mande a llamar algún elemento fuera de la clase, basta con colocar un guión bajo como prefijo, sin embargo, es probable, que tarde o temprano nos encontremos con variables o métodos con un doble guión bajo (**`__atributo_o_metodo_privado()`**). Esos casos son especiales, porque al utilizar un doble guión bajo, ya sea para una atributo o algún método, el intérprete de Python re nombra al elemento para evitar colisiones con las subclases. Aunque la idea original era esa, evitar colisiones, muchos desarrolladores utilizamos el doble guión bajo para prevenir accesos no autorizados.
```Python
class Perro:
	def __init__(self, nombre, edad):
	self.__nombre = nombre
	self.edad = edad
	
	def get_nombre(self):
		return self.__nombre
		
	def set_nombre(self, nombre):
		self.__nombre = nombre
		
	def habla(self):
		print(f"{self.__nombre} dice Guau!")
```


## Decorador property

El decorador property en Python ==se utiliza para convertir un método de una clase en una propiedad.== Proporciona una forma de definir un método que se comporta como un atributo, permitiendo el acceso, la asignación y otras operaciones relacionadas con el atributo, pero manteniendo la flexibilidad de ejecutar lógica personalizada antes o después de la operación.
Al utilizar el decorador property, se definen tres métodos especiales en la clase: **getter**, **setter** y **deleter**. Estos métodos se encargan de definir el comportamiento de la propiedad.

- El método **getter** se ejecuta cuando se accede al valor de la propiedad.
- El método **setter** se ejecuta cuando se asigna un valor a la propiedad.
- El método **deleter** se ejecuta cuando se elimina la propiedad.

Veamos un ejemplo para ilustrar su uso:
```python
class Persona:
    def __init__(self, nombre):
        self._nombre = nombre

    @property
    def nombre(self):
        return self._nombre

    @nombre.setter
    def nombre(self, valor):
        self._nombre = valor

    @nombre.deleter
    def nombre(self):
        del self._nombre

# Uso de la propiedad
p = Persona("John")
print(p.nombre)  # Acceso al valor de la propiedad

p.nombre = "Jane"  # Asignación de un nuevo valor a la propiedad
print(p.nombre)  # Acceso al nuevo valor

del p.nombre  # Eliminación de la propiedad
print(p.nombre)  # Genera un AttributeError: 'Persona' object has no attribute '_nombre'
```

En este ejemplo, se define la clase **`Persona`** con un atributo **`_nombre`**. Luego, se utiliza el decorador **`@property`** para definir la propiedad nombre que encapsula el atributo **`_nombre`**. Se definen los métodos **`getter`**, **`setter`** y **`deleter`** para definir el comportamiento de la propiedad.
Al utilizar la propiedad **`nombre`**, se accede y se asigna el valor como si fuera un atributo, pero en realidad se ejecutan los métodos correspondientes.
El uso de **`@property`** brinda una forma más elegante y controlada de trabajar con atributos, ya que permite definir lógica personalizada en los métodos **`getter`**, **`setter`** y **`deleter`**, lo que facilita la validación, el cálculo dinámico u otras operaciones adicionales.


## Métodos mágicos

Los métodos mágicos, también conocidos como métodos especiales o métodos dunder (double underscore), ==son métodos predefinidos en Python que tienen nombres especiales con doble subrayado al comienzo y al final==, como **`__init__`**, **`__str__`**, **`__len__`**, entre otros. Estos métodos permiten definir el comportamiento especial de las clases y objetos en determinadas situaciones.
Los métodos mágicos son invocados automáticamente por Python en respuesta a ciertos eventos o acciones. Por ejemplo, **`__init__`** se ejecuta automáticamente al crear una nueva instancia de una clase y se utiliza para inicializar los atributos de esa instancia. Otros ejemplos son **`__str__`**, que se utiliza para representar una instancia de una clase como una cadena legible, y **`__len__`**, que se utiliza para obtener la longitud de un objeto.
Al implementar métodos mágicos en una clase, se puede personalizar el comportamiento de los operadores integrados, como la suma (+), la multiplicación (\*), la indexación (\[]), entre otros, y se puede definir cómo se comporta la clase en diferentes contextos y operaciones.
==Los métodos mágicos son una parte poderosa de la programación orientada a objetos en Python, ya que permiten que las clases se comporten de manera intuitiva y se adapten a las necesidades específicas del programa.==
Es importante destacar que los métodos mágicos no se llaman directamente, sino que son invocados automáticamente por Python en función de la operación o el evento correspondiente.


#### Destructor

El destructor es un método que elimina una instancia de una clase y puede ser un método mágico:
```Python
def __del__(self):
	print(f"Chau Perro {self.nombre}")
```

Documentación referente a los diferentes métodos mágicos [aquí](https://rszalski.github.io/magicmethods)


## Contenedores

En Python, los contenedores ==son estructuras de datos que almacenan y organizan otros objetos.== Proporcionan una forma conveniente de agrupar elementos relacionados y permiten realizar operaciones y manipulaciones en conjunto.

En Python, los contenedores más comunes son las listas, las tuplas, los conjuntos y los diccionarios. Cada uno de ellos tiene características y comportamientos específicos:

1. Listas: Son colecciones ordenadas y mutables de elementos. Pueden contener objetos de diferentes tipos y se definen utilizando corchetes **`[]`** o la función **`list()`**.. Permiten agregar, eliminar, modificar y acceder a elementos mediante índices.
2. Tuplas: Son colecciones ordenadas e inmutables de elementos. Se definen utilizando paréntesis **`()`** o simplemente separando los elementos por comas. Las tuplas son similares a las listas, pero no se pueden modificar una vez creadas. Se utilizan para almacenar datos que no deben cambiar.
3. Sets: Son colecciones no ordenadas de elementos únicos. No permiten duplicados y se utilizan para realizar operaciones matemáticas de conjuntos, como unión, intersección y diferencia. Se definen utilizando llaves **`{}`** o la función **`set()`**.
4. Diccionarios: Son colecciones de pares clave-valor no ordenados. Cada elemento del diccionario se compone de una clave única y su valor asociado. Se definen utilizando llaves **`{}`** y dos puntos **`:`** para separar las claves y los valores. Los diccionarios permiten acceder a los valores mediante las claves, agregar nuevos pares clave-valor y modificar o eliminar pares existentes.

Estos contenedores son flexibles y se utilizan para diferentes propósitos en la programación de Python, dependiendo de las necesidades del programa. Cada uno tiene sus características y métodos específicos que los hacen adecuados para diferentes situaciones, en la siguiente pagina hay mas información sobre estos tipos de datos: [[Tipos avanzados]].


## Herencia

La herencia es un concepto fundamental en la programación orientada a objetos que permite crear nuevas clases basadas en clases existentes. En Python, la herencia se logra al crear una clase que hereda los atributos y métodos de otra clase, conocida como clase padre o clase base.
La clase que hereda se denomina clase hija o clase derivada. La herencia permite a la clase hija heredar los atributos y métodos de la clase padre, lo que permite reutilizar el código existente y facilita la creación de jerarquías de clases.

La sintaxis básica para definir una clase hija en Python es la siguiente:
```python
class ClasePadre:
    # Atributos y métodos de la clase padre

class ClaseHija(ClasePadre):
    # Atributos y métodos adicionales de la clase hija
```

Al heredar de una clase padre, la clase hija puede acceder y utilizar los atributos y métodos de la clase padre. Además, la clase hija puede agregar nuevos atributos y métodos, y también puede modificar o sobrescribir los atributos y métodos heredados según sea necesario.
La herencia permite establecer relaciones de especialización entre clases. La clase hija hereda los comportamientos generales de la clase padre y puede agregar comportamientos específicos adicionales. Esto facilita la creación de código modular y extensible, ya que se puede definir una funcionalidad común en la clase padre y personalizarla en las clases hijas según sea necesario.
La herencia múltiple también es posible en Python, lo que significa que una clase puede heredar de múltiples clases padre. Esto permite combinar características y funcionalidades de varias clases en una sola clase hija.
==En resumen, la herencia en Python es un mecanismo poderoso que permite crear jerarquías de clases y reutilizar el código existente. Facilita la organización y estructuración del código, promueve la reutilización y extensibilidad, y permite establecer relaciones de especialización entre clases.==


### Herencia multiple

La herencia múltiple es un concepto en la programación orientada a objetos que permite a una clase heredar atributos y métodos de múltiples clases padres. En Python, se permite la herencia múltiple, lo que significa que una clase puede heredar de más de una clase padre.

La sintaxis para definir una clase que hereda de múltiples clases padres en Python es la siguiente:
```python
class ClasePadre1:
    # Atributos y métodos de la primera clase padre

class ClasePadre2:
    # Atributos y métodos de la segunda clase padre

class ClaseHija(ClasePadre1, ClasePadre2):
    # Atributos y métodos adicionales de la clase hija
```

Al utilizar la herencia múltiple, la clase hija adquiere todos los atributos y métodos de ambas clases padres. Esto significa que la clase hija puede acceder y utilizar los atributos y métodos de todas las clases padres.
La herencia múltiple permite combinar características y funcionalidades de varias clases en una sola clase hija. Esto puede ser útil cuando se desea aprovechar el comportamiento de múltiples clases existentes o cuando se desea crear una clase que combine características específicas de diferentes dominios.
Sin embargo, es importante tener en cuenta que la herencia múltiple también puede complicar la estructura y el diseño del código. Puede haber conflictos si las clases padres tienen métodos con el mismo nombre. En caso de conflictos, se utiliza el orden de resolución de métodos conocido como MRO (Method Resolution Order) para determinar qué método se utiliza.
[What is MRO in python?](https://www.educative.io/answers/what-is-mro-in-python)


### Method overriding

==La anulación de métodos, también conocida como sobrescritura de métodos, es un concepto en la programación orientada a objetos que permite a una clase hija proporcionar una implementación diferente de un método que ya está definido en la clase padre.== 
Cuando una clase hija hereda un método de la clase padre, puede anular ese método al proporcionar su propia implementación. Esto significa que la versión del método en la clase hija reemplaza y anula la versión del método en la clase padre.
La anulación de métodos es útil cuando se necesita modificar o personalizar el comportamiento de un método heredado en una clase hija. Al anular un método, se puede cambiar la lógica interna, los cálculos, las operaciones o cualquier aspecto del comportamiento del método según las necesidades específicas de la clase hija.
La anulación de métodos se logra al definir un método con el mismo nombre en la clase hija. La firma (nombre y parámetros) del método anulado debe coincidir con el método heredado de la clase padre. Al llamar al método desde una instancia de la clase hija, se ejecutará la versión anulada en lugar de la versión heredada.

Es importante mencionar que la anulación de métodos no afecta a la clase padre o a otras clases hijas que puedan heredar el mismo método. Cada clase hija puede proporcionar su propia implementación del método y anularlo si es necesario, lo que brinda flexibilidad y personalización en la estructura de herencia.
En Python la función **`super()`** se utiliza para llamar y acceder a métodos de la clase padre desde la clase hija. Proporciona una forma conveniente de invocar los métodos de la clase padre en lugar de repetir su implementación en la clase hija.
Al utilizar **`super()`**, se puede llamar al método de la clase padre directamente sin especificar el nombre de la clase padre de manera explícita. Esto es útil cuando se desea extender o modificar el comportamiento de un método heredado, pero se quiere mantener y ejecutar la lógica existente de la clase padre.

La sintaxis básica para utilizar **`super()`** es la siguiente:
```python
class ClasePadre:
    def metodo(self):
        # Implementación del método en la clase padre

class ClaseHija(ClasePadre):
    def metodo(self):
        super().metodo()
        # Implementación adicional de la clase hija
```

En este ejemplo, la clase **`ClaseHija`** hereda de **`ClasePadre`** y define su propia implementación del método **`metodo()`**. Dentro de la implementación de la clase hija, se utiliza **`super().metodo()`** para llamar al método **`metodo()`** de la clase padre. Esto permite ejecutar la implementación de la clase padre y luego agregar la lógica adicional específica de la clase hija.

**`super()`** también se puede utilizar en casos de herencia múltiple, donde hay varias clases padres. En este caso, **`super()`** se utiliza para llamar a los métodos de las clases padres en el orden de resolución de métodos (MRO) determinado por Python.


## Clases abstractas

==Las clases abstractas son clases que no pueden ser instanciadas directamente, sino que se utilizan como plantillas para definir características y comportamientos comunes que deben ser implementados por las clases hijas.== En Python, las clases abstractas se definen utilizando el módulo **`abc`** (Abstract Base Classes).
Las clases abstractas se utilizan para establecer una interfaz común entre las clases hijas, especificando qué métodos deben ser implementados por las clases hijas y cómo deben interactuar entre sí. Estas clases proporcionan una estructura y un conjunto de métodos que deben ser implementados por las clases concretas.
La biblioteca **`abc`** proporciona la clase base `ABC` (Abstract Base Class), la cual se utiliza como base para definir una clase abstracta. Además, se utiliza el decorador **`@abstractmethod`** para marcar los métodos que deben ser implementados por las clases hijas.

A continuación, se muestra un ejemplo de cómo definir una clase abstracta en Python:
```python
from abc import ABC, abstractmethod

class ClaseAbstracta(ABC):
    @abstractmethod
    def metodo_abstracto(self):
        pass

    def metodo_concreto(self):
        # Implementación del método concreto
        pass
```

En este ejemplo, **`ClaseAbstracta`** es una clase abstracta que hereda de la clase base **`ABC`**. La clase define un método abstracto **`metodo_abstracto()`** utilizando el decorador **`@abstractmethod`**. Este método debe ser implementado por las clases hijas, mientras que el método **`metodo_concreto()`** proporciona una implementación concreta que puede ser heredada o sobrescrita por las clases hijas.

==Las clases hijas que heredan de una clase abstracta deben implementar todos los métodos abstractos definidos en la clase abstracta. Si una clase hija no implementa un método abstracto, se generará un error en tiempo de ejecución.==

Las clases abstractas son útiles para establecer una estructura común en una jerarquía de clases y asegurarse de que ciertos métodos sean implementados en todas las clases hijas. Además, permiten definir comportamientos predeterminados en métodos concretos que pueden ser heredados por las clases hijas.

> **`pass`** se utiliza como una declaración que no realiza ninguna acción, pero que permite evitar errores de sintaxis cuando se requiere una declaración en un bloque de código o en la definición de funciones o clases, pero no se necesita ejecutar ninguna instrucción en ese momento.


## Polimorfismo

El polimorfismo es un concepto fundamental en la programación orientada a objetos que ==se refiere a la capacidad de un objeto para tomar muchas formas o comportarse de diferentes maneras en función del contexto en el que se utilice.==
En Python, el polimorfismo se logra mediante la implementación de métodos con el mismo nombre en diferentes clases, permitiendo que estos métodos sean invocados de manera uniforme, aunque tengan diferentes implementaciones. Esto significa que un objeto de una clase puede ser tratado como un objeto de otra clase relacionada y responderá de acuerdo a su propia implementación del método.
El polimorfismo es útil porque permite escribir código más genérico y flexible, ya que se puede trabajar con objetos de diferentes clases de manera uniforme sin tener que preocuparse por los detalles específicos de cada clase. Esto facilita la reutilización de código y la construcción de estructuras más modulares y escalables.

Un ejemplo común de polimorfismo es el método **`print()`** en Python. Este método puede imprimir objetos de diferentes tipos, como cadenas, números, listas, diccionarios, etc. Aunque la implementación interna de **`print()`** puede variar dependiendo del tipo de objeto que se esté imprimiendo, se puede invocar de la misma manera y obtener resultados adecuados en todos los casos.
Otro ejemplo es el uso de la herencia y el polimorfismo en las relaciones entre clases. Si hay una clase base y varias clases derivadas que heredan de ella, es posible tratar a los objetos de las clases derivadas como objetos de la clase base, lo que permite escribir código genérico que puede trabajar con cualquier objeto derivado sin necesidad de conocer su tipo específico.

Un ejemplo de polimorfismo en Python:
```python
from abc import ABC, abstractmethod

class Animal(ABC):
	@abstractmethod
	def hablar(self):
		pass


class Perro(Animal):
    def hablar(self):
        return "Woof!"

class Gato(Animal):
    def hablar(self):
        return "¡Miau!"

class Vaca(Animal):
    def hablar(self):
        return "Muu!"

def hacer_sonar(Animal):
    print(Animal.hablar())

perro = Perro()
gato = Gato()
vaca = Vaca()

hacer_sonar(perro)  # Output: Woof!
hacer_sonar(gato)   # Output: ¡Miau!
hacer_sonar(vaca)   # Output: Muu!
```

==En resumen, el polimorfismo es la capacidad de los objetos de diferentes clases de responder al mismo método de manera diferente.== Esto se logra implementando métodos con el mismo nombre en diferentes clases y permite tratar a los objetos de diferentes clases de manera uniforme, lo que facilita la escritura de código genérico y flexible.


### Duck Typing

El polimorfismo en Python está estrechamente relacionado con el concepto de Duck Typing.
Duck Typing es un principio de programación en el que se enfoca en el comportamiento de un objeto en lugar de su tipo específico. Según el Duck Typing:
> Si camina como un pato y suena como un pato, entonces debe ser un pato

En Python, no es necesario que un objeto implemente una interfaz o herede de una clase específica para que se considere válido en un contexto determinado. En su lugar, se evalúa si el objeto proporciona los métodos o atributos necesarios para realizar una determinada acción. Si un objeto cumple con los requisitos necesarios, se puede utilizar en ese contexto, independientemente de su tipo o clase.
El polimorfismo en Python se basa en el Duck Typing, ya que se enfoca en la capacidad de un objeto para responder a un determinado método o comportamiento, en lugar de su tipo específico. Si un objeto implementa el método requerido, se puede tratar como si fuera del mismo tipo que otros objetos que también implementan ese método, aunque sean de clases diferentes.

![[duck.png | 500]]


## Extender tipos nativos

==Se refiere a la capacidad de agregar funcionalidad adicional a los tipos de datos integrados (nativos) de Python, como cadenas (strings), listas, diccionarios, entre otros.==
Python permite extender los tipos nativos mediante el concepto de _herencia de tipo_. Esto implica crear una nueva clase que herede de un tipo nativo existente y agregar métodos o atributos personalizados a la nueva clase.

Por ejemplo, supongamos que deseamos agregar un método personalizado a la clase **`str`** (cadena) que cuente la cantidad de vocales en una cadena. Podemos crear una nueva clase llamada **`VocalesString`** que herede de **`str`** y defina un nuevo método **`contar_vocales()`**:
```python
class VocalesString(str):
    def contar_vocales(self):
        count = 0
        for char in self:
            if char.lower() in 'aeiou':
                count += 1
        return count
```

Con esta nueva clase, podemos crear instancias de **`VocalesString`** y utilizar el método **`contar_vocales()`** para contar las vocales en una cadena:
```python
texto = VocalesString("Hola, cómo estás?")
print(texto.contar_vocales())  # Output: 6
```

En este ejemplo, hemos extendido el tipo nativo **`str`** creando la clase **`VocalesString`** y agregando un método personalizado. La instancia de **`VocalesString`** actúa como una cadena regular, pero también tiene acceso al nuevo método **`contar_vocales()`**.

La capacidad de extender tipos nativos en Python permite adaptar los tipos de datos existentes a nuestras necesidades específicas, agregando funcionalidad adicional sin tener que modificar directamente la implementación de los tipos nativos. Sin embargo, es importante utilizar esta capacidad con cuidado y moderación, ya que puede complicar la legibilidad y el mantenimiento del código si se abusa de ella.


---

* #POO
* #encapsulamiento
* #clases_abstractas 
* #metodos_abstractos 
* #herencia_multiple 
* #polimorfismo 
* #decoradores