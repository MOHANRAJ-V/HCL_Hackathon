FROM eclipse-temurin:8-jdk-ubi10-minimal

WORKDIR /app

# Copy jar built by Jenkins pipeline
COPY target/*.jar app.jar

EXPOSE 3000
ENTRYPOINT ["java", "-jar", "app.jar"]
