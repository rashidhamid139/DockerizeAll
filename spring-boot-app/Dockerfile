FROM openjdk:8-jre-alpine
#APK command
RUN apk add --no-cache bash

#Copy war into Image
COPY target/spring-boot-app-0.0.1-SNAPSHOT.war /app.war
#COPY LOGS
COPY run.sh /run.sh
COPY logback.xml /logback.xml
#run application with this command
CMD ["/usr/bin/java", "-jar", "-Dspring.profiles.active=default", "-Dlogging.config=/logback.xml",  "/app.war"]
##RUN Entry Command
ENTRYPOINT [ "sh", "run.sh" ]