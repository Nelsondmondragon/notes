# Programacion Funcional:
Es un paradigma.
Casos especificos por resolver.

Se enfoca en que resolver, no en como resolver.
Lo importante es tener una funcion que resuelva el problema, no importa su procedencia.

En la parte de los datos vamos aprender la diferencia de los datos mutables e inmutables.

# Beneficios de la programacion funcional.

- Legibilidad
- Testing
- Concurrencia.
- Comportamientos mas definidos.
- Menos manejo de estados.
- Nohay que instalar nada adicional.

# 1. Que es una funcion en Java?

Es un tipo de dato que puedo operar sobre un dato "x" y generar un dato "y".

- Es una serie de pasos parametrizados.
- pueden o no devolver un resultado.
- Se puede definir, almacenar o declarar bajo demanda(como cualquier otro tipo.)

Podemos definir funciones con respecto a si mismas(Recursividad)

Podemos definir funciones que tomen otra funciones como parametros.

# 2. Funciones como ciudadanos de primera clase.
Ya son reconocidos por el lenguaje.
Es algo que podemos definir y utilizar.
Es algo dentro del leguaje que es usable y operable.

- Se pueden declarar variables de tipo funcion.
- Se pueden tomar como parametros de otras funciones.

capacidad que confiere Java 8 en adelante para tratar las funciones como Tipos de datos, que pueden declararse, recibirse cómo parámetros o enviarse (retornarse) cómo resultados.

# 3. Funciones puras:
- Es una funcion que genera el mismo resultado para el mismo parametro.

- Funcionan en aislamiento( no dependen ni las afecta el contexto)

- Son deterministicas: quiere decir que podemos predecir el resultado.

- No genera valores aleatorios.

- No genera efectos secundarios:
  * No cambia una base de datos.
  * No crea un archivo.
  * No modifica el sistema.

NOTA: No podemos invocar una funcion impura desde una funcion pura.

# 3.1 Funciones Impuras
Funciones que no son puras.
- Una funcion pura no puede invocar una funcion impura.
- Una funcion impura puede llamar un funcion impura.
# 4. Entendiendo los efectos secundarios.
Un efecto secundario es todo cambio observable desde fuera del sistema, ej: funcion que cambia el color de algo.

### Por que evitar los efectos secundarios?
- Nos ayuda a tener una mejor estructura de nuestro codigo.
- Tener mas funciones puras.
- Tener separadas mejor separadas las definiciones y responsabilidades de nuestro codigo.

No podemos tener codigo sin efectos secundarios, pero podemos reducirlos.

# 5. Funciones de orden mayor
- Toma una funcion como parametro
- Retorna una funcion como resultado.

### Ventajas:
- Pasar comportamientos.
- Compartir un medio de comunicacion.
- Compartir logica/reglas.

# 6. Funciones lambdas.
- Parten de un concepto matematico de los annos 30. (Alonzo Church)
- Son funciones anonimas.

### Funcion:  
- Tiene nombre

### Lambda: 
- No tiene nombre. 

### Por que usarlas?
- Es un compartamiento de uso unico.
- Una regla que solo se requiere en un lugar.
- Es una funcion extremadamente simple.

# 7. Revisando el paquete java.util.function: Function
Ahora las funciones tambien son tipos

# 8. Revisando el paquete java.util.predicate
Es un tipo de funcion que trabajo sobre un tipo pero genera un boolean, se encargo de testear si algo es valido.

# 9. Consumer y Supplier
- Consumer: consumidor, se encarga de consumir los datos que le pases.
- Supplier: proveedor, se encarga de suministrar datos.

# 10. Operators y BiFunction
- UnaryOperator: Solo especifica un tipo de dato. Se entiende que tendra como resultado el mismo tipo.

- BinaryOperator: Solo se especifica un tipo de dato. Se entiende que tendra 2 parametros de entrada y el uno de retorno del mismo tipo de dato.

- Bifunction: 2 parametros de entrada, se tiene que especificar el tipo de dato. Puede tener diferentes tipos de entradas como tambien diferente tipo de salida.

# 11. Entendiendo dos jugadores clave: SAM y FunctionalInterface:
- SAM: single abstract method. -> representa que es una interfaz que tiene un solo metodo sin definir.

# 12. Operadores de referencia 

