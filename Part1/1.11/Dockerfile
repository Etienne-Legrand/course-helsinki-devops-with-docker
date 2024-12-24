FROM amazoncorretto:8
EXPOSE 8080
WORKDIR /usr/src/app
COPY . .
# Build the project
RUN ./mvnw package
# Run the project
CMD ["java", "-jar", "target/docker-example-1.1.3.jar"]