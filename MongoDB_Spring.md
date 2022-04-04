# How To Setup MongoDB with Spring-Boot basic
 -    [tutorial](https://www.youtube.com/watch?v=k5PeywcbVYc)
 -    [github](https://github.com/simpledimplejohn/spring-mongodb-test)

## Running locally on your machine
 - launch MongoDB in the terminal with `sudo mongod --dbpath /System/Volumes/Data/data/db`
 - run the app called Compass

## Things to add in Spring Boot
 - On project setup use `Spring Data MongoDB` dependency
 - Repository `public interface UserRepository extends MongoRepository<User, Integer>`
 - Model Class instead of,, use `@Document(collection="user")` Mongo uses Documents instead of Tables
 - Controller no change
 

## Application Properties
- spring.data.mongodb.host=localhost
- spring.data.mongodb.port=27017
- spring.data.mongodb.database=Third

