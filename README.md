# Todo API Project

This is a simple Todo API project built with ASP.NET Core and Entity Framework Core, using an in-memory database. The API provides basic CRUD operations for managing todo items and includes Swagger documentation for easy exploration and testing.

## Features

- In-memory database for data storage.
- CRUD endpoints for managing todo items.
- Swagger UI for API documentation and testing.

## Prerequisites

- [.NET SDK 6.0 or later](https://dotnet.microsoft.com/download)
  
## Getting Started

Follow these steps to run the project locally.

### 1. Clone the repository

```bash
git clone https://github.com/thectogeneral/Todo-API.git
cd Todo-API
```

### 2. Build the project

Navigate to the project directory and run:

```bash
dotnet build
```

### 3. Run the project

Run the project with:
```bash
dotnet run
```

### 4. Access the API

Once the application is running, you can access the API endpoints at http://localhost:5000 (or another port if specified).

### API Endpoints

| Method | Endpoint                 | Description                            |
|--------|---------------------------|----------------------------------------|
| GET    | `/`                      | Returns "Hello World!" message.        |
| GET    | `/todoitems`             | Retrieves all todo items.              |
| GET    | `/todositems/complete`   | Retrieves all completed todo items.    |
| GET    | `/todoitems/{id}`        | Retrieves a specific todo item by ID.  |
| POST   | `/todoitems`             | Creates a new todo item.               |
| PUT    | `/todoitems/{id}`        | Updates a specific todo item by ID.    |
| DELETE | `/todoitems/{id}`        | Deletes a specific todo item by ID.    |

In development mode, Swagger UI will be available at:
```bash
http://localhost:5000/swagger
```

### Sample JSON for Todo Item

When creating or updating a todo item, the JSON structure should look like this:
```bash
{
  "name": "Sample Task",
  "isComplete": false
}
```

### Project Structure

	•	TodoDb: The database context, using an in-memory database.
	•	Endpoints: Defined for each operation:
	•	GET endpoints for retrieving todos.
	•	POST endpoint for creating a new todo.
	•	PUT endpoint for updating an existing todo.
	•	DELETE endpoint for removing a todo.
