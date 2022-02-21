# 1. Yin y Yanf de una app Frontend y Backend

Motor y corroceria de un producto digital.

Las aplicaciones tiene una cara visible y una logica.

### 1. Disenno:

- Ui DESIGN / UX DESIGN -> adobe xd, sketch, figma

### 2. Frontend 
- Html
- Css -> Bootstrap, tailwind, poundation
- JavaScript -> Angular, react, vue, Svelte.

NOTA: Con las tecnologias del punto 1 y 2 podemos contruir la cara visible de nuestra aplicacion. 

#### 3. Backend 
- Backend: podemos utilizar muchos lenguajes tales como:
    * JavaScript -> con NODE
    * PHP -> con LARAVEL
    * JAVA -> con SPRING
    * GO
    * PYTHON -> con FAST API,FLASK,DJANGO puedes elegir cualquiera. 

# 2. Framework vs .Libreria
Aunque lo parezcan, no son lo mismo.
- Libreria : Codigo escrito por otra persona.
- Framework: Marco de trabajo -> conjunto de reglas, librerias y estadares para contruir un producto digital.

# 3. Como se conecta el frontend con el backend?

La union del frontend y backend se realiza con un componente especial que se llama API(Interfaz de programacion de aplicaciones)

Dos grandes estandares:
- SOAP: Simple Object Access Protocol -> Protocolo simple de acceso a objetos. Mueve la informacion por medio del estandar XML(extensible Markup Language).

- REST: Representational state transfer -> tranferencia del estado representacional. Mueve la informacion a traves de JSON(JavaScript Object Notation)

# 4. HTTP

Lenguaje que hable internet HTTP(Hypertext Transfer Protocol), protocolo de transferencia de hiper textos.

En el internet siempre tenemos dos partes que se comunican:

- Cliente: Todos los dispositivos que tienes al alcance de tu mano. 
- Servidor: Una computadora encendida las 24 horas, que contiene la aplicacion que ves en tu cliente.

NOTA: Se le dice protocolo http porque tiene un conjunto de reglas que sirven para comunicar el cliente y el servidor.

Protocolos que tenemos en la Web:
- IP (internet protocol): protocolo fundamental, gracias al cual funciona internet, le da una direcion en particular a la computadora para que pueda ser encontrada en la red.

- TCP (transmision control protocol) y UDP (User datagram Protocol): Sirven para transmitir a traves del IP.

- TLS (Transport Layer Security): Sirve para que estos datos viajen de manera segura.

- DNS : Domain name system: Sirve para convertir una direccion IP en un dominio(nombre del proyecto que vas a ver en internet, ej: google.com).

- HTTP: Protocolo que usa los mencionados anteriormente para transmitir la informacion entre cliente y servidor en el internet.

NOTA: Por encima del protocolo http se transmite esta informacion, que puede venir en forma de HTML,CSS, JavaScript o Web APIs.

El servidor envia el HTML, CSS, JavaScript  a un cliente, para que el mismo mediante su navegador pueda representar la aplicacion web, a su vez el cliente envia una request http al servidor, para que el mismo mediante su API pueda contestar con los datos que van a venir en formato JSON, para que el cliente pueda los pueda aprovechar. 

# 5. Como es el flujo del desarrollo de una aplicacion web.

- #### Entorno Local
    * Editor de Codigo -> Tenemos nuestro codigo
    * Sistema de control de versiones. -> Sistema de control de versiones.
    * Entorno Local: ->     Formado por una direccion IP y un PORT, a este se le denomina LocalHost


- #### Entorno de desarrollo
    * Sistema de control de versiones en la nube.
    * CI/CD -> continuous integration/ continuous deployment, integracion y despliegue continuo. Esta herramienta prueba el codigo que tenemos en la nube.


- #### Servidor, Entorno de produccion

El servidor  guarda la aplicacion en lo que llamamos un dominio. 

# 6. El hogar de tu codigo: el servidor.

- Servidor: Una computadora que contiene una aplicacion y que la distribuye en internet, ademas es una computara la cual por medio del protocolo HTTP puedo pedirle mi aplicacion y traerla a mi cliente, que va ser mi computadora o dispositivo que este usando.

- Nube -> Servidores en algun lugar del mundo.

- Hosting -> Guardar una aplicacion en un servidor, no es mas que un espacio en un servidor donde tu aplicacion va ser guardada.

Diferentes tipos de Hosting:

- Iaas: (Infrastructure as a service): Se debe seleccionar cada vez que vas a tener en cuenta los recursos del servicor: ram, cpu , ssd.
    Opciones para Iaas:
    * Amazon web Services
    * Microsoft Azure
    * Digital Ocean
- PaaS: (Platform as a service): Provee una manera sencilla en la que el servidor se encarga de actualizar todas las aplicaciones que hacen que viva tu propia aplicacion, ej: BD, Aplicaciones de seguridad.
    Opciones para Paas: 
    * Google Aee Engine.
    * Firebase.
    * Heroku
- Saas: (Software as a service): Es una aplicacion que un proveedor te presta para hacer funcionar tu negocio

    Ejemplos:
    * Google Docs
    * Slack : Aplicacion de mensajeria.
    * WordPress: Te permite crear tu propia aplicacion web sin escribir codigo.

# 7. Proyecto: Disenno y bosquejo de una API.


API REST -> Motor de nuestra aplicacion y sirve para conectarse con el frontend.


Django -> frmawork de desarrollo web que necesita de un plugin denominado REST Framework

endpoint/route/path


protocolo, dominio, endpoint

### - Listado de endpoint de TWEETS:

- /tweets -> mostrar todos los tweets

- /post -> publish a tweet

- /tweets/{id} -> show a tweet

- /tweets/{id}/update -> update a tweet

- /tweets/{id}/delete -> delete a tweet

Model -> tipos de datos en particular que yo voy a manejar en mi aplicacion.

#### NOTA:
Los modelos se le conocen como tables en SQL. SQL es lenguaje que nos permite a nosotros trabajar con base de datos.

#### NOTA 1:
Cada uno de estos modelos que se les denominan tablas en SQL, contienen registros dentro de SQL.

### - Listado de endpoints para USERS:

- /user -> show all users.

- /signup -> Register a user.

- /user/ {id}/ -> show a user.

- /user/{id}/update -> update a user.

- /user/{id}/delete -> delete a user.


# 8. Que lenguaje y framework escoger.

- python :
    * Django: Un framework, facilidad de trabajar con datos, panel de administracion, comunidad enorme, documentacion enorme.
    * Flask: framework que nos permite trabajar con aplicaciones sencillas y flexibles.
    * Fast Api: Framework mas rapido para crear API.

- Javascript:
    * express: Framework simple, facil de escribir.
    * Nest: Framework con un nivel de complejidad mayor a express, nos permite aprovechar mejor el codigo.

- php:
    * Laravel: sintaxis mas facil, crear aplicaciones sencillas.
    * Symfony: Mas complejo, crear aplicaciones mas escalables.

- Go: permite contruir aplicaciones rapidas.
    * gin : framework por excelencia de GO.

    * BEEGO: framework en crecimiento.

- Ruby:
    * Rails.