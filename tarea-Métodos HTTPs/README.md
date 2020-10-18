## INTRODUCCION

# Métodos HTTPs

### GET

El método GET significa recuperar cualquier información (en forma de una entidad) identificada por el Request-URI. Si el Request-URI se refiere a un proceso de producción de datos, son los datos producidos los que se devolverán como entidad en la respuesta y no el texto fuente del proceso. Cabe señalar que todas las peticiones que usan el método GET, deberán recuperar únicamente datos.

#### Ejemplo:

1. GET /index.html HTTP/1.1  
2. User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT) 
3. Host: www.yosoy.dev 
4. Accept-Language: es-mx 
5. Accept-Encoding: gzip, deflate 
6. Connection: Keep-Alive 
 

### OPTION

El método OPTIONS representa una solicitud de información acerca de las opciones de comunicación disponibles en el canal de solicitud/respuesta identificada por el Request-URI. En otras palabras, éste método es el que utilizamos para describir las opciones de comunicación existentes de un recurso destino. Dato: El cliente como tal puede especificar una URL para este método o, en su lugar, utilizar un asterisco para referirse al servidor completo.

#### Ejemplo: 

Se necesita saber cuáles métodos de solicitud soporta el servidor de nuestra profesora, podemos utilizar curl y una solicitud OPTIONS:

	
1. curl -X OPTIONS https://yosoy.dev -i

#### HEAD

El método HEAD es muy similar al GET (funcionalmente hablando), a excepción de que el servidor responde con líneas y headers, pero no con el body de la respuesta.

#### Ejemplo:

1. GET /index.html HTTP/1.1  
2. User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
3. Host: www.yosoy.dev
4. Accept-Language: es-mx
5. Accept-Encoding: gzip, deflate
6. Connection: Keep-Alive
