# 1. Introduccion al pensamiento computacional.
### Objetivo:
- Aprender a resolver problema de manera computacional.
- Entender los puntos en comun entre todos los lenguajes de programacion.
- Desarrollar las bases para una carrera en Computer Science.

# 2. Introduccion al Computo:
Las computadoras nos permiten hacer calculos.

- Eniac: primera computadora digital, insertar un nuevo programa en esta computadora podria tardar semanas.

Se utiliza el sistema binario porque nos da ciertas ventajas sobre la electronica.

- Von neumann realiza la primera computadora EDVAC a la cual se le podia agragar el programa en memoria.



Arquitectra de Von neumann:

- input deivice
- Central Processing Unit:
    * Control Unit.
    * Arithmetic/Logic Unit
- Memory Unit
- Output Device.

### Computo y computadoras:
- Las computadoras hacen dos cosas:
    * Hacen calculos.
    * Recuerdan calculos.

# 3. Introduccion a los lenguajes de programacion:
- Telar de Jakart: nos permitio separar las intrucciones del producto final.


## Como dar instrucciones?
- Conocimiento declarativo vs imperativo.
    * Declarativos: Nos dice que tipo relaciones existen entre diversos objetos, ej: una formula matematica.
    * Imperativo: Nos dice como llegar a un resultado.
- Algotimos: primeros programas disennados para el cerebro humano. 

### Que es un algoritmo ?
Un algoritmo es una lista finita de instrucciones que describen un computo.

Los binarios representan instrucciones y datos.


### Grace Murray Hopper
Se da cuenta que puede escribir intrucciones usando otro programa que las traducian al lenguaje entendido por las computadora.


### Programacion
- Turing completeness: Se le conocte a todos los leguajes que utilicen todos los primitivo para realizar cualquier tipo de computo.

- Los lenguajes de programacion modernos dan primitivos que son mas convenientes que los primitivos de turing.

### Lenguajes:
- Sintaxis: Define la secuencia de simbolos que esta bien formada.
- Semantica estatica: define que enunciados con sintaxis correcta tienen significado.
- Semantica: Define el significado. En los lenguajes de programacion solo hay un significado.


# 4. Elementos basicos de python:
Tipos de lenguajes de programacion:
- Alto nivel: Se acerca mucho mas al leguaje natrual, al la forma en la que nos comunicamos nosotros.
- Bajo nivel: significa que esta optimizado para que una maquina pueda entenderlo.

* General: Tiene todos lo primitivos para poder computar cualquier tipo de algoritmos.
* Dominio especifico: Leguajes especializados 

- Interpretados: Significa que mientras corre el programa cada instruccion se traduce al lenguaje maquina.
- Compilado: Significa que nosotros convertimos antes las intrucciones a un lenguaje maquina.


### Elementos de Python
- Literales
- Operadores
- statement o enunciado

### Objetos:
Son la abstraccion mas alta dentro de cualquier lenguaje de programacion.

Forma en la que modelamos el mundo en nuestros lenguajes de programacion.

# 5. Cadenas y entradas.
- Cadenas: Secuencias de caracteres.
- Cadenas de formato 

```python
f' {"Hip " * 3} hurra '

```

### Entradas (inputs)
- Python tiene la funcion input para recibir datos del usuario del programa.
- Input siempre regresa cadenas, por lo que si queremos utilizar otro tipo, tenemos que hacer type casting.

# 6. Programas ramificados:
- Operadores de comparacion:
    * 3 == 3
- Operadores logicos:
    * and
    * or
    * not

# 7. Busqueda binaria
- Cuando la respuesta se encuentra en un conjunto ordenado, podemos utilizar busqueda binaria.

- Es altamente eficiente, pues corta el espacio de busqueda de dos por cada iteracion.


# 8. Funciones y abstraccion:
- Arguementos de Keyword y valores por defecto.

