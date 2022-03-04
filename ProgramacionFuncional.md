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
Es algo dentro del leguaje que es usable y operable.

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
- So funciones anonimas.

### Funcion:  
- Tiene nombre

### Lambda: 
- No tiene nombre. 

### Por que usarlas?
- Es un compartamiento de uso unico.
- Una regla que solo se requiere en un lugar.
- Es una funcion extremadamente simple.