FROM maven:3.9-eclipse-temurin-21 AS build
WORKDIR /apps
COPY . .
RUN mvn clean package -DskipTests

FROM eclipse-temurin:21-jre
WORKDIR /apps
COPY --from=build /apps/target/gateway.jar gateway.jar
ENTRYPOINT ["java", "-jar", "gateway.jar"]