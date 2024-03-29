# Cinema app <img src="https://github.com/mrmax24/cinema-app/blob/main/film-tape.gif" style="border-radius:8px;" align="center" width=65px>
## Project description:
```bash
A simple web-application that supports authentication, registration and basic features of the ticket 
reservation service, based on Hibernate and Spring frameworks using REST common principles.
```


## Features:
- register and log in as a user/administrator; 
#### Registered as USER role:
- find movies and cinema halls
- find available movie sessions
- create shopping cart
- add tickets to shopping cart
- view shopping cart
- make an order
- view order history
#### Registered as ADMIN role:
- create and find movies and cinema halls
- create and find available movie sessions
- find user by email

## Project structure

The project has a Three-Tier Architecture:
- **Presentation layer** (Controllers) - accepts requests from clients and sends results back to them.
- **Application logic** layer (Service), provide logic to operate on the data sent to and from the DAO and the client.
- **Data access layer** (DAO), represents a bridge between the database and the application.

## Used technologies and libraries:
| Technology               | Version  |
|:-------------------------|:---------|
| `JDK`                    | `17`     |
| `Maven`                  | `4.0.0`  |
| `Hibernate`              | `5.6.14` |
| `Hibernate validator`    | `6.1.6`  |
| `Spring Framework`       | `5.3.20` |
| `Spring Web MVC`         | `-`      |
| `Spring Security`        | `5.6.10` |
| `Apache Tomcat`          | `9.0.50` |
| `Javax Servlet`          | `4.0.1`  |
| `Javax Annotation`       | `1.0`    |
| `JSON`                   | `-`    |
| `Jackson`                | `2.14.1` |
| `MySQL`               | `8.0.28` |
| `Checkstyle`          | `3.1.1`  |

## Technical details
- **Entities** represent columns in the database;
- **DTOs** represent communication between Presentation and Service layers;
- **DTO mappers** convert DTOs to entities and vice versa
- **BCryptPasswordEncoder** is used for password encryption
- **Hibernate annotations** are used for field validation
- **Custom annotations** are used for email and password validation
- **Jackson API** is responsible for converting objects to **JSON**
- **Config package** contains classes allow to configure Spring and Hibernate
- **Security package** contains class, allows to create UserDetails which store user information;



## Steps to run the program on your computer:
1. Clone the repo: https://github.com/mrmax24/cinema-app;
2. Install MySQL;
3. Create new schema in database;
4. Add you DB properties to db.properties file;
5. Configure Apache Tomcat version 9.0.50 **Artifact**: `war-exploded artifact`, **Application context**: `"/"`;
6. Create connection to DB using Database option (Intellij Idea Ultimate).
7. If you haven't Database option, connect to DB manually in src/main/resources/db.properties;
8. Done. Now just run it.
9. You can log in both as USER or ADMIN:
```bash
ADMIN: username: admin@i.ua, password: admin123
USER: username: user@i.ua, password: user123
```
10. Use **Postman** to send some http requests;


