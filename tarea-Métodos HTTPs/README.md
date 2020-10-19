## INTRODUCCIÓN

# [Métodos HTTPs](https://www.oscarblancarteblog.com/2018/12/03/metodos-http-rest/)

Los métodos HTTP definen la acción que se realizará sobre un determinado recurso. Los métodos HTTP, también suelen ser llamados HTTP Verbs. Aunque el nombre correcto es Verbs, la realidad es que, en la práctica, casi siempre son llamados “métodos”, por lo que utilizaremos el nombre “métodos” para referirnos a ellos.

## DESARROLLO

### [GET](https://yosoy.dev/peticiones-http-get-post-put-delete-etc/)

El método GET significa recuperar cualquier información (en forma de una entidad) identificada por el Request-URI. Si el Request-URI se refiere a un proceso de producción de datos, son los datos producidos los que se devolverán como entidad en la respuesta y no el texto fuente del proceso. Cabe señalar que todas las peticiones que usan el método GET, deberán recuperar únicamente datos.

#### Ejemplo:

1. GET /index.html HTTP/1.1  
2. User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT) 
3. Host: www.yosoy.dev 
4. Accept-Language: es-mx 
5. Accept-Encoding: gzip, deflate 
6. Connection: Keep-Alive 

### [HEAD](https://yosoy.dev/peticiones-http-get-post-put-delete-etc/)

El método HEAD es muy similar al GET (funcionalmente hablando), a excepción de que el servidor responde con líneas y headers, pero no con el body de la respuesta.

#### Ejemplo:

1. GET /index.html HTTP/1.1  
2. User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
3. Host: www.yosoy.dev
4. Accept-Language: es-mx
5. Accept-Encoding: gzip, deflate
6. Connection: Keep-Alive

### [POST](https://yosoy.dev/peticiones-http-get-post-put-delete-etc/)

El método POST es usado cuando se requiere enviar información al servidor como, por ejemplo, un archivo de actualización, información de formulario, etc. En otras palabras, éste método se usa cuando se necesita enviar una entidad para algún recurso determinado. La diferencia entre PUT y POST es que PUT es idempotente, mientras que si realizamos repetidas idénticas peticiones con el método POST, podría haber efectos adicionales como pasar una orden varias ocasiones.

#### Ejemplo: 

Se enviará información de formulario al servidor, que será procesada por un process.cgi:

1. POST /cgi-bin/process.cgi HTTP/1.1
2. User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
3. Host: www.yosoy.dev
4. Content-Type: text/xml; charset=utf-8
5. Content-Length: 88
6. Accept-Language: es-mx
7. Accept-Encoding: gzip, deflate
8. Connection: Keep-Alive

### [PATCH](https://www.oscarblancarteblog.com/2018/12/03/metodos-http-rest/)

Este método es similar al método PUT, pues permite actualizar un registro existente, sin embargo, este se utiliza cuando actualizar solo un fragmento del registro y no en su totalidad, es equivalente a realizar un UPDATE a la base de datos. Soporta el envío del payload


### [PUT](https://yosoy.dev/peticiones-http-get-post-put-delete-etc/)

El método PUT es usado para solicitar que el servidor almacene el cuerpo de la entidad en una ubicación específica dada por el URL.

#### Ejemplo:

Se solicita al servidor que guarde el cuerpo de la entidad dada en index.htm en la raíz del servidor:
	
1. PUT /index.htm HTTP/1.1
2. User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
3. Host: www.yosoy.dev
4. Accept-Language: es-mx
5. Connection: Keep-Alive
6. Content-type: text/html
7. Content-Length: 182


### [DELETE](https://yosoy.dev/peticiones-http-get-post-put-delete-etc/)

Este método es utilizado para solicitar al servidor que elimine un archivo en una ubicación específica dada por la URL. En otras palabras más simples, este método elimina un recurso determinado.

#### Ejemplo: 

Se le solicitará al servidor eliminar el archivo hello.htm en la ruta raíz del servidor:
1. DELETE /hello.htm HTTP/1.1
2. User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
3. Host: www.yosoy.dev
4. Accept-Language: es-mx
5. Connection: Keep-Alive

	
### [OPTIONS](https://yosoy.dev/peticiones-http-get-post-put-delete-etc/)