```java
        List<String> profesores = getList("Nicolas", "Juan", "Zulema");
        Consumer<String> printer = text -> System.out.println(text);
        profesores.forEach(printer);
        System.out.println("/////////////");
        profesores.forEach(System.out::println);
```



# 13. Analizando la inferencia de tipos
Entender que para poder utilizar la referencia de otro metodo, necesitamos que ese metodo tambien reciba el mismo parametro y genere el mismo resulta, java en tiempo de compilacion va inferir estos datos para no tener que ponerlos explicitamente. 

# 14. Comprendiendo la sintaxis de las funciones lambdas
Son funciones anonimas.

- Los predicados tiene que devolver un boolean.

- Las funciones al ser interfaces tarbajan directamente sobre objetos, no trabajan sobre tipos de datos primitivos.

# 15. Usando metodos default en nuestras interfaces
Podemos tener definicon a traves de la cual se utilice el metodo abstracto, esto me da la versatilidad de yo poder crear una interfaz que realice querys a una base de datos. 

# 16. Chaining
Encadenar el resultado de una ejecucion con respecto a otra ejecucion.

# 17. Entendiendo la composicion de funciones.
Funcion de orden Mayor-> es una funciona que toma como parametro una funcion o devuelve como resultado una funcion, tambien pueden ser los dos casos. Con esto podemos generar composicion de funciones.

- #### Compose:
Toma una funcion, ejecuta esa funcion primero y despues ejecuta sobre la cual se mando a llamar.

# 18. La clase Optional
La intencion de la clase, es que apartir de tus predicados, funciones o etc, no tengas que preocuparte por el valor de retorno directamente.

- Consumer: es una funcion que va tomar un dato y no va retornar ningun resultado.
- supplier: funcion que nos va generar un nuevo dato.

La clase optional es manera del cual no tenemos certeza si el valor esta o no presente. Y poder acceder a este dato mediante operadores, funciones.

# 19. Entendiendo que son los stream
Es una especie de lista que tiene elementos y se pueden iterar, los stream son autoiterables

- Un stream solo puede ser consumido una vez

- Operacion intermedia -> si te devuelve un stream es intermedia.

- Operacion final -> Si te devuelve cualquier otro tipo de data, incluso un void es una operacion final.

# 21. Operaciones y collectors
#### Repaso:

- ```Consumer<T>``` : recibe un dato de tipo T y no genera ningun resultado.
- ```Function<T,R>```: toma un dato de tipo T y genera un resultado de tipo R
- ```Predicate<T>``` : toma un dato de tipo T y evalua si el dato cumple con una condicion.
- ```Supplier<T>``` : no recibe ningun dato, pero genera un dato de tipo T cada vez que es invocado.
- ``` UnaryOperator<T>```: Recibe un dato tipo T y genera un resultado tipo T.

```java
.collect(Collectors.toList());
```

# 22. Stream de tipo especifico y paralelismo
.allMatch -> validar que todos los elementos cumplen con una codicion.


# 23. Operaciones terminales
Son aquellas que como resultado no generan un nuevo stream.
Generics

## Operaciones terminales de coincidencia
- AnyMatch: Nos indica si un stream contiene un elemento segun el predicate que le pasemos.

- allMatch: Nos indica si todos los elementos de un stream cumplen con un cierto predicate.

- noneMatch: Nos indica si todos los elementos de un Stream no cumplen un cierto Predicate.

## Operaciones terminales de busqueda
- findAny: tarate de devolver un optional con cualquier elemento presente en el stream de forma no determinista(random).
- findFirst: Si el stream tiene definida una operacion de ordenamiento retorna un optional conteniendo el primer valor, de lo contrario funciona igual que findAny.


En casos vacios las dos opciones retornan un Optional.

## Operaciones terminales de reduccion
- min: Obtener el elemento mas pequenno usando un comparator.
- max: Obtener el elemento mas grande usando un comparator.

En casos vacios las dos opciones retornan un Optional.


- reduce(BinaryAccumulator)
Retorna un Optional del mismo tipo que el Stream, con un solo valor resultante de aplicar el BinaryAccumulator sobre cada elemento o Optional.empty() si el stream estaba vacío. Puede generar un NullPointerException en casos donde el resultado de BinaryAccumulator sea null.

```java
Stream aLongStoryStream = Stream.of("Cuando", "despertó,", "el", "dinosaurio", "todavía", "estaba", "allí.");
Optional longStoryOptional = aLongStoryStream.reduce((previousStory, nextPart) -> previousStory + " " + nextPart);
longStoryOptional.ifPresent(System.out::println); //"Cuando despertó, el dinosaurio todavía estaba allí."
```


