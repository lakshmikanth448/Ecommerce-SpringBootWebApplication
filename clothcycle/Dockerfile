# Use Java 17 (recommended for Spring Boot)
FROM eclipse-temurin:17-jdk

# Set working directory inside container
WORKDIR /app

# Copy all project files into container
COPY . .

# Build the Spring Boot application
RUN ./mvnw clean package -DskipTests

# Expose Spring Boot default port
EXPOSE 8080

# Run the generated JAR file
CMD ["java", "-jar", "target/*.jar"]
