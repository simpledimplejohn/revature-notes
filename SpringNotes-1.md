# Spring Notes

## Starting a spring project
- file/new/spring starter project
    - Java 8, Maven, Jar
    - Pakcage is where the main method goes
    - boot version 2.6.
# Reflection
- spring is using reflection to scan for all these anotations

# Annotations General
- @Bean
Bellow are types of @Componennts: 
- @Repository
    - The DAO data layer
    - a class/interfaces that will be doing database calls
- @Service
    - Calls the DAO layer
    - Will need a DAO object, does this with @Autowired
    - Handels buisness logic
- @Controller
    - handles the web
    - @RestController is what is used which is a @Controller



# Aspects 
- @Aspect on the class
- @Configuration //also needed on the class
- Advice plus pointcut = Aspect ???????
- intercepts a method from a specific class
- point-cut, what we are doing when we grab that method
- These annotations are called _ADVICE_
- @Before("what classes this applies to") 
    - does something before the method is run
    - JoinPoint is what we are doing with it
- @After("what classes this applies to")
    - does something after the method has been run
    - JoinPoint is what we are intercepting
- @AfterReturning(value="where", returning="result")
    - can get the value of the method
- @AfterThrowing()
    - what to do after an exception has been thrown
- @Around("what class, what method")
    - can handle before and after method execution



