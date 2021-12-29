# 1. Que es ecmascript?

Esmascript es la especificacion de lenguaje propuesto por Ecma Internacional(Institucion encargada de los estandares) y javaScript es el lenguaje de programacion que utiliza esta especificacion para trabajar sobre estas caracteriticas que van siendo annadidas anno con anno a partir del 2015.


# 2. Default Params y Concatenacion

- Parametros por defecto: Establecer los parametros de una funcion por defecto

```javascript
//Antes de ecmascript6
function newFunction(name,age, country){
    var name = name || 'nelson';
    var age = age || 32;
    var country =country || 'CO';
    console.log(name,age,country);
}

//Despues de es6
function newFunction2(name ='Nelson', age=32,country='COL'){
    console.log(name,age,country)
};

```
- Concatenacion:

```javascript
//Antes de es6
let hello = "Hello";
let world = "world";
let epicPhrase = hello + ' ' + world;




//Despues de es6
//Temple literals y la interpolacion de cadenas.

let epicPhrase2 = `${hello} ${world}`;

console.log(epicPhrase2);

```

# 3. Lef y Const, multilinea,Spread Operator y Desestructuracion. 

- Multilinea. 

```javascript

//Multilinea anstes de es6

let lorem = "ecmascript practica\n"
+ "ecmascript practica dos frase";

//Multilinea despues de es6

left lorem2 =`ecmascript multilinea
ahora esto hace un salto de linea`;

console.log(lorem);
console.log(lorem2);

```

- Desestruturacion de elementos

```javascript
let person = {
    'name': 'nelson',
    'age': '22',
    'country': 'CO'
}

//Para acceder a los atributos de un objeto anstes de es6

console.log(person.name,person.age);

//desestructuracion de elementos con es6
let{name,age}=person;
console.log(name,age);


```

- Operador de propagacion

```javascript 
 let team1 = ['Nelson','Cristian','Gustavo'];
 let team2 = ['Valentina','Ximena','Sofia'];

 let education = ['Daniela', ...team1,...team2];

```
- Diferencia entre let y var.

var -> asignar de una manera global

lef -> solo esta disponible en el bloque de codigo que fue definido.
```javascript 
{
    var globalVar = "Global Var";
}

{
    let globalLet = "Global let";
}

console.log(globalVar);
console.log(globalLet);
```
 - Const:

 Nos permite crear constantes. 


 # 4. Arrow Functions, promesas y parametros en objetos.

 - Propiedad de objetos mejora.
 ```javascript

let name = 'Nelson';
let age = '22';

//Antes de es6
obj = { name:name, age:age};

//despues de es6
obj2 = {name,age};
 ```

- Arrow Functions:
Son funciones anonimas.
Trabajan con un sentencia mas reducida y un this no vinculable.

```javascript
const names =[
    {name: 'Nelson', age: 22},
    {name: 'Gustavo', age: 27}
]

//Pasando una funcion anonima
let listOfNames= name.map(function(item){
    console.log(item.name);
})


//No pasamos la funcion anonima, directamente establecemos el elemento que necesitamos.
let listOfName2 = names.map(item => console.log(item.name));

const listOfName3 = (names, age) =>
{
    console.log(name,age);
}

//Cuando solo pasemos un elemento
const listOfName4 = name =>{
    console.log(name);
}

//Funcion mas simplificada con un elemento. 
const square = num=> num*num;

//Funcion mas simplificada con varios elementos.
const square = (num,num2) => num2*num*num;
console.log(square(23,2));
```

- Promesas: 
Significa que algo que establecemos va a pasar. 

```javascript
const helloPromise=()=>{
    return new Promise((resolve,reject) =>{
        if(true){
            resolve('Hey');
        }else{
            reject('Ups!!');
        }
    });
}

helloPromise()
    .then(response => console.log(response))
    .then(response => console.log(response))
    .cathc(error => console.log(error));
```

# 5. Clases, Modulos y Generadores

- Clases: Sintaxis mas clara para manejar objetos y la herencia en JS.

```javascript
class calculator{
    constructor(){
        this.valueA = 0;
        this.valueB = 0;
    }

    sum(valueA,valueB){
        this.valueA=valueA;
        this.valueB=valueB;
        return this.valueA + this.valueB;
    }
}

const calc = new calculator();
console.log(calc.sum(2,2));
```

- Modulos

```javascript
//Archivo module.js
const hello = () => {
    return 'hello';
}

//export default hello;  <- clase platzi.
module.exports= hello;


//Archivo index.js

//import {hello} from './module'; 
//hello(); <- Clase platzi.
const hello = require('./module');

console.log(hello());
```

- Generetors: Es una funcion especial que retorna una serie de valores de acuerdo al algoritmo definido.

```javascript
function * helloWorld(){
    if(true){
        yield 'Hello, ';
    }

    if(true){
        yield 'World';
    }
};

const generatorHello = hellorWorld();
console.log(generatorHello.next().value());
console.log(generatorHello.next().value());
console.log(generatorHello.next().value());


```

# 6. Que se implemento en ES7?

- Includes:
```javascript
let numbers= [1,2,3,4,5,6,76,7];
if(numbers.includes(7)){
    console.log(true);
}else{
    console.log(false);
}
```
- Potencias
```javascript
let base = 4;
let exponent = 3;
let result = base**exponent;
console.log(result);

```

# 7. Que se implemento en la es8

