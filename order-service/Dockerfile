FROM openjdk:17-jdk-slim

WORKDIR /app

# Copy jar built by Jenkins pipeline
COPY target/*.jar app.jar

EXPOSE 3000
ENTRYPOINT ["java", "-jar", "app.jar"]
