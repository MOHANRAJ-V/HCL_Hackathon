FROM openjdk:27-ea-jdk-slim

WORKDIR /app

# Copy jar built by Jenkins pipeline
COPY target/*.jar app.jar

EXPOSE 8081
ENTRYPOINT ["java", "-jar", "app.jar"]
