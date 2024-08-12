# CMPG-323-Project-2---39013219-
This project is a CRUD RESTful API for managing telemetry data for NWU Tech Trends. The API allows users to perform operations such as retrieving, adding, updating, and deleting telemetry entries.

## Technologies Used
- .NET Core 8
- SQL Server
- Swagger
- JWT Authentication

## Setup Instructions
1. Clone the repository.
2. Open the solution in Visual Studio.
3. Set up the database using the provided SQL script.
4. Run the project to start the API.

## Implemented Features
- User Authentication
- CRUD Operations for Telemetry Data
- JWT Token Generation

##What to do as a(User): 
# NWU Tech Trends API

Welcome to the NWU Tech Trends API documentation. This API provides functionality for user authentication, registration, and more. Below you'll find details on how to use the API, including a list of available endpoints and their descriptions.

## Table of Contents
1. [Base URL](#base-url)
2. [Authentication](#authentication)
3. [Endpoints](#endpoints)
   - [Login](#login)
   - [Logout](#logout)
   - [Register User](#register-user)
   - [Register Admin](#register-admin)
   - [Admin Only Endpoint](#admin-only-endpoint)
   - [Refresh Token](#refresh-token)
4. [Error Handling](#error-handling)
5. [Rate Limiting](#rate-limiting)
6. [Reference List](#reference-list)

## Base URL

The base URL for all API requests is:

## Authentication

To access certain endpoints, you need to authenticate using a JWT token. Include the token in the `Authorization` header as follows:


## Endpoints

### Login

- **URL:** `/api/authenticate/login`
- **Method:** POST
- **Body:**
  ```json
  {
    "username": "string",
    "password": "string"
  }

### Logout

- **URL:** `/api/authenticate/logout`
- **Method:** POST
- **Body:**
  ```json
  {
    "token": "string",
    "refreshToken": "string"
   }

### Register User

- **URL:** `/api/authenticate/register`
- **Method:** POST
- **Body:**
  ```json
  {
    "username": "string",
    "email": "string",
    "password": "string"
  }
  
### Register Admin

- **URL:** `/api/authenticate/register-admin`
- **Method:** POST
- **Body:**
  ```json
  {
    "username": "string",
    "email": "string",
    "password": "string"
  }
  
### Admin Only Endpoint

- **URL:** `/api/authenticate/admin-only-endpoint`
- **Method:** POST
- **Body:**
  ```json
  {
    "This is an admin-only endpoint."
  }

### Refresh Token

- **URL:** `/api/authenticate/refresh-token`
- **Method:** POST
- **Body:**
  ```json
  {
    "token": "string",
    "refreshToken": "string"
  }

## Error Handling
The API uses standard HTTP status codes to indicate the result of requests. Error messages are included in the response body for easier debugging.

## Rate Limiting
The API implements rate limiting to prevent abuse. If the rate limit is exceeded, a 429 Too Many Requests status code will be returned.

## Reference List

AspNetCoreRateLimit. (n.d.). AspNetCoreRateLimit Documentation. [online] Available at: https://github.com/stefanprodan/AspNetCoreRateLimit [Accessed 12 Aug. 2024].

Serilog. (n.d.). Serilog Documentation. [online] Available at: https://serilog.net/ [Accessed 12 Aug. 2024].

JWT.io. (n.d.). Introduction to JSON Web Tokens. [online] Available at: https://jwt.io/introduction/ [Accessed 12 Aug. 2024].
