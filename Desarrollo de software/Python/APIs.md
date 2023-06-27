## ¿Que es HTTP?

HTTP (Hypertext Transfer Protocol) es un protocolo de comunicación utilizado para transferir información en la World Wide Web (WWW). Es el protocolo fundamental utilizado para la comunicación entre un cliente (como un navegador web) y un servidor web.

El protocolo HTTP permite que los clientes realicen solicitudes de recursos, como páginas web, imágenes, archivos, etc., a través de Internet. Estas solicitudes son enviadas al servidor web, que responde con la información solicitada en forma de respuesta HTTP.

Algunas características importantes del protocolo HTTP son:

1. Basado en el modelo cliente-servidor: En el modelo cliente-servidor, el cliente realiza solicitudes al servidor, y el servidor responde con los recursos solicitados.

2. Sin estado: El protocolo HTTP es sin estado, lo que significa que cada solicitud se trata de forma independiente y no se mantiene información sobre las solicitudes anteriores. Esto implica que cada solicitud debe incluir toda la información necesaria para que el servidor comprenda y responda adecuadamente.

3. Protocolo basado en texto: Las solicitudes y respuestas HTTP están formateadas como mensajes de texto legibles por humanos. Estos mensajes se componen de líneas de texto, que contienen encabezados (headers) y, opcionalmente, un cuerpo (body) que puede contener datos adicionales.

4. Uso de métodos HTTP: Los métodos HTTP, como GET, POST, PUT, DELETE, entre otros, se utilizan para indicar la acción que se desea realizar en el recurso solicitado.

El protocolo HTTP se basa en el uso de URLs (Uniform Resource Locators) para identificar los recursos que se desean obtener o manipular. Además, puede utilizar protocolos de seguridad, como HTTPS, para proporcionar una comunicación segura y encriptada entre el cliente y el servidor.

En resumen, HTTP es el protocolo que permite la transferencia de información en la web, permitiendo a los clientes obtener recursos y a los servidores responder con la información solicitada.

## Metodos HTTP

Los métodos HTTP, también conocidos como verbos HTTP, son parte integral del protocolo HTTP y se utilizan para indicar la acción que se desea realizar en un recurso específico. Los métodos más comunes en HTTP son:

1. GET: El método GET se utiliza para recuperar información o recursos del servidor. Cuando se realiza una solicitud GET, <mark class="hltr-yellow">el cliente solicita al servidor</mark> el contenido del recurso identificado por la URL. Esta solicitud no debe tener ningún efecto secundario en el servidor.

2. POST: El método POST se utiliza <mark class="hltr-yellow">para enviar datos al servidor</mark> para su procesamiento. Por lo general, se utiliza para enviar información del formulario, cargar archivos o realizar acciones que tienen un efecto secundario en el servidor, como crear un nuevo recurso. Los datos se envían en el cuerpo de la solicitud.

3. PUT: El método PUT se utiliza para enviar datos al servidor y <mark class="hltr-yellow">actualizar un recurso existente en el servidor</mark> con los nuevos datos proporcionados. Si el recurso no existe, puede ser creado. Similar a POST, los datos se envían en el cuerpo de la solicitud.

4. DELETE: El método DELETE se utiliza para <mark class="hltr-yellow">solicitar al servidor que elimine un recurso</mark> específico identificado por la URL. Después de una solicitud DELETE exitosa, el recurso correspondiente se elimina del servidor.

5. PATCH: El método PATCH se utiliza para realizar modificaciones parciales en un recurso. A diferencia de PUT, que requiere enviar el recurso completo, PATCH permite enviar solo las modificaciones necesarias.

6. HEAD: El método HEAD es similar a GET, pero el servidor solo responde con los encabezados de respuesta, sin incluir el cuerpo del recurso. Se utiliza para obtener información sobre el recurso sin descargar su contenido completo.

Estos son solo algunos de los métodos más comunes en HTTP. Otros métodos menos utilizados incluyen OPTIONS, TRACE y CONNECT, que tienen propósitos específicos en situaciones particulares.

Es importante tener en cuenta que cada método tiene su propia semántica y comportamiento definido en el estándar HTTP. Al utilizar estos métodos correctamente, se pueden construir aplicaciones web eficientes y seguras, siguiendo las convenciones y las mejores prácticas del protocolo HTTP.

## Formato JSON

JSON (JavaScript Object Notation) es un formato ligero de intercambio de datos que se utiliza ampliamente en aplicaciones web y servicios web para el envío y recepción de datos estructurados. Es un formato de texto que sigue la sintaxis de los objetos JavaScript y permite representar datos de forma legible tanto para los humanos como para las máquinas.

