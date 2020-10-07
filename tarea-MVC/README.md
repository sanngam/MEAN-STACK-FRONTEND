## INTRODUCCION

# MVC

Controlador de vista de modelo (MVC)

MVC es un patrón de diseño que se utiliza para desacoplar la interfaz de usuario (vista), los datos (modelo) y la lógica de la aplicación (controlador). Este patrón ayuda a lograr la separación de preocupaciones.

Al utilizar el patrón MVC para sitios web, las solicitudes se enrutan a un controlador que es responsable de trabajar con el modelo para realizar acciones y / o recuperar datos. El controlador elige la vista que se mostrará y le proporciona el modelo. La vista representa la página final, según los datos del modelo.[https://dotnet.microsoft.com/apps/aspnet/mvc]

## DESARROLLO
### Frameworks que utilizan el modelo MVC

 #### CodeIgniter [https://www.hostinger.mx/tutoriales/mejores-frameworks-php/]
 CodeIgniter es un framework PHP que usa una arquitectura de Model View Controller (MVC). En términos sencillos, eso significa que CodeIgniter utiliza diferentes componentes para manejar tareas de desarrollo específicas. Este enfoque es muy popular entre los desarrolladores porque permite crear aplicaciones web altamente escalables con un tamaño más reducido.
 
 Características principales:

    Utiliza un framework ligero, hecho pensando en el rendimiento.
    Comienza rápidamente, gracias a la simplicidad del framework y la excelente documentación.
    Crea aplicaciones escalables utilizando la arquitectura basada en MVC.
    
   #### Zend
   Mucha gente se refiere a Zend como un framework de «pegamento», que es una forma de referirse a su naturaleza basada en componentes. Zend es un framework basado en MVC, orientado a objetos, que permite cargar solo los componentes que quieres como bibliotecas individuales.
   
   Características principales:

    Utiliza un framework PHP orientado a objetos con una arquitectura MVC.
    Reutiliza tu código gracias al diseño de la plataforma.
    Integra Zend con bibliotecas externas fácilmente.
    Usa solo los componentes que desees e ignora todo lo demás.
    
  #### Phalcon
  Phalcon es un poco extraño en el mundo de los frameworks PHP. Su código fuente está escrito en C, por lo que es básicamente una extensión C de PHP. Esto suena raro, pero en la práctica, resulta ser uno de los frameworks más rápidos que hemos tenido el placer de usar.

En cuanto al rendimiento, Phalcon le hace honor a su nombre y entrega resultados consistentes. Phalcon también es muy ligero en cuanto a recursos, y utiliza una arquitectura MVC. Además, es único porque el framework en sí mismo casi no tiene archivos una vez que lo instalas.

Características principales:

    Usa un framework PHP basado en C.
    Aprovecha el fantástico rendimiento de Phalcon y la reduce sobrecarga de recursos.
    Utiliza solo los módulos y bibliotecas que necesitas.
    
 #### CakePHP
 A principios de la década del 2000, CakePHP fue el primer framework MVC de PHP en salir al mercado. En ese entonces fue una revelación, y sigue siendo uno de los mejores frameworks PHP que puedes usar (y uno de los más populares).

Las nuevas versiones de CakePHP han mejorado su rendimiento a lo largo del tiempo y han agregado muchos componentes nuevos. Sin embargo, donde CakePHP realmente se destaca es en la forma en que aborda las convenciones de programación. Esto significa que con CakePHP, una vez que domines tu conjunto de convenciones, puedes centrarte en el desarrollo y hacer más trabajo más rápido.

 Características principales:

    Aprovecha un amplio conjunto de componentes.
    Usa las convenciones de CakePHP para programar proyectos más rápido.
 
 ### Ventajas que ofrece el modelo MVC
  Entre las principales ventajas que puede ofrecernos un desarrollo MVC podemos destacar las siguientes:

   -Separación clara de dónde tiene que ir cada tipo de lógica, facilitando el mantenimiento y la escalabilidad de nuestra aplicación.
   
   -Sencillez para crear distintas representaciones de los mismos datos.
   
   -Facilidad para la realización de pruebas unitarias de los componentes, así como de aplicar desarrollo guiado por pruebas (Test Driven Development o TDD).
   
   -Reutilización de los componentes.
   
   -No existe ciclo de vida de las páginas. Con menos peso, menos complejidad.
   
   -Motor de Routing asociando una URL concreta con su correspondiente controlador, permitiendo URL semánticas. Las URL semánticas se indexan mejor en los buscadores, siendo más adecuadas para el posicionamiento web.
   
   -Recomendable para el diseño de aplicaciones web compatibles con grandes equipos de desarrolladores y diseñadores web que necesitan gran control sobre el comportamiento de la aplicación. [https://marketiweb.com/empresa/blog/item/114-que-es-la-arquitectura-mvc-y-cuales-son-sus-ventajas]
   
   ### Otros modelos/frameworks de patrones de diseño que existen
  
   Modelo–Vista–Presentador (MVP) es una derivación del patrón arquitectónico modelo–vista–controlador (MVC), y es utilizado mayoritariamente para construir interfaces de usuario. En MVP el presentador asume la funcionalidad del "medio-hombre". En MVP, toda lógica de presentación es colocada al presentador.

Un patrón de diseño llamado MVVM (Modelo-Vista-Vista-Modelo) aplicado a Xamarin Forms. Algunas de las caracteríticas más importantes que se obtienen al usar patrones de diseño:

    Código más limpio y organizado.
    Mayor claridad y mejor comprensión del proyecto frente a otros desarrolladores.
    Reutilización de código
    Mantenimiento más rápido






