# 1. Comandos Angular

- ng serve -o --port=3500 -> la bandera --port sive para escoger la configuracion del puerto que se quiera elegir.

- ng version dentro de un proyecto: Nos lista las dependencia que usamos y sus versiones.

# 2. Estructura de un proyecto angular

- browserslistrc: Indica en que versiones del navegador tiene que ser compatible la aplicacion.

- editorConfig: Reglas y normas claras dentro del equipo. necesario instalar el plugin -> EditorConfig

- tsConfig: Este archivo nos indica la configuracion de angular con typeScript, nos indica como va compilar, hacia donde va transpilar los archivos, que version de javaScript vamos a utilizar.
Tambien algunas configuracion del compilador de angular.

- Angular.Json: En este archivo podemos configurar diferentes ambientes. Tambien algunas configuraciones de compilacion de angular.

# 3. String {{Interpolation}}
Forma en la que podemos pasar datos desde el typeScript a nuestro template


# 4. Property [Binding]
Es la forma en la que podemos modificar atributos del HTML desde el typeScript.
Nota: Se recomienda que siempre se debe usar para configuracion de propiedades.

# 5. Event Binding

- Evento click
Se tiene en cuenta el evento y funcion.
```html
click()="onEven"
```

- evento scroll
```html
(scroll)="onScroll($event);
```

- event keyup:

```html
(keyup)="onKey($event);
```

# 6. Data binding con NgModel
Sirve mucho para los inputs.

Debemos importar el paquete de @angular/forms

# 7. Uso de *ngIf


# 8. Uso de *ngFor

# 9. Uso de *ngSwitch

Escenario de Angular online 
https://stackblitz.com/


# 10. Class and style

