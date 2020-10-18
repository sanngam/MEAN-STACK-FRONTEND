## INTRODUCCION

# Métodos HTTPs

### GET

El método GET significa recuperar cualquier información (en forma de una entidad) identificada por el Request-URI. Si el Request-URI se refiere a un proceso de producción de datos, son los datos producidos los que se devolverán como entidad en la respuesta y no el texto fuente del proceso. Cabe señalar que todas las peticiones que usan el método GET, deberán recuperar únicamente datos.

#### EJEMPLO

GET /index.html HTTP/1.1  
User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT) 
Host: www.yosoy.dev 
Accept-Language: es-mx 
Accept-Encoding: gzip, deflate 
Connection: Keep-Alive 
