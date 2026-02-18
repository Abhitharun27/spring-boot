# Spring Boot 3 JWT + MySQL Example

This project is a Spring Boot **3.x** application with:

- Spring Security (stateless)
- JWT generation and validation
- MySQL persistence using Spring Data JPA

## Requirements

- Java 17+
- Maven 3.9+
- MySQL 8+

## Configuration

Update `src/main/resources/application.yml` if your MySQL credentials differ.

## Run

```bash
mvn spring-boot:run
```

## API

### Register

`POST /api/auth/register`

```json
{
  "username": "alice",
  "password": "password123"
}
```

Returns:

```json
{
  "token": "<jwt>"
}
```

### Login

`POST /api/auth/login`

```json
{
  "username": "alice",
  "password": "password123"
}
```

Returns:

```json
{
  "token": "<jwt>"
}
```

### Secured endpoint

`GET /api/hello`

Set header:

`Authorization: Bearer <jwt>`
