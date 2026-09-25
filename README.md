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
- MySQL 8+

### Database setup

Create the database and an application user (as MySQL `root`):

```sql
CREATE DATABASE quickbite;
CREATE USER 'quickbite_user'@'localhost' IDENTIFIED BY 'your_password';
GRANT ALL PRIVILEGES ON quickbite.* TO 'quickbite_user'@'localhost';
```

Copy the environment template and fill in your password:

```bash
cd backend
cp .env.example .env
```

`backend/.env` is gitignored and is loaded by `application.properties` on startup.

### Run

Run the backend from the `backend/` directory so `.env` is found:

```bash
cd backend
mvn spring-boot:run
```

Tests start the full application, so MySQL must be running for `mvn test`.

The initial health endpoint is available at `http://localhost:8080/api/health`.
