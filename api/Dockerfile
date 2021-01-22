FROM openjdk:11

WORKDIR /usr/src/app

ADD . .
RUN apt-get update
RUN ./mvnw clean package -Dquarkus.package.type=uber-jar -DskipTests

CMD ["java" ,"-jar", "target/tlcdemoApp-1.0.0-SNAPSHOT-runner.jar"]