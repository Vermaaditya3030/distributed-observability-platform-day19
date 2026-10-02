FROM maven:3.9.9-eclipse-temurin-17 AS build
WORKDIR /app
COPY pom.xml .
COPY metrics-service/pom.xml metrics-service/pom.xml
COPY metrics-service/src metrics-service/src
RUN mvn -pl metrics-service -am package -DskipTests
FROM eclipse-temurin:17-jre
COPY --from=build /app/metrics-service/target/metrics-service-1.0.0.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
