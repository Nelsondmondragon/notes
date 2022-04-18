Artefactos nucleos de Angular 

- Pipes.
- Componentes.
- Servicios.
- Directivas.

# 1. Que son los componentes?
Se empieza abstraer todo en componentes.

- Componente generado tiene 4 archivos
    * component.html -> es la vista de nuestro componente.
    * component.scss -> estilos de nuestro componente.
    * component.spec.ts -> archivo para realizar pruebas.
    * component.ts -> contiene toda la logica, une al html y los archivos de estilo.


# 2. Uso de inputs

# 3. Uso de Outputs
El Output se usa con el EventEmitter

# 4. Componente de producto

# 5. Ciclo de vide de componentes

- Constructor: 
    * Crea la instancia de ese componente.
    * Corre antes del render.
    * se corre cada vez que se hace una instancia.
    * No  correr cosas async.

- onChanges:
    * Corre antes y durante del render siempre y cuando se detecten cambios en los inputs.
    - Evalua los cambios de los inputs.
 
- ngOnInit():
    * Corre antes del render, pero solo una vez.
    * Podemos correr cosas async 

- ngAfterViewInit():
    * Despues del render.

- ngOnDestroy():
    * Sucede cuando eliminemos todos los componentes 

# 6. ngDestroy & SetInput


# 7. Implementando el side Menu

# 8. Comunicacion padre e hijo

# 9. Conociendo los servicios
Es la forma en la que angular nos permite hacer modular nuestra aplicacion y apartar 
nuestra logica de negocio a nivel de codigo, manipular datos, hacer servicios compartidos para poder ser utilizados por toda la aplicacion.

Los servicios permiten modularizar y hacer elementos reusables.

# 10. Que es la inyeccion de dependecias?
- Angular marca los servicios con el decorador @Injectable, esto hace que se pueda inyectar en otros componentes.

- Los servicios pueden ser inyectados desde componentes.

- El motor de dependencias de angular utiliza el patron de dependencias Singleton.
- Singleton: Guarda en memoria una unica instancia de un servicio para devolverla a los demas componentes que la necesiten.
- Tener cuidado con la inyeccion circular.


# 11. Obteniendo datos de una API
- Angular Http -> @angular/common/http

- Angular por defecto maneja un patron llamado observable

# 12. Pipes
- Es una tuberia, tenemos una entrada, hacemos una transformacion y luego una salida.
- la salida de una tuberia puede ser la entrada de otra.

# 13. Construyendo mi propio pipe

# 14. Directivas
Se usa para la modificacion del DOM de forma directa y tambien se utiliza para modificar atributos.

# 15. Reactividad basica
State Management

# 16. Guia de estilos de angular y listiner
