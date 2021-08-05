1. # Clases avanzadas

- Clases Abstractas: Nos permite hacer nuestro software mucho mas mantenible y robusto, nos permite agregar modulos futuros sin realizar tantos ajustes.
    * No implementamos todos los metodos.
    * No crearemos instancias.

Palabra **Abstract**
- En clases: Nos indica que esta clase siempre va ser heredada.
- En metodos: Metodo obligatorio de implementar. 

Nota: Con las clases abstractas podemos ver polimorfismo a nivel de clases. 

2. # Que es JavaDocs

Nos permite documentar nuestro proyecto Java.

```
/**Documentacion*/

```
```java
//Trae toda la ascendencia del metodo.
/**
*{@inheritDoc} 
*/


//Nos permite ver toda la herencia de una clase
/**
*Hereda de {@link Movie}
*@See Film
*/
```

3. # Clases anidadas y tipos
- Clases Helper
- Agrupadas por logica
- Encapsulamiento.

Clases Estaticas
```java

public class Enclosing {

    private static int x=1;

    public static class StaticNested{
        private void run(){
            //implementation
        }
    }


    @Test
    public void test(){
        Enclosing.StaticNested nested = new Enclosing.StaticNested();
        nested.run();
    }
}

```

Clases Anidadas- Inner

```java
public class Outer{
    public class Inner{

    }
}

Outer outer = new Outer();
Outer.Inner inner= outer.new Inner();
```

Clases Locales
```java
public class NewEnclosing{
    void run(){
        class Local{
            void run(){
                //Implementation
            }
        }

        new Local().run;
    }

    @Test
    public void test(){
        NewEnclosting newEnclosing = new NewEnclosing();
        newEnclosing.run();
    }
}
```


Clases Anonimas:

Son clases Abstractas.

4. # Metodos con implementacion metodos default y private. 

- DAO-Data Access Object:

Patron de disenno, Metodos CRUD(Create, Read, Update y Delete).

5. # Clases Abstractas vs Interfaces

- Interfaces
    * Se utilizan para implementar metodos que se comparten entre familias.
    * Se nombran de acuerdo a las acciones que pueden tener muchos objetos.

- Clases Abstractas
    * Se piensa en los objetos.

### Nota: 
- El disenno de nuestras aplicaciones siempre este orientado a intefaces.
- Crear buenas abstracciones.
- Encontrar el comportamiento comun.
- Declaracion de Metodos.

6. # Manejo de Errores

siempre que ocurre una excepcion se lanzara un objeto Throwable
- Throwable
    - Error: Errores causados por la maquina virtual.
    - Exception: 
        - RuntimeException:
            * Exepciones Unchecked: Exepciones inesperadas.Errores donde no sabemos que paso, ej: divison por 0. Son errores de logica.
        - IOException:
            * Exepciones Checked: Son exepciones que esperamos que sucedan.

7. # Try-catch-finally / Try-with-resources

Excepciones: Manejar excepciones significa que annadiras un bloque de codigo para manejar un error.

- Try-catch-finally: 
```java
try{

}catch(Exception name){

}catch(Exception name){

}finally{
    //Bloque de codigo que siempre se va utilizar
}


```

- Try-with-resources: Soluciona el problema de los recursos, disponible despues de java 9
```java
try(Connection connection = connectToDB()){

}catch (SQLException){
    e.printStackTrace();
}
```

8. # JDBC(Java Data Base Connectivity)

Es una API compuesta por varias clases, operiones a base de datos.

JDBC API <- Java Application -> JDBC Driver -> DataBase.

Componentes: 
- DriverManager: Nos permite crear una instancia de la conexion
-Connection: Genera la sesion, almacena el ciclo de vida de la sesion de la conexion a la BD.
- Statement: Nos permite consultar datos de una tabla sin parametros.
- PreparedStatement: Nos permite consultar datos de una tabla con parametros. 
- ResultSet: Es una interface  que nos permite manipular los datos que hemos obtenido. 


9. # Interfaces Avanzadas:
- Interfaces Funcionales: Tienen un solo metodo abstracto. (SAM(Single Abstrac method))
@FunctionalInterface (Buena practica).

10. # Programacion Funcional.
Paradigma de programacion.
 

Programacion Funcional: Se enfoca en el Que.
Programacion Imperativa: Se enfoca en Como.

Funcion de orden superior: Es aquella que recibe como parametro una funcion y nos devuelve otra funcion.

11. # Lambdas
Agregado a partir de la version 8 Java.

Forma de representar codigo.

```

(parametros) -> {cuerpo-lambdas}
```

- Fragmentos de codigo con vida corta.
- Encapsulamos codigo especifo.

12. # Lambdas como variables y recursividad:

La programacion funcional aplicado a lambdas no utiliza iteracion, se utiliza recursividad

13. # Stream y Filter

Agregados a partir de Java 8
- Stream: Un metodo que annadio a las colecciones para poder manejar lambdas.

- Filter: Condicion para filtrar

## Nota: 
En la programacion funcinal no podemos manejar asignaciones por que tenemos inmutabilidad(No podemos tener nigun tipo de asignaciones).

14. # Predicate y Consumer

- Predicate: Son expresiones que aceptan expresiones booleanas, es decir, condiciones logicas.

- Consumer: Expresion que recibe un parametro de entrada <T<T>> pero no retorna o genera ningun valor de salida. son funciones terminales.