## Requirements

For building and running the application you need:

- [JDK 21](https://www.oracle.com/java/technologies/downloads/#java21)
- [Gradle](https://docs.gradle.org/8.11.1/release-notes.html)

## Running the application locally

### Setup Docker
1. Fill information to [db.env](infra/docker/local/db.env)
2. Create and `application.properties` file look like `application-example.properties` into [resources](src/main/resources) package
3. cd to `infra/docker/local`
4. Run docker compose:
    ```shell
    docker compose up -d
    ```
5. Run application:
   * There are several ways to run a Spring Boot application on your local machine. One way is to execute the `main` method in the `ShopsaveApiApplication.java` class from your IDE.
   * Alternatively you can use the [Spring Boot Gradle plugin](https://docs.spring.io/spring-boot/gradle-plugin/running.html) like so:
    ```shell
    ./gradlew bootRun
    ```