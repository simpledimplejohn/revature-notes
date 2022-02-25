#  How to dockerize spring-boot app
- Run docker desktop
- Create a .jar file with `mvn clean package`
- Create a Docker file called `Dockerfile` in root directory
    - `FROM openjdk:11-jdk-alpine` alpine is the light weight linux OS
    Copy the jar file (argument 1) from within the project
    to the docker image to be run (argument 2)
    - `COPY /target/record-store-0.0.1-SNAPSHOT.jar record-store-0.0.1-SNAPSHOT.jar` 
    Now how docker runs the file with the array
    - `ENTRYPOINT ["java", "-jar", "/record-store-0.0.1-SNAPSHOT.jar"]`

- Create a .jar file with `mvn clean package` to update with docker file
- Build the docker file
    - `docker build -t recordstore:auto .` git it a name argument 1, . is argument 2
    