Algunas características importantes de JSON son:

1. Estructura de datos: JSON permite representar datos estructurados en forma de pares clave-valor. Los datos pueden organizarse en objetos (delimitados por llaves `{}`), matrices (delimitadas por corchetes `[]`) y valores individuales.

2. Tipos de datos: JSON admite una variedad de tipos de datos, incluyendo cadenas de texto, números, booleanos, arrays, objetos y valores nulos.

3. Sintaxis simple y legible: JSON utiliza una sintaxis sencilla y legible basada en el uso de comillas dobles para las cadenas de texto y la separación de los pares clave-valor mediante dos puntos (`:`). Los elementos en un array o un objeto se separan por comas.

4. Independencia de lenguaje: JSON es independiente de cualquier lenguaje de programación y se puede utilizar con una amplia gama de lenguajes de programación, lo que facilita el intercambio de datos entre diferentes sistemas.

5. Fácil manipulación y procesamiento: JSON es fácil de parsear y generar en la mayoría de los lenguajes de programación, lo que facilita su manipulación y procesamiento en las aplicaciones. Existen bibliotecas y APIs disponibles en muchos lenguajes para trabajar con JSON de manera eficiente.

Ejemplo básico de JSON:

```json
{
  "nombre": "Juan",
  "edad": 25,
  "ciudad": "México",
  "intereses": ["programación", "viajes", "lectura"],
  "activo": true
}
```

En este ejemplo, tenemos un objeto JSON que representa información sobre una persona. El objeto tiene diferentes pares clave-valor:

- "nombre" es una cadena de texto que contiene el valor "Juan".
- "edad" es un número entero con el valor 25.
- "ciudad" es una cadena de texto con el valor "México".
- "intereses" es un array que contiene varios elementos, como "programación", "viajes" y "lectura".
- "activo" es un valor booleano que indica si la persona está activa o no.

JSON se ha convertido en un estándar de facto para el intercambio de datos en aplicaciones web y servicios web debido a su simplicidad, legibilidad y soporte amplio en diferentes lenguajes y plataformas. Es ampliamente utilizado en APIs web para el envío y recepción de datos estructurados, y se ha convertido en un formato común para el almacenamiento y transporte de datos en aplicaciones modernas.

## Consumir APIs con Python

El módulo `requests` es una biblioteca de Python que permite realizar solicitudes HTTP de manera sencilla. Proporciona una interfaz fácil de usar para enviar solicitudes HTTP, manejar respuestas y trabajar con datos en formato JSON, XML o de otro tipo.

Algunas características clave del módulo `requests` son:

1. Realización de solicitudes HTTP: El módulo `requests` ofrece métodos como `get()`, `post()`, `put()`, `delete()`, entre otros, que permiten realizar diferentes tipos de solicitudes HTTP a servidores web.

2. Manejo de respuestas: Puedes acceder a la respuesta de una solicitud HTTP a través del objeto `Response` devuelto por las funciones del módulo `requests`. Este objeto proporciona información sobre el código de estado, encabezados y contenido de la respuesta.

3. Parámetros de solicitud: Puedes pasar parámetros adicionales a las solicitudes HTTP, como encabezados personalizados, datos del cuerpo de la solicitud, parámetros de URL, autenticación, cookies, entre otros.

4. Manejo de errores: El módulo `requests` maneja automáticamente los errores HTTP, como códigos de estado no exitosos. También puedes verificar manualmente los códigos de estado y lanzar excepciones en función de ellos.

5. Trabajo con sesiones: El módulo `requests` proporciona la posibilidad de crear sesiones persistentes, lo que permite mantener cierta información entre múltiples solicitudes, como cookies y valores de autenticación.

### Método GET

Ejemplo básico de cómo usar el módulo `requests` para hacer una solicitud GET:

```python
import requests

URL = 'http://httpbin.org/get'

response = requests.get(URL)

print(response)
print(response.status_code)
print(response.text)    # Objeto de tipo string
print(response.json())  # Objeto de tipo diccionario

payload = response.json()
print(payload.get('origin'))

print(response.url)
```

El código que has compartido utiliza el módulo `requests` para hacer una solicitud GET a la URL 'http://httpbin.org/get' y luego muestra diferentes aspectos de la respuesta.
Aquí está el análisis paso a paso del código:

