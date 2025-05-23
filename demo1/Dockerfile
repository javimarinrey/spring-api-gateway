FROM maven:3.9-eclipse-temurin-21 AS build
WORKDIR /apps
COPY . .
RUN mvn clean package -DskipTests

FROM eclipse-temurin:21-jre
WORKDIR /apps
COPY --from=build /apps/target/demo1.jar demo1.jar
ENTRYPOINT ["java", "-Dspring.profiles.active=prod", "-jar", "demo1.jar"]