1. # HTML Y CSS DEFINICION Y USOS:
	
	World wide web <- Tim Berners-lee

	#### Tecnologias base de internet.

	- HTTP : Protocolo de tranferencia de hipertexto(Hyper Text Transfer Protocol) es la base que permite la comunicion de datos entre los dispositivos conectados en la red, ejemplo: computadores o servidores.

	- URL : Localizador de recursos uniforme(Uniform Resource Locator) Conocido como la direccion de un sitio web, es la manera en que le agregamos un nombre a un punto de la red
	
	- HTML : Leguaje de marcado de Hipertexto(Hyper Text Markup language)
	lenguaje para describir la estructura de la paginas web. 


	1994 <- nace el primer borrador de los Cascade Style Sheets(css) <- Serie de reglas que describen la apariencia de una pagina web.

	Responsive Design
2. # QUE SON Y PARA QUE NOS SIRVEN HTML Y CSS?
	
	- HTML <- Lenguaje de marcado, nos permite estructurar nuestros sitios web.

	- CSS <- Lenguaje de hojas de estilos, estilizar las paginas web. 

3. # DOM, CSSOM, RENDER TREE Y EL PROCESO DE RENDERIZADO DE LA WEB.

	* DOM(Document object Model) <- Es una tranformacion del codigo HTML escrito por nosotros a objetos entendibles por el navegador.

	* CSSOM <- es una representacion de objetos de nuestros estilos en css para que sean entendibles por el navegador.

	* RENDER TREE <- Union entre el DOM y el CSSOM para renderizar todo el codigo de nuestra pagina web.


	Pasos que sigue el navegador para construir las paginas web.

	1. Procesa el HTML para construir el DOM.

		Pasos del procesado del  HTML
		1. Bytes <- Transforma el codigo en Bytes
		2. Characters <- Tranforma los bytes a caracteres especificados en el codigo Ejemplo UTF-8
		3. Tokens <- Transforma los caracteres en los tags 
		4. Nodes <- Transforma los tokens en objetos.
		5. DOM <- Arbol estructurado de los nodes


	2. Procesa el CSS para contruir el CSSOM.

		Se crea un arbol estructurado del css.

	3. El DOM se une con el CSSOM para crear el Render Tree.
	4. Se aplican los estilos CSS en el Render Tree.
	5. Se "Pintan" los nodos en la pantalla para que los usuarios vean el contenido de la pagina web. 

4. # ANATOMIA DE UN ELEMENTO HTML: ATRIBUTOS, ANIDAMIENTO Y ELEMENTOS VACIOS.

	- Atributos <- Deben ir en la etiqueta de apertura
	- Anidamiento <- Elementos que estan dentro de otros, se le conoce como anidamiento.
	- Elementos vacios <- No tienen etiquetas de cierre, solo etiqueta de apertura y atributo.

5. # ANATOMIA DE UN DOCUMENTO HTML: DOCTYPE, HTML, HEAD Y BODY

6. # LA IMPORTANCIA DEL CODIGO SEMANTICO.
	* La semantica HTML no es mas que darle sentido y estructura a lo que estas escribiendo.

	* Influye en el ranking de busquedas de la pagina (SEO)

	* Accesibilidad.

7. # TIPOS DE ERRORES EN HTML, DEBUGGIN Y SERVICIO DE VALIDACION DE ETIQUETAS.

	* Errores sintacticos: Son errores de escritura en el codigo que hacen que el programa no funcione.

	* Errores logicos: En estos errores la sintaxis es correcta, pero el codigo no hace lo que deberia, por lo que el programa funciona de forma incorrecta. 

8. # ANATOMIA DE UNA DECLARACION CSS: SELECTORES, PROPIEDADES Y VALORES.

	- Anatomia de una declaracion css.
```css
		P(Selector){
			color(propiedad):red(valor);
		}
```
9. # TIPOS DE SELECTORES, PSEUDO-CLASES Y PSEUDO-ELEMENTOS

	- Tipos de selectores:
		* Universal<- *
		* Tipo <- h1
		* Calse <- .greeting
		* Id <- #id

	- Pseudo-clases
```css
		p:first-child{
			color:red;
		}
		p:last-child{
        	color:chartreuse;
    	}
    	p:nth-child(2n){
       	 	color: blueviolet;
    	}
    	p:nth-child(2n+1){
        	color: aqua;
    	}
```
- Pseudo-Elementos

```css
    p::first-letter{
        color: red;
        font-size: 20px;
    }
```
 10. # MODELO DE CAJA

 	margin
 		border
 			padding
 				1319x53


 11. # VALORES RELATIVOS Y ABSOLUTOS.

- Unidades de medida absolutas<- cm, px, mm, in, pt, pc

- Unidades de medida relaticas<- em, vmax, vh, %

 12. # FUNCIONES DE LAS PROPIEDADES DE CSS MAS USADAS.

 13. # POSICIONAMIENTO EN CSS.

 14. # QUE SON Y PARA QUE NOS SIRVEN LAS ARQUITECTURAS CSS?