1. `import requests`: Importa el módulo `requests`, que se utiliza para realizar solicitudes HTTP.
2. `URL = 'http://httpbin.org/get'`: Define la URL de destino a la que se realizará la solicitud GET.
3. `response = requests.get(URL)`: Realiza una solicitud GET a la URL especificada y almacena la respuesta en la variable `response`.
4. `print(response)`: Muestra el objeto `Response` que contiene información sobre la respuesta HTTP, como el código de estado, los encabezados, etc.
5. `print(response.status_code)`: Muestra el código de estado de la respuesta HTTP.
6. `print(response.text)`: Muestra el contenido de la respuesta como una cadena de texto.
7. `print(response.json())`: Intenta interpretar el contenido de la respuesta como JSON y mostrarlo como un diccionario. Si la respuesta no puede ser interpretada como JSON, se generará una excepción.
8. `payload = response.json()`: Almacena el contenido de la respuesta interpretado como JSON en la variable `payload`.
9. `print(payload.get('origin'))`: Accede al valor correspondiente a la clave 'origin' en el diccionario `payload` y lo muestra. En este caso, 'origin' se refiere a la dirección IP desde la cual se realizó la solicitud.
10. `print(response.url)`: Muestra la URL a la que se realizó la solicitud.

#### Params

El query en una petición GET es una forma de enviar parámetros adicionales a través de la URL. Estos parámetros se agregan después del signo de interrogación "?" y se especifican en forma de pares clave-valor, separados por el símbolo "&".

Por ejemplo, consideremos la siguiente URL:

```
http://example.com/search?query=python&page=1&limit=10
```

En este caso, el query de la petición GET es `query=python&page=1&limit=10`. Aquí, se están enviando tres parámetros: `query` con el valor "python", `page` con el valor "1" y `limit` con el valor "10".

En Python, al utilizar el módulo `requests`, puedes pasar los parámetros del query como un diccionario utilizando el parámetro `params`. El módulo `requests` se encargará de construir automáticamente el query y agregarlo a la URL de la solicitud.

Aquí hay un ejemplo:

```python
import requests

url = 'http://example.com/search'
params = {
    'query': 'python',
    'page': 1,
    'limit': 10
}

response = requests.get(url, params=params)
```

En este ejemplo, se utiliza el diccionario `params` para especificar los parámetros del query. Luego, al realizar la solicitud GET con `requests.get()`, el módulo `requests` construirá automáticamente el query y lo agregará a la URL de la solicitud.

El query en una petición GET es útil cuando deseas enviar información adicional al servidor para filtrar resultados, realizar búsquedas, paginación u otras operaciones. El servidor puede procesar los parámetros del query y devolver los resultados correspondientes en función de ellos.

### Método POST
El método POST es utilizado en solicitudes HTTP para enviar datos al servidor. A diferencia del método GET, que envía datos a través de la URL, el método POST envía los datos en el cuerpo del mensaje de la solicitud.

En Python, puedes utilizar el módulo `requests` para realizar solicitudes POST de manera sencilla. A continuación se muestra un ejemplo básico de cómo hacer una solicitud POST utilizando `requests`:

```python
import requests

url = 'http://example.com/post'
data = {
    'nombre': 'John Doe',
    'edad': 25,
    'ciudad': 'New York'
}

response = requests.post(url, data=data)
```

En este ejemplo, se define la URL de destino en la variable `url` y los datos a enviar en el cuerpo de la solicitud se especifican en el diccionario `data`. Luego, se utiliza `requests.post()` para enviar la solicitud POST.

El módulo `requests` se encarga de establecer automáticamente el encabezado `Content-Type` adecuado (generalmente `application/x-www-form-urlencoded`) y codificar los datos en el cuerpo de la solicitud.

Si necesitas enviar datos en formato JSON en lugar de datos de formulario, puedes utilizar el parámetro `json` en lugar de `data`:

```python
import requests

url = 'http://example.com/post'
data = {
    'nombre': 'John Doe',
    'edad': 25,
    'ciudad': 'New York'
}

response = requests.post(url, json=data)
```

En este caso, `requests` establecerá el encabezado `Content-Type` como `application/json` y enviará los datos en el cuerpo de la solicitud en formato JSON.

Al realizar una solicitud POST, es común recibir una respuesta del servidor, que generalmente contiene información sobre el resultado de la operación. Puedes acceder a la respuesta utilizando la variable `response` y trabajar con ella según sea necesario, como leer el código de estado, el contenido de la respuesta o los encabezados.

#### Headers
Los encabezados (headers) son componentes importantes de las solicitudes y respuestas HTTP. Proporcionan información adicional sobre la solicitud o respuesta y ayudan a los servidores y clientes a comunicarse de manera efectiva.