```python 
def nombre_completo(nombre,apellido,inverso=false):
    if inverso:
        return f'{apellido} {nombre}'
    else:
        return f'{nombre} {apellido}'


nombre_completo('Nelson','Cortes')
nombre_completo('Nelson','Cortes', inverso=true)
nombre_completo(apellido='Cortes',nombre='Nelson')
```
# 9. Alcance:
 

# 10. Especificaciones del codigo

# 11. Recursividad:
- Algoritmica: Una forma de crear soluciones utilizando el principio de "Divide y venceras:

- Programatica: Una tecnica programatica mediante la cual una funcion se llama a si misma.

# 12. Tuplas
- Son secuencias inmutables de objetos.
- A diferencia de las cadenas pueden contener cualquier tipo de objetos
- Puede utilizarse para devolver varios valores en una funcion.

# 13. Rangos
- Representan un secuencia de enteros.
- range(comienzo,fin,pasos)
- Al igual que las cadenas y las tuplas, los rangos son inmutables.
- Muy eficiente en uso de memoria y nomalmente utilizados en for loops.

Nota: para comprar object_equality usamos el operador is

# 14. Lista y mutabilidad
- Son secuencias de objetos, pero a diferencia de las tuplas, si son mutables.

- Cuando modificadas una lista, puede existir efectos secundarios (side effects).

- Es posible iterar con ellas.

### Clonacion
- Casi siempre es mejor clonar una lista en vez de mutarla.
- Para clonar una lista podemos utilizar rebanadas(slices) o la funcion list.

### List comprehension
- Es una forma concisa de aplicar operaciones a los valores de una secuencia.
- Tambien se pueden aplicar condiciones para filtrar.

```python 
my_list = list(range(100))
double = [i*2 for i in my_list]



pares = [i for i in my_list if i % 2 == 0]
```

# 15. Diccionarios.
- Son como listas, pero en lugar de usar indices utilizan llaves.
- No tienen orden interno.
- Los diccionarios son mutables.
- Pueden iterarse.

```python
my_dict = {
    'David': 35,
    'Erika': 25
}
```

Eliminar 


```python
my_dict = {
    'David': 35,
    'Erika': 25
}

del my_dict['David']
```


# 16. Pruebas de caja negra.
- Se basan en la especificacion de la funcion o el programa.

- Prueba inputs y valida outputs.

- Unit testing o integration testing. 


# 17. Pruebas de caja de cristal.
- Se basan en el flujo del programa.
- Prueba todos los caminos posibles de una funcion. Ramificaciones, bucles for y while, recursion.
- Regression testing o mocks. 

# 18. Debugging
- No te molestes con el debugger. aprende a utilizar el print statement.

- Estudia los datos disponibles.

- Utiliza los datos para crear hipotesisi y experimentos. Metodo cientifico.

- Ten una mente abierta. Si entendieras el programa,probablemente no habrian bugs.

- lleva un registro de lo que has tratado, preferentemente en la forma de tests.

### Disenno de experimentos.
- Debugear es un proceso de busqueda. Cada prueba debe acotar el espacio de busqueda.
- Busqueda binaria con print statements.

# 19. Manejo de excepciones.
- Son muy comunes en la programacion. No tienen nada de excepcional.

- Las excepciones de python normalmente se relacionan con errores de semantica.

- Se pueden crear excepciones propias.

- Cuando una excepcion no se maneja(unhandled exception), el programa termina con error.

- Las excepciones se manejan con los keywords:
    * try
    * Except
    * Finally

- Se pueden utilizar tambien para ramificar programas.

- No deben manejarse de manera silenciosa( por ejemplo, con print statements)

- Para aventar tu propia excepcion utiliza el keyword raise.

# 20. Afirmaciones
- Programacion defensiva.
- Pueden utilizarse para verificar que los tipos sean correctos en una funcion.
- Tambien sirven para debuguear.

```python
assert type(palabra) == str, f'{palabra} no es str'
```