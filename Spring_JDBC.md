# THE JDBC API

## USE THE DAO design pattern
* Models hold objects that will be filled by database calls
* DAO classes for each object, makes database calles
    - write SQL queries and make session calls for these
    * insert
    * findById
    * findByName
    * findAll
    * update
    * delete
* Service Layer: user interface methods
    * use the scanner to get the input
    * pass that to the appropriate DAO layer to make DB call
* ConnectionUtil boilerplate for making connection
    * Grabs info from application.properties
    * uses java.sql.Connection to establish a connection
* Application.properties holds db link, username, pw

