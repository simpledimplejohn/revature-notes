# Swagger
## Swagger can bet set up to give more information about your api

# Setup only works for Spring Boot version 2.5.5

- Pom.xml setup
    boot version
    <version>2.5.5<</version>
    <dependency>
        <groupId>io.springfox</groupId>
        <artifactId>springfox-boot-starter</artifactId>
    <version>3.0.0</version>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-configuration-processor</artifactId>
        <optional>true</optional>
    </dependency>
- Files needed: 
    - com.revature.config package
        - SwaggerConfig.java includes a @configuration and @bean
    - com.revature.controller
        - RootController.java 
            @GetMapping("/docs") // where the swagger info can be found
            boilerplate code see example
- Using Swagger
    - Run application
    - navigate to: `http://localhost:5001/api/swagger-ui/index.html`

## Actuator added with initial springboot setup 
    - 	<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-actuator</artifactId>
		</dependency>
    - got to path `http://localhost:5001/api/actuator`
        - gives a health check on the app to see if it is running

## Using the h2 database
    - Configure in application.properties file using boilerplate
    - navigate to `http://localhost:5001/api/h2-console`
    - login, only exists while app is running, resets eachtime app is shut down

## Controller advice to intercept errors
    - 