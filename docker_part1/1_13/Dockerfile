FROM openjdk:8

WORKDIR /mydir
RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/docker-hy/spring-example-project .
RUN ./mvnw package

EXPOSE 8080
CMD [ "java", "-jar", "./target/docker-example-1.1.3.jar" ]