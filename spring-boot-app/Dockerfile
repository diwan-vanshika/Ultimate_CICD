# Use JDK 17 as the base image
FROM eclipse-temurin:17-jre
RUN apt-get update && apt-get install -y docker.io

# Simplify the artifact path
ARG artifact=target/spring-boot-web.jar

# Set the working directory
WORKDIR /opt/app

# Copy the artifact to the container
COPY ${artifact} app.jar

# Set the entry point to run the application
ENTRYPOINT ["java","-jar","app.jar"]
