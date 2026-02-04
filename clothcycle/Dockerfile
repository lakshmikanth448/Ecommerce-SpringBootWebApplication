# Java 17
FROM eclipse-temurin:17-jdk

# Install Maven
RUN apt-get update && apt-get install -y maven

# Set working directory to project root
WORKDIR /Ecommerce-SpringBootWebApplication

# Copy everything from clothcycle folder
COPY . .

# Build Spring Boot app
RUN mvn clean package -DskipTests

# Expose Spring Boot port
EXPOSE 8080

# Run the generated jar
CMD ["java", "-jar", "target/*.jar"]
