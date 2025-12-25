# Architecture Documentation

This document describes the architectural patterns and project structure for the **eCommerce Backend**.

## Overview
The project follows the **Model-View-Controller (MVC)** design pattern, separation of concerns, and clean code principles.

## Directory Structure
```text
├── controllers/     # Business logic and request handling
├── models/          # Mongoose schemas and data models
├── routes/          # API route definitions
├── utils/           # Utility functions and helper classes
├── public/          # Static files (images, CSS, etc.)
├── views/           # EJS templates (for emails or basic web views)
├── dev-data/        # Sample data for development and seeding
├── app.js           # Express application configuration
└── server.js        # Entry point to start the server
```

## Core Patterns

### 1. MVC Pattern
- **Models**: Located in `models/`, they define the data structure and schema for MongoDB using Mongoose.
- **Views**: While primarily a backend API, `views/` holds EJS templates for server-side rendering (e.g., email templates).
- **Controllers**: Located in `controllers/`, they contain the logic to process requests, interact with models, and send responses.

### 2. Global Error Handling
The application uses a centralized error-handling middleware (`errorController.js`) and a custom `AppError` class. This ensures consistent error responses across all API endpoints.

### 3. Middleware Pipeline
Requests flow through a series of global and route-specific middlewares:
- Security headers (Helmet)
- CORS configuration
- Rate limiting
- Body parsing
- Data sanitization (NoSQL injection, XSS)
- Custom route handlers

### 4. Handler Factory
To reduce code duplication, common CRUD operations are abstracted into a `handlerFactory.js`. This allowed controllers to easily inherit standard functionality for finding, creating, updating, and deleting documents.

### 5. API Versions
The project uses versioned routing (e.g., `/api/v1/...`) to allow for future changes without breaking existing clients.
