## INTRODUCCION

# Métodos HTTPs

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


### [PUT](https://yosoy.dev/peticiones-http-get-post-put-delete-etc/)

El método PUT es usado para solicitar que el servidor almacene el cuerpo de la entidad en una ubicación específica dada por el URL.
Ejemplo:

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

Ejemplo: Se le solicitará al servidor eliminar el archivo hello.htm en la ruta raíz del servidor:
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