- Predecible. <- Establecer reglas claras.
- Reutilizable. <- Reutilizar codigo.
- Mantenible. <- Codigo mantenible.
- Escalable. <- Crecimiento de la aplicacion sin afectar el rendimiento.

- Buenas Practicas.
- Establecer reglas.
- Explicar la estructura base.
- Establecer estandares de codificacion.
- Evitar largas hojas de estilo.
- Documentacion

 15. # OOCSS, BEM, SMACSS, ITCSS Y ATOMIC DESIGN

- OOCSS<- Separa el diseno del contenido.
- BEM(Block element modifier) <- Separa los bloques, los elementos y los modificadores.
- SMACSS <- Scalable and Modular architecture for CSS.

Para realizar esta metodologia se deben complir 7 pasos.

1. Base : Dividir nuestro css en componentes bases, los componentes son los elementos de nuestras aplicacion.
2. Layotu : Elementos utilizados en la pagina una sola vez, ejemplos el header o el footer.
3. Module : Son componentes que utilizamos en nuestra aplicacion mas de una vez.
4. State : Los estados que generan las acciones en nuestros componentes.
5. Themes : Separar los temas del codigo, para solo trabajar en el tema.

- ITCSS <- Nos permite dividir nuestros archivos de css para que no se combinene entre si.

 		7. Ajustes.
 		6.Herramientas.
 		5.Generico.
 		4.Elementos.
 		3.Objetos.
 		2.Componentes.
 		1.Uitlidades.

- ATOMIC DESIGN <- Basada en que el css sea mas escalable y modular

1. Atomos.
2. Moleculas.
3. Organismos.
4. Templates
5. Paginas.

16. # QUE ES UN COMPONENTE? ANALICEMOS NUESTROS DISENOS.

Un componente es un elemento que podemos utilizar para contruir futuros componentes

17. # ESTRUCTURA CON HTML Y BEM DE UN MENU DESPLEGABLE.

18. # ESTILIZANDO NUESTRO MENU DESPLEGABLE CON CSS

19. # FexBox

#### Que es Flexbox y para que nos sirve?

Nos permite alinear elementos .

link [https://flexboxfroggy.com/#es]

20. # Nuevo sistema de layout: CSS Grid.

Podemos manejar todo nuestro layout, nos permite ubicar elementos en una rejilla, si no que tambien nos ayuda con todo el sistema de Layout.

link [https://cssgridgarden.com/#es]

##### Nota: Nuestras paginas pueden estar construidas con felxbox y css grid.


21. # Maquetacion de la pantalla de login: Estructura HTML.

Practica.

22. # Maquetacion de la pantalla de login: Estilizacion con CSS.

Practica.


23. # Media Queries.

La idea es ajustar todos los disennos a dispositivos mas pequenno. 

```css
@media only screen and (max-width: 600px){
    .login__container{
        background-color: transparent;
        border: none;
        padding: 0px;
        width: 100%;
    }
    .footer{
        align-items: flex-start;
        flex-direction: column;
    }
}
```


24. # Maquetacion de la pantalla principal.

	Practica


25. # Maquetacion de la pantalla de Not Found.

Practica.

26. # Que es un preprocesador, cuales existen y cuales son sus diferencias.?

Para evitar tantas lineas de codigo en CSS, se utilizan los preprocesadores de CSS, los cuales extienden funcinalidades de CSS comun, permitiendonos tener variables, funciones, mixins, reutilizacion de codigo, flexibilidad en el desarrollo, etc.

Un preprocesador se escribe con una sistaxis especial que nosotros le indicamos y de compilarse en CSS para ser comprendido por el navegador.

#### Preprocesadore mas conocidos: La sintaxis depende de cada preporcesador.
1. LESS.
2. SASS.
3. Stylus.

27. # Instalacion de SASS y configuracion Inicial.

28. # Hablemos de variables, herencia, anidamiento, operadores y mas.

#### Variables

```css
$white: white;

.login__container--register a{
	color: $white;
}
```

#### Anidamiento

```css
	.login__container--register{
		font-size: 14px;

		a{
			color: $white;
			font-weight: bold;
			font-size: 16px;
		}
	}

```
#### extends
```css
.flex{
	display: flex;
	align-items: center;
}

.header{
	@extend .flex;
}
```
#### Mixin

```css
@mixin flex{
	display: flex;
	align-items: center;
}

.header {
	@include flex;
}
```
29. # La accesibilidad y nuestra responsabilidad como desarrolladores.

Debemos tener en cuenta a las personas con discapacidad visual, que no tienen la posibilidad de ver lo mismo que la mayoria de nosotros.Estas personas no siempre usan el mouse, sino lectores de pantalla.

30. # StoryBook

Es una guia para documentar todos los componenrtes de nuestra aplicacion, asi va ser mucho mas sencillo mirar que componentes tenemos, que comportamientos tienen, entonces nos permite hacer una especie de libreria donde podemos ver todos nuestros compoenentes en accion.

Documentacion

`link` https://storybook.js.org/docs/html/get-started/introduction/