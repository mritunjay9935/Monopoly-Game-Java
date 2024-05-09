Here is the updated `Readme.md` file with the points you provided:

```markdown
# Java-based Monopoly Game Application

This is a Java-based Monopoly game application built with Spring Boot and Maven.

## Project Structure

* `src/main/java/com/example/game` - Contains the main application file `GameApplication.java` which is the entry point of the application. It is annotated with `@SpringBootApplication` and `@EnableJpaAuditing` to enable JPA auditing.

* `src/main/java/com/example/game/entities` - Contains the `BaseEntity.java` which is a base class for all entities in the application. It includes fields like `id`, `createdAt`, `lockId`, and `modifiedAt`. It uses JPA annotations for ORM mapping and Lombok for reducing boilerplate code.

* `src/main/java/com/example/game/exceptions` - Contains custom exception classes like `NoHostException.java` which is a runtime exception thrown when no host is found.

* `src/main/java/com/example/game/handlers` - Contains exception handler classes like `ApplicationExceptionHandler.java`. This class extends `ResponseEntityExceptionHandler` and provides methods to handle various exceptions like `NoHostException`, `UserNotFoundException`, `InvalidMoveException`, and `NoActiveGameException`.

## Database Setup

Before running the application, you need to set up a PostgreSQL database.

1. Install PostgreSQL: You can download it from the official [PostgreSQL website](https://www.postgresql.org/download/). Follow the instructions based on your operating system.

2. Create a Database: After installing PostgreSQL, open the SQL shell (psql) or use a GUI tool like pgAdmin to create a new database. Run the following command to create a new database named `monopoly`:

   ```sql
   CREATE DATABASE monopoly;
   ```

3. Update application properties: In the `src/main/resources/application.properties` file, update the following properties with your PostgreSQL credentials and the newly created database name:

   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/monopoly
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   ```

## Setup

To run this project, you will need to have Java and Maven installed.

1. Clone the repository
2. Navigate to the project directory
3. Run `mvn clean install` to build the project
4. Run `mvn spring-boot:run` to start the application

## Game Application Usage Guide

1. Installation:
    - Ensure you have Java and Maven installed on your system.
    - Clone the repository to your local system.
    - Navigate to the project directory.
    - Run `mvn clean install` to build the project.
    - Run `mvn spring-boot:run` to start the application.

2. Features:
    - Game Management: The application allows you to create, manage, and play games. The main entry point of the application is `GameApplication.java`.
    - Entity Management: The application uses `BaseEntity.java` as a base class for all entities in the application. It includes fields like `id`, `createdAt`, `lockId`, and `modifiedAt`.
    - Exception Handling: The application has custom exception classes like `NoHostException.java`, `UserNotFoundException.java`, `InvalidMoveException.java`, and `NoActiveGameException.java` to handle various scenarios during the game play.
    - Exception Handlers: The application uses `ApplicationExceptionHandler.java` to handle the exceptions thrown during the game play.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

Please replace `your_username` and `your_password` with your actual PostgreSQL username and password.
```