FROM openjdk:8-jdk-slim

WORKDIR /usr/src/app

COPY . .

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
#CMD java -jar ./target/docker-example-1.1.3.jar

# docker build -t spring .

# docker run -it -p 8080:8080 spring