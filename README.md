# Java-SpringBoot-BookStore
Full Stack: React and Java Spring Boot with MySQL Database Project

Crete React Front End components

Retrieve data from Spring Boot REST APIs



Spring Boot
    Developed a Full stack project with React and Spring Boot
    Leveraged the Hibernate API to connect with MySQL
    Developed REST APIs with Spring Data REST
    Developed custom queries using the Spring Data JPA    
    Accelerated the development process with Spring Data REST
    Applied pagination and sorting to REST API endpoints
    Secured the Spring Boot REST API using OIDC and JWT


在Spring Boot中编写API可以通过创建RESTful服务来实现
1.Controller类来处理。创建一个新的Controller类，使用@RestController注解标记它，这表明这个类将处理HTTP请求并返回JSON或XML响应。
2.定义API方法：在Controller类中，你可以定义各种API方法，这些方法将响应不同的HTTP请求。你可以使用@GetMapping、@PostMapping、@PutMapping、@DeleteMapping等注解来定义API端点，以及@RequestBody和@RequestParam等注解来接收请求参数
3.业务逻辑：在API方法中，编写业务逻辑，包括数据检索、更新、创建等操作。你可以使用Spring Data JPA来访问数据库、使用其他服务或资源等。

请求从Controller开始，Controller将请求传递给Service层，Service层使用DAO访问数据库，然后将结果映射为Response Models返回给Controller。Controller使用Response Models构建HTTP响应，将响应返回给客户端。 Request Models用于接收和验证客户端请求中的数据。
-  Entity：实体类通常是与数据库表相关的Java类，它们代表了数据模型的结构。Entity类通常使用JPA注解（如@Entity，@Table，@Column等）来映射到数据库表。它们是数据的持久性表示。
-  DAO（Data Access Object）：DAO类通常用于与数据库交互。它们包括了数据库操作的方法，如查询、插入、更新和删除。DAO类通常使用Spring Data JPA或Hibernate等ORM框架来简化数据库操作。
-  Request Models：请求模型或DTO（Data Transfer Object）是用于接收客户端请求的数据模型。它们通常是普通的Java类，用于从HTTP请求中提取数据。Request Models有助于验证和处理客户端传递的数据。
-  Response Models：响应模型也是数据模型，但它们用于构建API端点的响应。它们定义了API返回给客户端的数据结构。通常，Response Models是Entity类的精简版本，只包括需要的字段。
-  Service：Service类包含业务逻辑，它们用于处理Controller层的请求。Service类调用DAO类来访问数据库，执行数据操作，并将结果映射为Response Models。Service类处理业务规则、事务管理和其他业务逻辑。
-  Controller：Controller类用于处理HTTP请求和构建HTTP响应。它们接收请求参数（通过Request Models），将请求传递给Service层，并将Service层返回的数据映射为Response Models。Controller类通常包含API端点的路由定义（使用@RequestMapping等注解），并处理HTTP请求的验证和身份验证。
