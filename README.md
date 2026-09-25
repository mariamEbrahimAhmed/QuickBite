# QuickBite

QuickBite is a food ordering platform planned as a monorepo.

## Projects

- `backend/` - Spring Boot REST API
- `web/` - React client (planned)
- `mobile/` - Flutter or React Native client (planned)

## Backend

Requirements:

- Java 17+
- Maven 3.9+

Run the backend:

```bash
cd backend
mvn spring-boot:run
```

The initial health endpoint is available at `http://localhost:8080/api/health`.
