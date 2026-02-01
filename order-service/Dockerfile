# Use official Maven image for building the project
FROM maven:latest AS build

# Set working directory
WORKDIR /app

# Copy pom.xml first and download dependencies (layer caching)
COPY pom.xml .

# Download dependencies only
RUN mvn clean install -DskipTests

# Copy the rest of the source code
COPY src ./src

# Build the project
RUN mvn package -DskipTests

# Use a smaller base image to run the jar
FROM openjdk:17-jdk-slim

WORKDIR /app

# Copy the jar from the build stage
COPY --from=build /app/target/*.jar app.jar

# Expose port
EXPOSE 3000

# Run the application
ENTRYPOINT ["java", "-jar", "app.jar"]