El método OPTIONS representa una solicitud de información acerca de las opciones de comunicación disponibles en el canal de solicitud/respuesta identificada por el Request-URI. En otras palabras, éste método es el que utilizamos para describir las opciones de comunicación existentes de un recurso destino. Dato: El cliente como tal puede especificar una URL para este método o, en su lugar, utilizar un asterisco para referirse al servidor completo.

#### Ejemplo: 

Se necesita saber cuáles métodos de solicitud soporta el servidor de nuestra profesora, podemos utilizar curl y una solicitud OPTIONS:

	
1. curl -X OPTIONS https://yosoy.dev -i


# Códigos de estado de HTTP

Los códigos de estado de respuesta HTTP indican si se ha completado satisfactoriamente una solicitud HTTP específica. 

#### 100-199 Respuestas informativas

Petición recibida, continuando proceso. Esta respuesta significa que el servidor ha recibido los encabezados de la petición, y que el cliente debería proceder a enviar el cuerpo de la misma (en el caso de peticiones para las cuales el cuerpo necesita ser enviado; por ejemplo, una petición Hypertext Transfer Protocol). Si el cuerpo de la petición es largo, es ineficiente enviarlo a un servidor, cuando la petición ha sido ya rechazada, debido a encabezados inapropiados.

#### 200-299 Respuestas satisfactorias 

Esta clase de código de estado indica que la petición fue recibida correctamente, entendida y aceptada. 

[ERROR 200](https://es.stackoverflow.com/questions/175843/error-en-http-response-code-200-sin-mostrar-el-resultado-esperado)

#### 300-399 Redirecciones

Esta clase de código de estado indica que una acción subsecuente necesita efectuarse por el agente de usuario para completar la petición. La acción requerida puede ser llevada a cabo por el agente de usuario sin interacción con el usuario si y solo si el método utilizado en la segunda petición es GET o HEAD. El agente de usuario no debe redirigir automáticamente una petición más de 5 veces, dado que tal funcionamiento indica usualmente un Bucle infinito. 

[ERROR 302](https://es.stackoverflow.com/questions/211228/jax-ws-error-http-302-found-dian-colombia) 

#### 400-499 Errores de los clientes
La solicitud contiene sintaxis incorrecta o no puede procesarse.

La intención de la clase de códigos de respuesta 4xx es para casos en los cuales el cliente parece haber errado la petición. Excepto cuando se responde a una petición HEAD, el servidor debe incluir una entidad que contenga una explicación a la situación de error, y si es una condición temporal o permanente. Estos códigos de estado son aplicables a cualquier método de solicitud (como GET o POST). Los agentes de usuario deben desplegar cualquier entidad al usuario. Estos son típicamente los códigos de respuesta de error más comúnmente encontrados. 

[ERROR 404](https://es.stackoverflow.com/questions/57467/error-http-404-0-no-encontrado-iis) 

[ERROR 403](https://es.stackoverflow.com/questions/334740/error-403-al-iniciar-aplicaci%c3%b3n)

[ERROR 405](https://es.stackoverflow.com/questions/28135/error-http-405-en-android) 

[ERROR 409](https://es.stackoverflow.com/questions/304271/solucionar-error-networkerror-there-was-an-error-in-the-connection-because-ht) 

[ERROR 422](https://es.stackoverflow.com/questions/185183/porqu%c3%a9-guzzle-5-0-lanza-el-error-422-si-estoy-armando-bien-la-consulta)

#### 500-599 Errores de los servidores
El servidor falló al completar una solicitud aparentemente válida.

Los códigos de respuesta que comienzan con el dígito "5" indican casos en los cuales el servidor tiene registrado aún antes de servir la solicitud, que está errado o es incapaz de ejecutar la petición. Excepto cuando está respondiendo a un método HEAD, el servidor debe incluir una entidad que contenga una explicación de la situación de error, y si es una condición temporal o permanente. Los agentes de usuario deben desplegar cualquier entidad incluida al usuario. Estos códigos de respuesta son aplicables a cualquier método de petición. 

[ERROR 500](https://es.stackoverflow.com/questions/229916/me-sale-error-http-error-500-en-formularo-php-y-msql) 

[ERROR 503](https://es.stackoverflow.com/questions/375225/http-error-503-ubuntu-18-04-allowoverride-all) 
