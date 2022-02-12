# How to set up a spring boot with SonarCloud

## Things We need to do
- Create a git repository
- Init git repo for project and push
- Login to SonarCloud with github
- authorize github 
- Create an orgianzation  key = simpledimplejohn-github
- Security token token = "ghdfjsklfhdsajklfd"

- mvn clean sonar:sonar =Dsonar.host.url=https://sonarcloud.io -Dsonar.orginaztion=simpledimplejohn-github -Dsonar.login-ghdfjsklfhdsajklfd

- if build sucuess can now view on url
