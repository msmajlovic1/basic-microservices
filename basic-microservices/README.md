Docker Compose for Node.js and Spring Boot Applications

This docker-compose.yml file enables running Node.js and Spring Boot applications within Docker containers. The containers are launched as separate services and communicate via the defined Docker network.


Set up Application Directories:
Place your Node.js application code in the ./node-app directory.
Place your Spring Boot application code (including the app.jar file) in the ./springboot-app directory.
Check Environment Configuration:
Ensure that the .env file is correctly configured for your environment. Adjust the variables such as ports, database credentials, or any other environment-specific settings as needed.
Run Docker Compose:

docker-compose up

Verify Application Startup:
The Node.js application will be accessible at http://localhost:8081.
The Spring Boot application will be accessible at http://localhost:8080.
