#  How to dockerize spring-boot app
- Run docker desktop
- Create a .jar file with `mvn clean package`
- Create a Docker file called `Dockerfile` in root directory
    - `FROM openjdk:8-jdk-alpine` alpine is the light weight linux OS
    - `FROM adoptopenjdk/openjdk11:alpine-jre`
    Copy the jar file (argument 1) from within the project
    to the docker image to be run (argument 2)
    - `COPY /target/record-store-0.0.1-SNAPSHOT.jar record-store-0.0.1-SNAPSHOT.jar` 
    Now how docker runs the file with the array
    - `ENTRYPOINT ["java", "-jar", "/record-store-0.0.1-SNAPSHOT.jar"]`

- Create a .jar file with `mvn clean package` to update with docker file
- Create build dockerfile (image) -auto is the version 
    - `docker build -t recordstore:auto .` git it a name argument 1, . is argument 2
- See docker images
    `docker images`
- Remove docker images
    `docker rmi imageID`
- Build docker container -d detached mode (not verbose), exposing port 5001 to port 5001
    `sudo docker run -d -p 5001:5001 -t recordstore`
    `docker run -p 5001:5001 recordstore:auto`
- See docker containers
    `sudo docker ps`
- Stop docker containers
    `docker stop id` ideal
    `docker kill id` if you have to force, but can cause damage

