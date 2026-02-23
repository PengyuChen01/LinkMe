# LinkMe

A mobile H5 web application that helps people find like-minded partners based on tags, team matching, and smart recommendations.

## Features

- **Tag System** - Users can add and manage personal tags (skills, interests, goals, etc.)
- **Search** - Search for other users by tags, with Redis caching support
- **Teams** - Create teams, join teams, search teams by tags, invite members
- **Recommendations** - Similarity-based user recommendations using distributed computing

## Tech Stack

### Backend
- Java 21 + Spring Boot 3.4
- Spring MVC + MyBatis Plus
- MySQL
- Redis (caching)
- Swagger + Knife4j (API docs)

### Frontend
- Vue 3
- Vant UI (mobile component library)
- Vite

## Project Structure

```
LinkMe/
├── backend/          # Spring Boot backend
│   ├── src/main/java/com/linkme/backend/
│   │   ├── common/       # Base response, error codes, utils
│   │   ├── constant/     # Constants
│   │   ├── controller/   # REST controllers
│   │   ├── exception/    # Custom exceptions & global handler
│   │   ├── mapper/       # MyBatis Plus mappers
│   │   ├── model/        # Domain models & request DTOs
│   │   └── service/      # Service interfaces & implementations
│   └── src/main/resources/
│       └── application.properties
├── frontend/         # Vue 3 frontend
└── BusinessRequirement.txt
```

## Getting Started

### Prerequisites
- JDK 21
- MySQL 8.x
- Maven 3.9+

### Backend Setup

1. Create the MySQL database:
   ```sql
   CREATE DATABASE linkme;
   ```

2. Configure database connection in `backend/src/main/resources/application.properties`

3. Run the application:
   ```bash
   cd backend
   ./mvnw spring-boot:run
   ```

4. The server starts at `http://localhost:8080`

## API Endpoints

| Method | Path           | Description       |
|--------|----------------|-------------------|
| POST   | /user/register | User registration |
| POST   | /user/login    | User login        |
| POST   | /user/logout   | User logout       |
| GET    | /user/current  | Get current user  |
| GET    | /user/search   | Search users (admin) |
| POST   | /user/delete   | Delete user (admin)  |
