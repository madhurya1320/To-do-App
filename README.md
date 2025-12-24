# Todo App

[![Build](https://img.shields.io/badge/build-unknown-lightgrey)](https://shields.io/) [![Tests](https://img.shields.io/badge/tests-unknown-lightgrey)](https://shields.io/) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow.svg)](LICENSE)

Minimal Spring Boot TODO web application for creating, listing, and toggling tasks.

## Overview

This repository contains a small Java Spring Boot application that demonstrates a server-rendered TODO list with a simple HTML UI. Tasks have a title and a completed state. The app is organized with Controller, Service, Repository, and Model layers.

## Features

- Create new tasks
- List all tasks
- Toggle task completed status
- Server-rendered HTML UI (Thymeleaf-style template)

## Tech stack

- Java (Spring Boot)
- Maven (project includes the Maven wrapper)
- Thymeleaf-style server-side templates (HTML)

## Requirements

- Java 11+ (use the JDK version configured in your environment)
- Maven (optional; the project includes `mvnw`/`mvnw.cmd`)

## Quick start

1. Open a terminal and change to the project folder:

```bash
cd todo-app
```

2. Build the project (Linux/macOS):

```bash
./mvnw clean package
```

On Windows use:

```powershell
mvnw.cmd clean package
```

3. Run the application (development):

```bash
./mvnw spring-boot:run
```

Or run the packaged jar:

```bash
java -jar target/*.jar
```

4. Open your browser to http://localhost:8080 (or the port shown in the console).

## Project structure (important files)

- `src/main/java/com/todo_app/todo_app/TodoAppApplication.java` — Application entry point
- `src/main/java/com/todo_app/todo_app/Controller/TaskController.java` — HTTP endpoints
- `src/main/java/com/todo_app/todo_app/Service/TaskService.java` — Business logic
- `src/main/java/com/todo_app/todo_app/repository/TaskRepository.java` — Persistence layer
- `src/main/java/com/todo_app/todo_app/models/Task.java` — Task model
- `src/main/resources/templates/tasks.html` — Server-rendered tasks page
- `src/main/resources/application.properties` — Configuration

## Tests

Run the test suite with:

```bash
./mvnw test
```

On Windows:

```powershell
mvnw.cmd test
```

## Configuration

Adjust `src/main/resources/application.properties` to change server port or persistence settings.

## Contributing

1. Fork the repository
2. Create a branch for your feature/fix
3. Run tests and linting locally
4. Open a pull request describing your changes

## Possible improvements

- Persist tasks to an actual database (H2, PostgreSQL, etc.) instead of in-memory storage
- Add task editing and deletion
- Add REST API endpoints returning JSON for integration with SPA or mobile clients
- Add tests covering service and controller logic

