

FROM eclipse-temurin:17-jdk

RUN apt-get update && apt-get install -y maven

WORKDIR /

COPY clothcycle/pom.xml .
COPY clothcycle/src .clothcycle/src

RUN mvn clean package -DskipTests

FROM eclipse-temurin:17-jdk
WORKDIR /

EXPOSE 8080

CMD ["java", "-jar", "target/clothcycle-0.0.1-SNAPSHOT.jar"]

