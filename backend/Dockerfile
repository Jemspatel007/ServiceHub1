# Use an official OpenJDK runtime as the base image
FROM openjdk:17-oracle

RUN pwd && ls

# Set the working directory inside the container
WORKDIR /app

RUN pwd && ls

# Copy the compiled JAR file from your target directory into the container
COPY target/ServiceHub-0.0.1-SNAPSHOT.jar /app/app.jar

# Exposing the port on which banckend application will run
EXPOSE 8080

# Set the active Spring Boot profile to "production"
ENV SPRING_PROFILES_ACTIVE=production

# Command to run your Spring Boot application when the container starts
ENTRYPOINT ["java", "-jar", "app.jar"]
