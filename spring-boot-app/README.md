# Building and running the application

## Option 1
``mvn clean install``\
``mvn spring-boot:run``

## Option 2
``mvn package spring-boot:repackage``\
``java -Dspring.profiles.active=default -jar target/spring-boot-app-0.0.1-SNAPSHOT.war``

# Accessing the application
http://localhost:8081/springbootapp/employees



# Build Image from Dockerfile
sudo docker build --tag=spring-boot-app .

# Get image list
sudo docker image ls

# Build a container from image with tag name
sudo docker run -d -p 8081:8081 spring-boot-app

# Get all running containers list
sudo docker ps


# Stop a container using its container ID
sudo docker stop <container_id>