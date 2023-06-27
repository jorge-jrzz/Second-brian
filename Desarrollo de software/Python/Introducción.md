
### REPL
REPL significa Read, Eval, Print, Loop.
O sea, esto vendría siendo un loop que está constantemente leyendo, evaluando e imprimiendo todo lo que nosotros escribimos acá.
El REPL se encarga de comunicarse con el interprete.
![[REPL.jpeg]]
**Se utilizan para lanzar sentencias Python para ser evaluadas rápidamente;** y es una de las herramientas más potentes que tiene el lenguaje.
Para salir del REPL se necesita de la siguiente combinación:
* Windows → ctlr + Z + Enter
* MacOS    → ctlr + D

### Linter
Un linter en Python es una herramienta que ayuda a los programadores a identificar y corregir errores en el código fuente de un programa, sin la necesidad de compilar o correr el programa. El término "linter" se deriva del nombre de la herramienta "lint" que fue desarrollada originalmente para C.
En Python, los linters pueden ayudar a identificar errores de sintaxis, problemas de estilo de código, errores de tipo y otras cuestiones que pueden afectar el rendimiento y la calidad del código.
Hay varios linters populares disponibles para Python, entre ellos:
1. pylint: Este es uno de los linters más populares para Python. Pylint puede identificar problemas de estilo de código, errores de sintaxis y otros errores comunes. También es altamente personalizable y se puede configurar para adaptarse a los estándares de codificación específicos del proyecto.
2. flake8: Flake8 es un linter de Python que combina tres herramientas diferentes: Pyflakes, pycodestyle y McCabe. Pyflakes detecta errores de sintaxis y errores de nombres no utilizados, pycodestyle comprueba el cumplimiento de las normas de codificación PEP8 y McCabe mide la complejidad ciclomática del código.
3. mypy: Mypy es un linter de tipo estático para Python que permite al programador declarar tipos explícitamente en el código. Esto ayuda a prevenir errores de tipo en tiempo de ejecución y mejora la legibilidad y mantenibilidad del código.
En general, el uso de un linter en Python puede ser una práctica muy útil para mejorar la calidad del código y reducir los errores.
PEP significa "**Python Enhancement Proposal**" o "Propuesta de Mejora de Python" en español. Las PEPs son documentos escritos por miembros de la comunidad de Python que proponen mejoras y cambios en el lenguaje de programación Python y en su biblioteca estándar.
Las PEPs cubren una amplia gama de temas, desde la sintaxis del lenguaje hasta la organización de la biblioteca estándar de Python y los procesos de desarrollo de Python. Cualquier persona puede escribir una PEP y presentarla para su consideración.
Las PEPs son importantes para la evolución de Python porque proporcionan una forma estructurada para que la comunidad de Python proponga y discuta mejoras y cambios en el lenguaje y la biblioteca estándar. También proporcionan una forma para que los desarrolladores de Python discutan y decidan sobre el futuro del lenguaje y la biblioteca estándar.
Además, las PEPs proporcionan una forma para que los desarrolladores de Python aprendan sobre los cambios propuestos en el lenguaje y la biblioteca estándar, y para que los usuarios de Python comprendan cómo funcionan y se implementan estas propuestas.
Las PEPs están numeradas y se organizan en categorías. Por ejemplo, las PEPs del 1 al 99 se refieren a cuestiones relacionadas con el proceso de PEP, mientras que las PEPs del 200 al 299 se refieren a las características del lenguaje de programación Python.
En resumen, las PEPs son documentos importantes en la comunidad de Python que ayudan a dar forma a la evolución del lenguaje y la biblioteca estándar, y proporcionan una forma estructurada para que los miembros de la comunidad discutan y decidan sobre el futuro de Python.
La PEP universal es la [PEP8](https://peps.python.org/pep-0008/) y la forma de configurar el auto formato cada ves que nosotros guardemos nuestro código de Python en VS Code es la siguiente :

[Autoformateo en VS Code](https://youtu.be/ndqMxywWDjM?t=156)

---

### Ejecución de Python
Las ***implementaciones*** de Python son programas que toman el código escrito en Python y lo transforman en código de máquina, que puede ser interpretado por la computadora; El problema con los lenguajes de máquina es que cada lenguaje de máquina es distinto y este va a depender del sistema operativo y también del hardware.
Un lenguaje de programación es un conjunto de reglas que deben cumplirse para poder ser considerado como tal, y Python es un lenguaje de alto nivel, lo que significa que es fácil de entender para los humanos, pero no para las máquinas, ya que ellas entienden el lenguaje de máquina, que es una serie de ceros y unos.
Existen varias implementaciones de Python, cada una escrita en un lenguaje de programación diferente, como Cpython, PyPy, IronPython, Jython y Brython. cPython es la implementación oficial de Python y es la que recibe primero las nuevas funcionalidades de Python. Las diferentes implementaciones permiten utilizar código escrito en diferentes lenguajes de programación, como Java o C.

Ejemplo de implementación de Java (Jython):

![[Captura_Jython.png]]