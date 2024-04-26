# Use an OpenJDK base image for Java 8
FROM openjdk:8-jdk-alpine AS builder

# Set the working directory in the container
WORKDIR /app

# Install Git and Maven
RUN apk update && apk add git maven

# Change directory to spring-boot-app
WORKDIR /app/basic-microservices-master/spring-boot-app

# Copy the source code including the pom.xml file
COPY . .

# Build the Spring Boot application with Maven
RUN mvn clean package -DskipTests

# Set the final base image for running the application
FROM openjdk:8-jre-alpine

# Set the working directory in the container
WORKDIR /app

# Copy the Spring Boot application artifact from the build stage
COPY --from=builder /app/basic-microservices-master/spring-boot-app/target/*.jar /app/app.jar

# Expose the port the Spring Boot application runs on
EXPOSE 8080

# Define the command to run the Spring Boot application when the container starts
CMD ["java", "-jar", "/app/app.jar"]
