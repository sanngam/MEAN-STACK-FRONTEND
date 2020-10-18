## INTRODUCCION

# Métodos HTTPs

### GET

El método GET significa recuperar cualquier información (en forma de una entidad) identificada por el Request-URI. Si el Request-URI se refiere a un proceso de producción de datos, son los datos producidos los que se devolverán como entidad en la respuesta y no el texto fuente del proceso. Cabe señalar que todas las peticiones que usan el método GET, deberán recuperar únicamente datos.

#### EJEMPLO

1. GET /index.html HTTP/1.1  
2. User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT) 
3. Host: www.yosoy.dev 
4. Accept-Language: es-mx 
5. Accept-Encoding: gzip, deflate 
6. Connection: Keep-Alive 