- Object Entries:
Nos permite devolver la clave y los valores de un objeto en una matriz.

```javascript
const data ={
    const data ={
        frontend: 'Nelson',
        backend: 'Gustavo',
        desing: 'Cristian'
    }
}

const entries = Object.entries(data);
console.log(entries);
```

- Object Values:
Me devuelve los valore de un objeto a un arreglo.

```javascript
const data ={
    const data ={
        frontend: 'Nelson',
        backend: 'Gustavo',
        desing: 'Cristian'
    }
}

const values = Object.values(data);
console.log(values);
```

- Padding: Nos permite modificar un string, es util en el fontend para mostrar una estructura de datos.

```javascript
const string = 'hello';

console.log(string.padStart(7,'hi'));

console.log(string.padEnd(12,' ----'));

console.log('food'.padEnd(12,' ----'));
```

- Trailing comas:
 Nos permite tener una sintaxis mas flexible al annadir mas elementos

 ```javascript
const ejem = {
   name: 'Nelson',
}
 ```

 - Caracteristicas Importantes de es8 
    
    * Async-Await

 ```javascript

const helloWorld = () => {
    return new Promise((resolve, reject) => {
        (true)
        ? setTimeout(() => resolve('Hello world'), 3000)
        : reject(new Error('Test Error'));
    })
};

const helloAsync = async () => {
    const hello  = await helloWorld();
    console.log(hello);
}

helloAsync();

const anotherFunction = async () => {
    try {
        const hello = await helloWorld();
        console.log(hello);
    } catch (error) {
        console.log(error);
        
    }
}
anotherFunction();

 ```

 # 8. Que se implemento en es9?

 - Operador de Reposo: nos permite extraer las propiedades de un objeto que aun no se ha construido. 

```javascript 
const obj = {
    namee : 'nelson',
    age: 22,
    country: 'CO'
};

let {namee,...all} = obj;
console.log(namee, all);
```

- Propiedades de propagacion en la union de objetos:

```javascript
const obj = {
    name: 'nelson',
    age: 23
}

const obj1 = {
    ...obj,
    country: 'COl'
}

console.log(obj1);
```

- Promise finally: podemos saber cuando ha termina el llamado y poder ejecutar alguna logica de codigo.

```javascript
const obj = {
    name: 'nelson',
    age: 23
}

const obj1 = {
    ...obj,
    country: 'COl'
}
```

- Regex: 

```javascript
const regexData = /([0-9]{4})-([0-9]{2})-([0-9]{2})/;
const match = regexData.exec('2018-04-20');
const year = match[1];
const month = match[2];
const day = match[3];

console.log(year, month, day);
```

# 9. Que se implemento en es10?

Salio en Junio 2019

- flat : Nos devuelve un matriz con cualquier submatriz aplanada aplanada

```javascript
let array = [1,2,3,4,[1,2,3,4,[1,2,3]]];

//Se le pasa de argumento el numero de niveles
console.log(array.flat(2));
```

- FlatMap: nos permite mapear cada elemento, despues pasarle una funcion y aplanarlo.

```javascript
let array = [1,2,3,4,5];
console.log(array.flatMap(value => [value, value *2]));
```

- trimStart: Nos permite eliminar los espacion al inicio de un string

- trimEnd: Nos permite eliminar los espacion al final de un string

- optional catch binding

```javascript
//normalmenmte
try {

}catch (error){
    error
}

//es10

try{

}catch{
    error
}

```
- From entries: Convertir un arreglo a un objeto, clave-valor.

```javascript

let entries = [['name','nelson'],['age',32]];

console.log(Object.fromEntries(entries))
```

- Object tipo mySymbl: nos permite acceder a una descripcion.

```javascript
let mySymbl = `My Symbol`;
let symbol - Symbol(mySymbl);
console.log(symbol.description);


```

# 10. Que se implemento en es11

- Dynamic Import: Vamos a realizar una importacion de algun elemento de forma dinamica para cuando necesitemos cargar un pieza de codigo,
nos permite dividir nuestro codigo para cuando lo necesitemos nada mas. 

- BigInt

```javascript
const aBigNumber= 9007199254740991n;
const anotherBigNumber = BigInt(9007199254740991);

console.log(aBigNumber);
console.log(anotherBigNumber);
```


- promiseAllSettled(): nos devuelve una promesa que se resuelve despues de que todas las promesas dadas se hayan cumplido o rechazado

```javascript
const promise1 = new Promise((resolve, reject) => reject("reject"));
const promise2 = new Promise((resolve, reject) => resolve("resolve"));
const promise3= new Promise((resolve, reject) => resolve("resolve 1"));

Promise.allSettled([promise1,promise2,promise3])
.then(response => console.log(response));
```

- globalThis : Tiene el valor global de this, que es similar al objeto global. 

- Operador de nulo: 

```javascript
const foo = null ?? 'deult string';
console.log(foo);
```

- Optional chaining(?): Podemos trabajar diferente niveles de estos recursos. No revienta la aplicacion

```javascript
    const user = {};
    console.log(user?.profile?.email);


    if(user?.profile?.email){
        console.log('email');
    }else{
        console.log('fail');
    }

```

# 11. Que se implemento en es11

- replaceAll: Nos permite reemplazar todas las coincidencia.

- promise.any : nos devuelva la primera que se resuelve.

- weekRef: Aseguramos que un elemento no se recogido por el recolector de basura.