# base image
FROM openjdk:8
# variables
ENV apppath="/spring-petclinic.jar"
ARG downloadpath="https://rajshared.s3.amazonaws.com/spring-petclinic.jar"
# download the jar file
ADD ${downloadpath} ${apppath}
# open 8080 port
EXPOSE 8080
# commend to run container
CMD java -jar ${apppath}