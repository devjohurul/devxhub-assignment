# DevXHub API

A Spring Boot REST API that demonstrates basic authentication and authorization mechanisms with role-based access control.

## Features

- REST API with public and protected endpoints
- Role-based access control (USER and ADMIN roles)
- Basic authentication
- User management
- JWT-based stateless authentication

## Technical Stack

- Java 21 (Amazon Corretto 21.0.7)
- Spring Boot 3.5.3
- Spring Security 6.x
- JPA/Hibernate
- Gradle
- PostgreSQL

## API Endpoints

| Endpoint | Method | Access | Description |
|----------|--------|--------|-------------|
| `/public` | GET | Public | Open endpoint accessible without authentication |
| `/user` | GET | USER, ADMIN | Protected endpoint for authenticated users |
| `/admin` | GET | ADMIN | Protected endpoint for admin users only |
| `/users` | POST | ADMIN | Create a new user |

## Authentication

The application includes two predefined users:
- Username: `intern`, Password: `password123`, Role: `USER`
- Username: `admin`, Password: `admin123`, Role: `ADMIN`

JWT tokens are used for stateless authentication with token expiration of 1 hour.

## Getting Started

### Database Configuration

The application requires a PostgreSQL database with the following configuration:
- spring.datasource.url=jdbc:postgresql://localhost:5432/intern_db
- spring.datasource.username=postgres
- spring.datasource.password=root
- spring.jpa.hibernate.ddl-auto=update

#### Ensure that PostgreSQL is installed and the database has been created before running the application.

### Prerequisites

- Java 21+
- Gradle 7.x+
- PostgreSQL database

### Setup Instructions

1. Clone the repository
2. Configure your PostgreSQL database according to application properties
3. Build the application
4. Run the application
5. The API will be available at http://localhost:8080
