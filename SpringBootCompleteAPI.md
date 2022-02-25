# Building a complete API in Spring Boot

## Main annotation
- @SpringBootApplication 
    - @CommopnentScan - scanns the components for autowiring
    - @Configuration - 
    - @EnableAutoConfiguration

## Setup
- Sprint Starter Project
    - Group com.revature
    - Artifcfact CompleteAPI
    - Package com.revature
- Import the following dependencies:
    - Spring Data JPA
    - H2 Database
    - Spring Web
    - PostgreSQL
    ?    - Lombok
    - Spring Boot Actuator //tells us what's happening in the app 
    - Spring Boot DevTools // real time changes on a running application
- Manually add Lombok with the following pom.xml tags
```
		<dependency>
			<groupId>org.projectlombok</groupId>
			<artifactId>lombok</artifactId>
			<optional>true</optional>
		</dependency>

        <plugin>
				<configuration>
					<excludes>
						<exclude>
							<groupId>org.projectlombok</groupId>
							<artifactId>lombok</artifactId>
						</exclude>
					</excludes>
				</configuration>
			</plugin>
```
- Add a dependcy after initialization
    - right click on pom.xml
    - go to Spring - Edit Starters
    - add something like validation

## About UserController
- GetMapping/PostMapping automatically set up the HttpRequest headers/body/etc most of the time
    - ResponseEntity allows you to manually set these and is useful sometimes
    ```
    @GetMapping("/{id}")
    public ResponseEntity<User> findUserById(@PathVariable("id") int id) {
        return ResponseEntity.ok(userServ.getById(id));
    }
    ```

## Run Spring Boot Maven from the command line
- `mvn clean package`
- `mvn spring-boot:run`