En Python, al usar el módulo `requests`, puedes agregar encabezados personalizados a tus solicitudes HTTP utilizando el parámetro `headers`. Aquí hay un ejemplo básico:

```python
import requests

url = 'http://example.com/api'
headers = {
    'User-Agent': 'MiAplicacion/1.0',
    'Authorization': 'Bearer my_token',
    'Content-Type': 'application/json'
}

response = requests.get(url, headers=headers)
```

En este ejemplo, se define la URL de la solicitud en la variable `url` y se especifican los encabezados personalizados en el diccionario `headers`. Luego, al realizar la solicitud GET con `requests.get()`, se incluyen los encabezados en la solicitud.

El encabezado `User-Agent` se utiliza para identificar la aplicación o cliente que realiza la solicitud. Puedes establecerlo según tus necesidades. El encabezado `Authorization` se usa comúnmente para enviar tokens de autenticación, como un token JWT o un token de acceso. El encabezado `Content-Type` especifica el tipo de contenido que se envía en la solicitud, en este caso, se está enviando un cuerpo en formato JSON.

Además de agregar encabezados a las solicitudes, el módulo `requests` también proporciona métodos para acceder a los encabezados de las respuestas recibidas. Por ejemplo:

```python
import requests

url = 'http://example.com/api'

response = requests.get(url)
content_type = response.headers.get('Content-Type')
```

En este ejemplo, después de realizar una solicitud GET, se accede al encabezado `Content-Type` de la respuesta utilizando `response.headers.get('Content-Type')`. Esto te permite obtener información sobre el tipo de contenido de la respuesta, lo cual puede ser útil al procesar la respuesta recibida.

Los encabezados también se pueden utilizar en las solicitudes POST. Puedes incluir encabezados personalizados en una solicitud POST utilizando el parámetro `headers` del módulo `requests`. Aquí tienes un ejemplo:

```python
import requests

url = 'http://example.com/api'
headers = {
    'User-Agent': 'MiAplicacion/1.0',
    'Authorization': 'Bearer my_token',
    'Content-Type': 'application/json'
}
data = {
    'nombre': 'John Doe',
    'edad': 25
}

response = requests.post(url, headers=headers, json=data)
```

En este ejemplo, se especifican los encabezados personalizados en el diccionario `headers`. Luego, al realizar la solicitud POST con `requests.post()`, se incluyen los encabezados en la solicitud.

Es importante tener en cuenta que los encabezados utilizados en una solicitud POST pueden variar según los requisitos del servidor al que estás enviando la solicitud. Por ejemplo, puedes necesitar especificar un encabezado de autenticación específico o un encabezado de tipo de contenido diferente, dependiendo de la API o el servicio web al que estás accediendo.

Los encabezados son herramientas poderosas para personalizar y controlar las solicitudes y respuestas HTTP. Al trabajar con APIs, servicios web u otras interacciones HTTP, es importante comprender cómo utilizar los encabezados de manera adecuada para cumplir con los requisitos y lograr una comunicación efectiva entre el cliente y el servidor.

### Métodos PUT y DELETE
Los métodos PUT y DELETE son otros dos métodos HTTP utilizados para interactuar con recursos en un servidor.

- El método PUT se utiliza para actualizar un recurso existente en el servidor. En una solicitud PUT, se envía una representación completa del recurso que se desea actualizar. Si el recurso no existe, puede ser creado. Si el recurso existe, se sobrescribe con los nuevos datos proporcionados.

- El método DELETE se utiliza para eliminar un recurso existente en el servidor. Al enviar una solicitud DELETE a una URL específica, el servidor elimina el recurso asociado a esa URL.

En Python, puedes utilizar el módulo `requests` para realizar solicitudes PUT y DELETE de manera similar a las solicitudes GET y POST. Aquí tienes un ejemplo:

```python
import requests

# Ejemplo de solicitud PUT
url = 'http://example.com/api/resource/1'
data = {
    'campo1': 'valor1',
    'campo2': 'valor2'
}

response = requests.put(url, json=data)

# Ejemplo de solicitud DELETE
url = 'http://example.com/api/resource/1'

response = requests.delete(url)
```

En el ejemplo anterior, se utiliza `requests.put()` para enviar una solicitud PUT a la URL especificada y se envía una representación de datos en formato JSON mediante el parámetro `json`. Esto actualizará el recurso existente en el servidor con los nuevos datos proporcionados.

Para enviar una solicitud DELETE, se utiliza `requests.delete()` y se especifica la URL del recurso que se desea eliminar. Esto indicará al servidor que elimine el recurso asociado a esa URL.

