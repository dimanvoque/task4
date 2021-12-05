FROM openjdk:8-jdk-alpine

WORKDIR /app
COPY . .
RUN cd target

CMD ["java", "-jar", "dostavimvse-0.0.1-SNAPSHOT.jar"]
