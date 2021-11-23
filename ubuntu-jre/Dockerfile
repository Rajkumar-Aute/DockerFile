FROM ubuntu
RUN apt update
RUN apt install openjdk-8-jdk wget -y
RUN wget https://rajshared.s3.amazonaws.com/spring-petclinic.jar
EXPOSE 8080
CMD ["java", "-jar", "spring-petclinic.jar"]