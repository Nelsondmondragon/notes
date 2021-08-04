1. # Que es Spring?
	- Posee una structura modular y flexible.
	
	- Que usaremos de Spring?
	  * Spring framework: Permite crear aplicaciones empresariales modernas.
	  * Spring Boot : Nos permite crear aplicaciones autocontenidas y autoconfigurables.
	  * Spring Data JPA : Gestiona e integra BD con nuestras aplicaciones.
	  * Spring Security : Gestionar seguridad de nuestra aplicacion.

2. # Que es una aplicacion autocontenida?
	
Pequennos servicios o aplicaciones que interactuen entre si, cada aplicacion internamente contiene su propio servidor de aplicacion.

- Spring Boot
	* Es el proyecto de spring para crear aplicaciones autocentenidas.
	* Olvidarnos de la infraestructura y centrarnos en el desarrollo.
	* Puede funcionar con Tomcat(por defecto)
	jetty o Undertow.
	* Incluye gestion de dependencias iniciales, configuracion automatica y mas.

3. # Crear nuestra aplicacion con Initializr.

	- Spring initializr?
	  * Sitio oficial para generar un proyecto de spring boot.
	  * En poco tiempo y a nuestra medida.
	  * Con todo lo que necesitamos para empezar.

	Tipo:
	 - Maven Project: Gestion de las dependencias con archivos xml

	 - Gradle Project: Los archivos gradle son escritos en gruby, me permite crear tareas que puedo ejecutar al momento de hacer despliegue o integracion continua.

4. # Hola mundo con spring Boot.

```java 
@RestController
@RequestMapping("/greet")
public class Controller {

    @GetMapping("/hello")
    public String greet() {
        return "Hello word";
    }
}
```

5. # Configurar spring boot.

- Propiedades de la aplicacion.
	* application.properties, application.tml
	o linea de comandos.

	* Posibilidad de anadir propiedades propias.

	* Gestion de perfiles segun el tipo de despliegue.

6. # Crear la estructura de los datos.

	- Dominio: 

		* DTO & objetos de dominio(Son objetos que hacen parte del contexto de nuestra aplicacion).

		* Servicios encargados de servir como puente entre los controladores de la API y la capa de persistencia.

		* Especificaciones de repositorio: interfaces que definen las reglas que debe cumplir la persistencia para intervenir entre los objetos de dominio y la BD.

		* Capa Web: Controladores de nuestra api

		* Capa de persistencia: Capa obligada a interactuar con la BD.

7. # Que es JPA?

	JPA es una especificacion de java(un estandar) para un framework ORM.

	Interactua con las tablas de la BD en forma de objetos JAVA.

	Algunas de sus implementaciones son:
	- Hibernate
	- TopLink
	- EclipseLink
	- ObjectDB


	Anotaciones de JPA
	* @Entity <- le indica a una clase java que esta representando una tabla de la BD
	* @Table <- recibe el nombre la tabla a la cual esta mapeando nuestra clase.
	* @Column <- Se le coloca a los atributos de la clase, cuando los nombres sean diferentes.
	* @Id&@Embededld(Compuesta) <- Representa la primary key de nuestra tabla en la clase.
	* @GeneratedValue <- Generar automaticamente valores de la primary key en nuestras clases
	* @OneToMany&@ManyToOne <- Representar las relaciones 

8. # Conocer spring data.

	Spring data es un proyecto que usa JPA para que la gestion de tareas desde JAVA 
	en las BD sea mas podera y llena de posibilidades.

	* Es un proyecto que internamente contiene otros, nosotros usaremos el spring Data JPA.

	* Optimizacion de tareas repetitivas.

	* Repositorios sin condigo con JPARepository, CrudRepository & PagingAndSortingRepository

	* Auditorias Transparentes. 

9. # CONECTAR BD A NUESTRA APLICACION

20. # MAPEAR LAS TABLAS COMO CLASES

21. # CREAR ENTITY CUANDO SU CLAVE PRIMARIA ES COMPUESTA.
 
22. # MAPEAR RELACIONES ENTRE CLASES.

23. # USAR LA INTERFACE CRUDREPOSITORY

	- Spring Data Repository

	  * Ahorran un monton de codigo y tiempo de implementacion.
	  * Operaciones SIN CODIGO en la BD
	  * Repository de Spring Data
		1. CrudRepository <- Nos permite realizar las operaciones basicas.
		2. PaginAndSortingRepository. <- Nos permite hacer lo mismo del CrudRepository y adicionalmente nos permite tareas de paginacion y ordenamiento.
		3. JPARepository <- Los mismo de CrudRepository y PaginAndSortingRepository, mas tareas especificas, como guardar o cambinar todo en memorias sin que otra entidades o entornos vean esos cambios en la BD.