- reduce(valorInicial, BinaryOperator)
Retorna un valor del mismo tipo que el Stream después de aplicar BinaryOperator sobre cada elemento del Stream. En caso de un Stream vacío, el valorInicial es retornado.

```java
Stream<Integer> firstTenNumbersStream = Stream.iterate(0, i -> i + 1).limit(10);
int sumOfFirstTen = firstTenNumbersStream.reduce(0, Integer::sum); //45 -> 0 + 1 + … + 9
```

- reduce(valorInicial, BinaryFunction, BinaryOperator)
Genera un valor de tipo V después de aplicar BinaryFunction sobre cada elemento de tipo T en el Stream y obtener un resultado V.

Esta version de reduce usa el BinaryFunction como map + reduce. Es decir, por cada elemento en el Stream se genera un valor V basado en el valorInicial y el resultado anterior de la BinaryFunction. BinaryOperator se utiliza en streams paralelos (stream.parallel()) para determinar el valor que se debe mantener en cada iteración.
```java
Stream aLongStoryStreamAgain = Stream.of("Cuando", "despertó,", "el", "dinosaurio", "todavía", "estaba", "allí.");
int charCount = aLongStoryStreamAgain.reduce(0, (count, word) -> count + word.length(), Integer::sum);
```

- Count: Una operación sencilla: sirve para obtener cuantos elementos hay en el Stream.
```java
Stream yearsStream = Stream.of(1990, 1991, 1994, 2000, 2010, 2019, 2020);
long yearsCount = yearsStream.count(); //7, solo nos dice cuantos datos tuvo el stream.
```

- toArray: Agrega todos los elementos del Stream a un arreglo y nos retorna dicho arreglo. La operación genera un Object[], pero es sposible hacer castings al tipo de dato del Stream.

- collect: Mencionamos la operación collect en la lectura sobre operaciones y collectors, donde mencionamos que:Collector es una interfaz que tomara datos de tipo T del Stream, un tipo de dato mutable A, donde se irán agregando los elementos (mutable implica que podemos cambiar su contenido, como un LinkedList) y generara un resultado de tipo R.


## Operaciones terminales de iteracion
- ForEach: es una operacion que recibe un Consumer y no tiene un valor de retorno(void). La principal utilidad de esta operacion es dar un uso final a los elementos de stream.

```java
Stream> courses = getCourses();
courses.forEach(courseList -> System.out.println("Cursos disponibles: " + courseList));
```

Nota: La operaciones terminales se encargan de dar un fin y liberar el espacio usado por un Stream. 

```java
Stream infiniteStream = Stream.iterate(0, x -> x + 1);
List numbersList = infiniteStream.limit(1000)
    .filter(x -> x % 2 == 0) // Operación intermedia
    .map(x -> x * 3) //Operación intermedia
    .collect(Collectors.toList()); //Operación final
```


# 24. Operaciones intermedias
Se le dice operacion intermedia a toda operacion dentro de un stream que como resultado devuelva un nuevo Stream. Es decir, tras invocar una operacion intermedia con un cierto tipo de dato, obtendremos como resultado un nuevo stream conteniendo los datos ya modificados.

## Operaciones Disponibles: 
- filter(…)
- map(…)
- flatMap(…)
- distinct(…)
- limit(…)
- peek(…)
- skip(…)
- sorted(…)

# 25. Collectors

Siempre buscamos la manera de convertir nuestro stream a algo operable.

# 26. Job-search Un proyecto para encontrar trabajo


### Herramienta Gradle:
Nos va a permitir ejecutar tareas que son frecuentes en un proyecto de desarrollo, compilar el proyecto, generar un archivo zip o simplemente correr o ejecutar una aplicacion.

- setting.gradle: Nos permite tener las configuraciones globales de nuestro proyecto

- build.gradle: Es un archivo que trae la configuracion de como se hara la construccion de nuestro proyecto.

# 27. Revisando las opciones de nuestro CLI

- Jcoommander: nos va ayudar a transformar lo que recibamos por terminal a objetos JAVA.
- Feign-core: Se encarga de realizar peticiones web,el resultado viene en formato JSON.
- Feign-Gson: nos permite convertir JSON a objetos de java.