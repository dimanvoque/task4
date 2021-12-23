FROM maven:3-jdk-8-alpine

WORKDIR /dostavimvse

COPY . .

RUN mvn install -Dstart-class=Main
RUN cp target/dostavimvse-0.0.1-SNAPSHOT.jar Main.jar

RUN mvn clean install -Dstart-class=ru.fivt.dostavimvse.DostavimvseApplication
RUN cp target/dostavimvse-0.0.1-SNAPSHOT.jar DostavimvseApplication.jar

ENTRYPOINT java -jar Main.jar & java -jar DostavimvseApplication.jar