14. # QUERY METHODS 

	- Uso de query Methods
	  * En ocasiones, necesitamos consultas que el repository de spring Data no nos puede ofrecer

	  * Los query Methods proveen la posibilidad de generar consultas mediante el nombre de los metodos.

	  * Tienen la posibilidad de retornar Optional<T>

	#### QUERY METHODS
```java
	findByIdCategoriaOrderByNombreAsc(int idCategoria)
```
	Tambien podemos usarlos de forma nativa con @Query
	ejemplo: 
```java
@Query(value = "SELECT * FROM productos WHERE id_categoria = ?", nativeQuery = true)
```

15. # QUE ES EL PATRON DATA MAPPER Y QUE RESUELVE?

	Consiste en convertir o traducir dos objetos que pueden hacer una misma labor

	 - Y esto en que nos ayuda?
		 * No exponer la BD en el API.
		 * Desacoplar nuestra API a una BD puntual.
		 * No tener campos innecesarios en el API.
		 * Sin mezclar idiomas en el dominio.

 #### NOTA: proyecto enfocado al dominio.

 #### En que nos ayudan los objetos de dominio?

	* No exponer la BD en el API.
	* Desacoplar nuestra API a una BD puntual.
	* No tener campos innecesarios en el API.
	* Sin mezclar idiomas en el dominio

16. # ORIENTAR NUESTRA API AL DOMINIO CON MAPSTRUCT

	- @Mapper <-le idicamos a nuestra clase que es una mapeadora.

	- @Mappings <- Indicamos como queremos traducir nuestros objetos con una lista de mapping.
		- @Mapping <- Inidcamos el origen y el destino.

17. # ORIENTAR NUESTRO REPOSITORIO A TERMINOS DEL DOMINIO.

	Con esto logramos que nuestros objetos queden enfocados al dominio y no a una tabla puntual

18. # INYECCION DE DEPENDENCIAS.

	* Principios S.O.L.I.D
	
	* Inyeccion de dependencias(DI) Consiste en pasar la dependencia a la clase que lo va utilizar, en lugar de crearla,con el fin de no acoplar la clase a la implementacion que esta utilizando.

	* Inversion de control(loC). Se refiere a que es un framework quien toma el control de los objetos, en este caso spring.
	Spring contiene un contenedor de IoC, el cual se encarga de administrar objetos que se conocen como Beans o component, Spring utiliza la anotacion @Autowired para hacer inyeccion de dependencias.
	
	* Spring y @Autowired

19. # IMPLEMENTAR LA ANOTACION @SERVICE

20. # IMPLEMENTAR LA ANOTACION @RESTCONTROLLER

	- @RestController <- Le indica a spring que esta clase va ser un controlador de una API rest
	
	- @RequestMapping("") <- En el parametro va que path va aceptar la peticiones que le hagamos

EJ: 
```java
@RestController
@RequestMapping("/products")
public class ProductDController {
///
}
```

21. # Exponer nuestra API

#### Que anotaciones usaremos.

- Nuestra API se expone por @RestController.

- Los metodos se exponene con @GetMapping (Obtener Info.), @PostMapping(Guardar o Obtener info.) o @DeleteMapping (Eleminar Info.)


22. # Controlar las respuestas HTTP.

### ResponseEntity

- Que es y en que nos ayuda?

- HttpStatus.

23. # Crear el dominio de compras.

```java
@Data
public class PurchaseDto {

    private int idPurchaseDto;
    private String idClientDto;
    private LocalDateTime dateDto;
    private String paymentMethodDto;
    private String commentDto;
    private String stateDto;
    private List<PurchaseDtoItem> items;

}

@Data
public class PurchaseDtoItem {
    private int productIdDto;
    private int quantity;
    private  double total;
    private boolean active;
}

public interface PurchaseRepository {
    List<PurchaseDto> getAll();
    Optional<List<PurchaseDto>> getByClient(String idClient);
    PurchaseDto save(PurchaseDto purchaseDto);
}

```


24. # Mapear el dominio de compras.
```java
@Mapper(componentModel = "spring", uses = {PurchaseDtoItemMapper.class})
public interface PurchaseDtoMapper {

    @Mappings({
            @Mapping(source = "idPurchase",target = "idPurchaseDto"),
            @Mapping(source = "idClient",target = "idClientDto"),
            @Mapping(source = "date",target = "dateDto"),
            @Mapping(source = "paymentMethod",target = "paymentMethodDto"),
            @Mapping(source = "commentary",target = "commentDto"),
            @Mapping(source = "status",target = "stateDto"),
            @Mapping(source = "products",target = "items")
    })
    PurchaseDto toPurchaseDto(Purchase purchase);
    List<PurchaseDto> toPurchaseDtos(List<Purchase> purchases);

    @InheritInverseConfiguration
    @Mapping(target = "client",ignore = true)
    Purchase toPurchase(PurchaseDto purchaseDto);
}
```


