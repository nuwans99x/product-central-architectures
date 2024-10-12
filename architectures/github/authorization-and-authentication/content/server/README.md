# Server Application - .NET

This directory contains the server-side application built with .NET for handling user authentication and authorization.

## Overview

The server application provides RESTful APIs for user registration, login, and role-based access control. It utilizes ASP.NET Core to manage user sessions and issues JSON Web Tokens (JWT) for secure communication.

## Features

- User Registration
- User Login
- JWT Token Generation
- Role-Based Access Control
- Password Hashing and Storage

## Prerequisites

- .NET 6.0 SDK or higher
- SQL Server (for database)

## Getting Started

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd server

2. Restore dependencies:
    ```bash
    dotnet restore

3. Configure the database: Update the appsettings.json file with your database connection string.

4. Run database migrations:
    ```bash
    dotnet ef database update

5. Run the application:
    ```bash
    dotnet run

    The API will be available at http://localhost:5000.

## API Endpoints
Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	Log in an existing user
GET	/api/auth/profile	Get user profile information
GET	/api/auth/roles	Get available roles

## Security Considerations
- Ensure HTTPS is used for secure data transmission.
- Use secure password hashing algorithms (e.g., BCrypt).
- Validate user input to prevent security vulnerabilities like SQL Injection.

## Documentation
Refer to the main repository README for an overview of the architecture and setup instructions.

## License
This project is licensed under the MIT License.
