change password in the file /home/glushenkov/IntelliJ/09_04_18_spring-security-hibernate-integration-example/src/main/resources/db.properties <br>
sql /home/glushenkov/IntelliJ/09_04_18_spring-security-hibernate-integration-example/src/main/resources/sql.sql<br>
login admin password admin@123 (String encoded=new BCryptPasswordEncoder().encode("admin@123"))

* start app $> mvn jetty:run

<br>
Another resources

//    @Secured("ROLE_CUSTOMER")
    @PreAuthorize("hasAuthority('ROLE_CUSTOMER')")

//@EnableGlobalMethodSecurity(securedEnabled = true) // to @Secured("ROLE_CUSTOMER")
@EnableGlobalMethodSecurity(securedEnabled = true) // @PreAuthorize("hasAuthority('ROLE_CUSTOMER')")
на класс с аннтоациями
@Configuration
@EnableWebSecurity
@EnableWebMvc
@ComponentScan

there are annotation + database +  roles
https://www.concretepage.com/spring/spring-security/spring-mvc-security-jdbc-authentication-example-with-custom-userdetailsservice-and-database-tables-using-java-configuration

there is a registration
http://websystique.com/springmvc/spring-mvc-4-and-spring-security-4-integration-example/

https://www.boraji.com/spring-mvc-5-spring-security-5-hibernate-5-example