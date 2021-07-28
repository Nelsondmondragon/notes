# Apuntes
1. ## Que es JavaScript?

Surge de la necesidad de crear paginas dinamicas.

**JS es un lenguaje interpretado, orientado a objetos, debilmente tipado y dinamico.**

- POO: Utiliza el concepto de clases y objetos que nos permite hacer codigo reutilizable.

- Debilmente Tipado: Nos permite hacer operaciones con diferentes tipos de datos.

  Ej ->  *4 + "8"; // 48*

- Dinamico: No necesita ser compilado previamente.

#### JavaScript es un lenguaje interpretado?.

    Es interpretado por el motor del navegadro, el cual se encarga de traducir nuestro codigo a bytecode.

#### JS es Backwards Compatible:
    Las versiones nuevas no rompen nuestro codigo viejo, pero no las podemos utilizar hasta que se hagan estandar, para que el navegador lo entienda sin problema.

#### JS compilador BABEL
    Compilador que permite utilizar las nuevas versiones.

2. # Por que JS?

 - Desarrollo web.
 - Desarrollo de apps.
 - Desarrollo de apps para desktop.
 - Back-end/IOT

3. # Elementos de un lenguaje de programacion: Variables, Funciones y Sintaxis.

Dos componentes principales:
- Data que guardamos en memoria.
- Tareas (Funciones) que haremos con esa data.

4. # Variables en JS

Representacion de algun lugar en memoria para guardar un valor.

5. # Funciones JS

- Declarativas: Va a inicializar un valor y lo guarda en memoria.
```javascript
    function(){
        return 1;
    }
```
- Expresion:Variable donde guardamos la funcion en memoria.
```javascript

var miFunction = function(a+b){
    return a+b;
}
```

6. # Scope
Alcance de las variables

7. # Hoisting

Las variables y las funciones se procesan antes algun codigo. 

8. # Coercion.
Coersion significa que es la forma en la que podemos cambiar un tipo a otro tipo de valor.

- Coercion implicita: 
El leguaje nos ayuda a cambiar de un tipo de valor a otro.
Ej:

```javascript 
var a = 4 + "7";
```

- coercion explicita: 
Es cuando obligamos a un tipo de valor a cambiar a otro tipo.

```javascript 
var c = String(a);
```

9. # Valores: Truthy y Falsy.
- Valores falsos:
    ```javascript 
    0,null,NaN, Undefined, false, "". 
    ```
- Valores Verdaderos:
    ```javascript
     "a",1,[],{},function(){},true
    ```

10. # Operadores: Asignacion, Comparacion y aritmeticos.

- Operadores binarios: Se realizan operaciones con dos valore.
   
   * +.
   * -.
   * *.
   * /.

- Operador de concatenacion

   ```javascript
   "nelson" + "cortes"
   "nelson cortes"
   ```
- Operadores unitarios: Un solo operador.
```javascript
console.log(!false);
//true
```
- Operadores de asignacion:
Se utiliza para asignar valores a una variable.
```javascript
var a = "j"
```
- Operadores de comparacion:
  
```javascript
  3=="3" // Compara el valor
  //salida -> true


  3==="3" //Compara el tipo de valor
  // Salida -> false

  3<5 // menor que
  5>3 //mayor que
  5<=6 //menor o igual que
  5>=5 //mayor igual que

  a && b // validar que se cumplan dos condiciones.
  
  a || b // alguna de las puede ser verdadera. 
```

11. # Condicionales

12. # Switch

13. # Arrays

Estructura de datos y de un tipo objeto, guarda mas valores adentro. 

```javascript
var frustas =["Manzana","Platano"];

```
- Metodos:
  * .push(elemento) <- agrega el elemento.
  * .pop(elemento) <- Eliminar el ultimo elemento.
  * .unshift(elemento) <- agrega un elemento en la posicion 0.
  * .shift(elemento) <- Elimina el elemento de la primera posicion.
  * .indexOf(elemento) <- buscar el index de cierto elemento.

14. # Loops: For y For...of

- For
```javascript
 for(int i = 0; i < estudiantes.length; i++){
     console.log(estudiantes[i]);
 }
```
- For...of
```javascript
   for(var estudiante of estudiantes){
       console.log(estudiante);
   }
```

15. # Loops: While

```javascript
while(estudiantes.length>0){
    console.log(estudiantes);
    estudiantes.shift();
}
```

16. # Objects

Es como llevamos un objeto del mundo fisico al paradigma de objetos de programacion.

17. # Objects: Funcion constructora.

Se le conoce como funcion constructora, nos permite crear un template.

Ej:
```javascript
function car(marca, model, annio){
    this.marca=marca;
    this.model=model;
    this.annio=annio;
}

var carNew= new car("Toyota", "Model 3", 2020);
```

18. # Metodos de Recorridos de Arrays

```javascript
var articles = [
   {name:"Bici", price:3000},
   {name:"Tv",price:2000},
   {name:"Libro",price:500},
   {name:"Laptop",price:250},
   {name:"Iphone",price:5000}
];

//Filter
var articleFilter = articles.filter(function(article){
  return article.price <= 500;
});

//map
var nameArticle = articles.map(function(article){
    return article.name;
});
```

19. # Recorriendo Arrays con .find(), .forEach y .some()

```javascript
var articles = [
   {name:"Bici", price:3000},
   {name:"Tv",price:2000},
   {name:"Libro",price:500},
   {name:"Laptop",price:250},
   {name:"Iphone",price:5000}
];

//.find()

var findArticle = articles.find(function(article){
 return article.name === "Laptop"
});

//forEach
articles.forEach(function(article){
 console.log(article.name);
});

//some <- comprueba si existe un objeto de acuerdo a la funcion establecida.

var articlesLowPrice = articles.some(function(article){
 return article.price <=500; 
});

```

20. # Eliminando elementos de un Array

 - .shift() -> elimina el primer elemento de un array.

 - .pop() -> Elimina el ultimo elemento de un array