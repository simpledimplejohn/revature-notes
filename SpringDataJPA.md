# Spring Data JPA
- Includes hibernate

## Create (can be added later too)
- SpringStarter Project
- Import Spring Data JPA
- import PostgresSQL Driver
- import h2 (if needed)
- import Spring Web (includes Jackson, tomcat, etc.)

## Build:
- Models
    - @Entity for class
    - @Id etc for fields
    - need the noargs constructor/no id construction/everything constructor
    - getters/setters/hashcode/equals
- DAO interface no longer have to write all the DAO stuff, just done
    - @Repository annotation
    - extends JpaRepository<Object, Integer> // the object it takes in and the primary key
        - Now it generates all crud methods
        - .save(), .delete(), .update()
    - Will be injected into the service layer to be used.
    - Can write custom sql queries with @Query
    - _Property Expression_
        - Can write custom methods, SQL statments infered on the properties.... wow
        - pretty crazy what it does here.
- Service Layer
    - @Service marked
    - `@Autowired`
      `private DAORepository daoRepo` this brings in the DAO layer
    - can now call the crud methods 
        daoRepo.save(), daoRepo.findAll(), daoRepo.deleteById() 
- Controller 
    - handles the mapping end point
    - @RestController Means it will be handling routing to the server
    - @RequestMapping("/users") endpoint it will show at this link (if you don't have its just at localhost:8080)
    - @Autowire our service class to access those methods
    - @PostMapping("/add") users/add
        - creates a post request at an endpoint
        - @RequestBody, the object comes from the Request Body of the HTTP call
    - @GetMapping("/all") users/all
        - creates a getrequest at this endpoint


- src/main/resources application.yml
    - database connection
    - can be converted into yml by right clicking
    - be sure to add to .gitignore



    