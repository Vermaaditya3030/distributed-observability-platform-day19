FROM maven:3.9.9-eclipse-temurin-17 AS build
WORKDIR /app
COPY pom.xml .
COPY gateway-service/pom.xml gateway-service/pom.xml
COPY gateway-service/src gateway-service/src
RUN mvn -pl gateway-service -am package -DskipTests
FROM eclipse-temurin:17-jre
COPY --from=build /app/gateway-service/target/gateway-service-1.0.0.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
