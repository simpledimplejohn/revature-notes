# Docer EC2 Notes

### Launch EC2
* login to aws go to EC2
* orange button launch instance
* Chose an AMI use Free Linux Kernel 5.10 to choice 64 bit x86
* Choose instance type (free tier) (click next configure instance details)
* nothing under Configure Instance (next)
* nothing for add storage (next)
* nothing for add tags (next)
* Configure Security Group (create a new security group) //control who has access to EC2
  * add rule, custom TCP, Port: 8080, description: Tomcat Port
  * add rule, HTTP, port 80, description: To connect to web app
  * add rule, Custom TCP, port: 5432, Source Anywhere, description: postgresql
  * REVIEW AND LAUNCH
* Double check that its free tier before launching, click LAUNCH button
* Create a new key pair, name it something "project2-key-pair" and download key pair then LAUNCH
    Free tier is 750 hours of free usage
* Click Ciew Instance to see instance running

### Setting up EC2
* Go to instances in AWS consolue
* click on Instance ID
* Click CONNECT button
* To Connect in Browser select EC2 Instance Connect (do not change username) click CONNECT
  * Now have access using Linux 
  * for fun run: `sudo yum install cowsay -y`, `cowsay hello world`
  * Install Java `sudo yum install java-1.8.0-openjdk-devel -y` -y means yes to all
  * Install Maven `sudo yum install maven -y`
  * Install Git `sudo yum install git -y`
  * Install Tomcat `sudo amazon-linux-extras install tomcat8.5 -y`

### Open EC2 with PEM Key
* Click instance and click connect
* open folder with pem key-pair.pem file in it
* run commands for specific EC2 instance in Connect to instance SSH client
  - _mac_: run: `chmod 400 project2-key-pair.pem` enter whatever your key-pair name is
  * run: `ssh -i "project-2-new-keypair.pem" ec2-user@ec2-3-138-136-240.us-east-2.compute.amazonaws.com` whatever is listed as your SSH client example
  * To exit type `exit`

### Running Spring Boot API
* Create a folder and CD into it
* Clone Repo into this folder
* CD into source folder
* run `mvn clean package` to build
* `java -jar target/NiceDay-0.0.1-SNAPSHOT.jar` whatever the jar file name is goes after target


### Running a War webapp
* `sudo cp target/PROJECT_NAME.war /var/lib/tomcat/webapps`
* copy the public IP address from the EC2 instance 

### Running docker and an app in docker
* `docker build -t nameOfImage:auto`
* `docker run -p port:port nameOfImage:auto`
* port 9192??
