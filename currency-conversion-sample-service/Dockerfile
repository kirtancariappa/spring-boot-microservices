# Use Maven to build the application
FROM maven:3.8.6-eclipse-temurin-17 AS build
WORKDIR /app
COPY . .
RUN mvn clean package -DskipTests

# Use a lightweight JDK image to run the app
FROM eclipse-temurin:17-jdk-alpine
WORKDIR /app

# Copy the built JAR from the Maven image
COPY --from=build /app/target/*.jar app.jar

# Run the application
ENTRYPOINT ["java", "-jar", "app.jar"]