25. # Crear el repositorio de compras.


```java
@Repository
public class PurchaseRepositoryP implements PurchaseRepository {

    private PurchaseCrudRepository purchaseCrudRepository;
    private PurchaseDtoMapper mapper;

    @Override
    public List<PurchaseDto> getAll() {
        return mapper.toPurchaseDtos((List<Purchase>) purchaseCrudRepository.findAll());
    }

    @Override
    public Optional<List<PurchaseDto>> getByClient(String idClient) {
        return purchaseCrudRepository.findByIdClient(idClient)
                .map(purchases -> mapper.toPurchaseDtos(purchases));
    }

    @Override
    public PurchaseDto save(PurchaseDto purchaseDto) {
        Purchase purchase= mapper.toPurchase(purchaseDto);
        purchase.getProducts().forEach(purchaseProduct -> purchaseProduct.setPurchase(purchase));
        return mapper.toPurchaseDto(purchaseCrudRepository.save(purchase));
    }
```


26. # Probando nuestros servicios de Compras.

Los error mas comunes se presentan en los objetos dto y el mapeo de las tablas.


27. # Documentar nuestra API con Swagger.

#### Dependencias 
```
//swagger2 -> Documentamos 
implementation 'io.springfox:springfox-swagger2:2.9.2'

//swagger ui -> nos permite ver la documentacion en una pagina. 
implementation 'io.springfox:springfox-swagger-ui:2.9.2'
```
#### Por que documentar nuestra API?

- Le agregamos una capa de entendimiento.
- Es mas facil de usar.
- Es mas profesional.
- Quien consuma tendra informacion oficial y de primera mano.

28. # Configurando la seguridad de nuestra API con spring Security.

- Spring Security

	* Autenticacion y autorizacion para aplicaciones de spring.
	* Como todos los proyectos de spring, es muy facil de configurar.
	* Proteccion ante ataques como session Fixation, clickJacking, cross site request forgery, entre otros. 
	* Configuracion por defecto. 

```java
@Service
public class PlatziUserDetailsService implements UserDetailsService {


    @Override
    public UserDetails loadUserByUsername(String username) throws UsernameNotFoundException {
        return new User("nedacort", "{noop}platzi", new ArrayList<>());
    }
}



@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {

    @Autowired
    private PlatziUserDetailsService platziUserDetailsService;

    @Override
    protected void configure(AuthenticationManagerBuilder auth) throws Exception {
        auth.userDetailsService(platziUserDetailsService);
    }
}

```

29. # Generar un JWT(JSON web Token)

- Que es un JWT: Nos permite controlar las peticiones que recibe nuestra aplicacion.

	* Estandar de codigo abierto basado en JSON para crear tokens de seguridad.

	* La autenticacion viaja en el header de la peticion. 

	```
	Authorization : Bearer <token>
	```

### Como funciona un JWT
Un JWT esta dividido en 3 secciones:
1. Header : Algoritmo y tipo de token que se esta generando.
2. Payload : Toda la informacion del token.
3. Signature : Es la firma y agarra los dos anteriores y los encripta segun el algoritmo seleccionado.


dependencia: 
```
implementation 'io.jsonwebtoken:jjwt:0.9.1'
```

Metodo para generar el token de seguridad con JWT, creacion de dtos para ayudar con en el momento de crear el controlador, para la
autenticacion de la app

```java 
public class JWTUtil {
    private static final String KEY = "pl4tz1";

    public String generateToken(UserDetails userDetails) {

        return Jwts.builder().setSubject(userDetails.getUsername()).setIssuedAt(new Date())
                .setExpiration(new Date(System.currentTimeMillis() + 1000 * 60 * 60 * 10))
                .signWith(SignatureAlgorithm.HS256, KEY).compact();
    }
}


@Data
public class AuthenticationRequest {
    private String username;
    private String password;
}

@Data
public class AuthenticationResponse {
    private String jwt;

    public AuthenticationResponse(String jwt) {
        this.jwt = jwt;
    }

}
```

30. # Desplegar nuestra API desde la ventana de comandos.

Para desplegarla con el terminal de nuestro pc vamos a llamar a la tarea:

```
java -jar platzi-market-1.0.jar
```

Algunas propiedades adicionales antes de adjutar el jar

- -Xmx2048m
- -Dspring.profiles.active=pdn
- -Dserver.port=88

Antes de desplegar la aplicacion debemos:

- Cambiar **version = '0.0.1-SNAPSHOT'** por **version= 1.0**


Nos ubicamos en la carpeta de nuestro proyecto y ejecutamos el siguiente programa.

```
java -jar build/libs/platzi-market-1.0.jar
```

Para cambiar el perfil se hace de la siguiente forma.

```
java -jar "-Dspring.profiles.active=pdn" build/libs/platzi-market-1.0.jar
```

31. # Desplegar nuestra BD con heroku