Es importante tener en cuenta que los métodos PUT y DELETE pueden no estar habilitados en todos los servidores o APIs, ya que su uso está sujeto a restricciones y políticas de acceso. Asegúrate de consultar la documentación del servicio al que estás accediendo para confirmar si estos métodos son compatibles y cómo deben utilizarse correctamente.

### Download files
Para descargar archivos de un servidor en Python, puedes utilizar el módulo `requests`. Aquí tienes un ejemplo de cómo descargar un archivo:

```python
import requests

url = 'http://example.com/archivo.pdf'
nombre_archivo = 'archivo.pdf'

response = requests.get(url)
response.raise_for_status()

with open(nombre_archivo, 'wb') as archivo:
    archivo.write(response.content)

print('Descarga completa')
```

En este ejemplo, se utiliza `requests.get()` para enviar una solicitud GET a la URL del archivo que deseas descargar. Luego, se verifica el estado de la respuesta utilizando `response.raise_for_status()` para asegurarse de que no haya ocurrido ningún error durante la descarga.

Después de eso, se abre un archivo en modo de escritura binaria (`'wb'`) y se escribe el contenido de la respuesta en el archivo utilizando `response.content`. Finalmente, se imprime un mensaje indicando que la descarga se ha completado.

Otra forma de descargar archivos un poco mas pesado de servidores, es la siguiente:

```Python

import requests

URL = 'https://codigofacilito.com/images/cody'

response = requests.get(URL, stream=True)

if response.status_code == 200:
	with open('images/cody.png', 'wb') as file:
		for chunk in response.iter_content(1024):
			file.write(chunk)
			
```

Al utilizar `stream=True` en la solicitud GET, se obtiene la capacidad de descargar el archivo en trozos (chunks) en lugar de descargarlo completo de una vez. Esto puede ser útil para archivos grandes, ya que se pueden procesar y guardar en el disco en pequeños fragmentos, lo que reduce la carga de memoria.

En el código, se realiza una solicitud GET a la URL especificada y se verifica si el estado de la respuesta es 200 (éxito). Si es así, se abre un archivo en modo de escritura binaria (`'wb'`) y se iteran los trozos de contenido de la respuesta utilizando `response.iter_content()`. Luego, cada trozo se escribe en el archivo.

Es importante destacar que este código asume que la URL proporcionada apunta a un archivo de imagen (`cody.png` en este caso). Asegúrate de ajustar la URL y el nombre del archivo según tus necesidades.

### Cookies
Las cookies son pequeños archivos de texto que se almacenan en el navegador del usuario cuando visita un sitio web. Se utilizan para almacenar información relacionada con la sesión del usuario y permiten realizar un seguimiento de sus acciones en el sitio web.

En Python, puedes trabajar con cookies utilizando el módulo `requests`. Puedes enviar cookies en tus solicitudes HTTP o recibir y manipular las cookies establecidas por el servidor en las respuestas.

Para enviar cookies en una solicitud, puedes utilizar el parámetro `cookies` de `requests.get()` o `requests.post()` para pasar un diccionario de cookies. Por ejemplo:

```python
import requests

url = 'http://example.com'
cookies = {'session_id': '123456', 'user_id': '987654'}

response = requests.get(url, cookies=cookies)
```

En este ejemplo, se envían dos cookies llamadas "session_id" y "user_id" en la solicitud GET.

Para recibir y manipular las cookies establecidas por el servidor en las respuestas, puedes acceder al atributo `cookies` del objeto de respuesta (`response.cookies`). Esto te permitirá obtener información sobre las cookies recibidas y configurar cookies personalizadas para las siguientes solicitudes. Por ejemplo:

```python
import requests

url = 'http://example.com'

response = requests.get(url)

# Obtener todas las cookies establecidas por el servidor
cookies = response.cookies

# Obtener el valor de una cookie específica
session_id = cookies.get('session_id')

# Configurar una cookie personalizada para la siguiente solicitud
cookies_custom = {'custom_key': 'custom_value'}
response = requests.get(url, cookies=cookies_custom)
```

En este caso, `response.cookies` contiene un objeto `RequestsCookieJar` que permite acceder a las cookies individuales y sus valores. Puedes usar métodos como `get()` para obtener el valor de una cookie específica.


---

En resumen, el módulo `requests` de Python es una poderosa herramienta para trabajar con solicitudes HTTP de manera sencilla y eficiente. Proporciona una interfaz fácil de usar y ofrece muchas funcionalidades para interactuar con servidores web y consumir APIs.