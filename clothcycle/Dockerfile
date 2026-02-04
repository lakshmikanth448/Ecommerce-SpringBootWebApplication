# Java 17 base image
FROM eclipse-temurin:17-jdk

# Install Maven
RUN apt-get update && apt-get install -y maven

# Set working directory
WORKDIR /app

# Copy project files
COPY . .

# Build the application
RUN mvn clean package -DskipTests

# Expose port
EXPOSE 8080

# Run Spring Boot jar
CMD ["java", "-jar", "target/*.jar"]
