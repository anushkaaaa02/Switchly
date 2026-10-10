
# Switchly 🚀

**Switchly** is a backend application designed to manage feature flags for projects through RESTful APIs. It provides endpoints to create, retrieve, update, and delete feature flags, helping applications control feature availability in a structured way.

## ✨ Features

- **Feature Flag Management:** Create, retrieve, update, and delete feature flags.
- **Project-Based Flags:** Associate feature flags with specific projects.
- **Flag State Management:** Enable or disable feature flags through API requests.
- **RESTful API:** Interact with the application using standard HTTP methods.
- **In-Memory Storage:** Store application data using in-memory repository implementations.
- **Exception Handling:** Handle errors such as resources not found and conflicting requests.

## 🛠️ Tech Stack

- **Language:** Java
- **Framework:** Spring Boot
- **API Testing:** Postman
- **Build Tool:** Maven
- **Version Control:** Git and GitHub

## 📁 Project Structure

```text
apiswitchly/
└── api/
    └── src/
        └── main/
            ├── java/
            │   └── live/switchly/api/
            │       ├── controller/
            │       ├── dto/
            │       ├── exception/
            │       ├── model/
            │       ├── repository/
            │       └── service/
            └── resources/
                └── application.yaml
```

## ⚙️ Getting Started

### Prerequisites

Make sure you have the following installed:

- Java JDK 21
- Maven (or use the Maven Wrapper if available)
- Git
- Postman

### Installation

**1. Clone the repository**

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

**2. Navigate to the project directory**

```bash
cd Switchly/apiswitchly/api
```

**3. Run the application**

If the Maven Wrapper is available on Windows:

```bash
.\mvnw.cmd spring-boot:run
```

Alternatively, if Maven is installed:

```bash
mvn spring-boot:run
```

The application will start on the configured port. The current setup uses port `8080`.

## 🔗 API Endpoints

The API uses the base path `/api/v1`.

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/v1/projects/{projectId}/flags` | Create a feature flag |
| GET | `/api/v1/projects/{projectId}/flags` | Get all flags for a project |
| GET | `/api/v1/flags/{flagId}` | Get a flag by ID |
| PUT | `/api/v1/flags/{flagId}/state` | Enable or disable a flag |
| DELETE | `/api/v1/flags/{flagId}` | Delete a flag |

**Note:** The endpoints listed above reflect the current controller structure. Verify the exact request and response formats in the source code before using them.

## 🧪 Testing with Postman

You can test the REST APIs using Postman.

1. Start the Spring Boot application.
2. Create a new HTTP request in Postman.
3. Select the appropriate HTTP method.
4. Enter the endpoint URL.
5. For POST requests, select **Body → raw → JSON** and provide the required request data.
6. Click **Send** and inspect the response and HTTP status code.

Example base URL:

```text
http://localhost:8080/api/v1
```

## 🚀 Future Enhancements

- Integrate a persistent database such as PostgreSQL or MySQL.
- Add authentication and authorization.
- Implement automated unit and integration tests.
- Add API documentation using Swagger/OpenAPI.
- Introduce environment-specific feature flag configurations.

## 👩‍💻 Author

**Anushka Sharma**

GitHub: [anushkaaaa02](https://github.com/anushkaaaa02)

---

*Switchly — Manage feature availability through simple and structured APIs.*
