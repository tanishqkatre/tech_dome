**Python Django Web API**

This repository contains a Python web API built with Django. The API provides endpoints for managing todo items and user authentication.

**Table of Contents**

**Requirements**
        API Endpoints
        TodoController
        AuthController
        Authorization
        JWT Token
Project Structure
Documentation
Submission
Requirements
Python 3.x
Django
SQL Server database
API Endpoints
**TodoController**
GET /todo/get/{id} : Get single todo item
GET /todo/getall : Get all the todo items
PUT /todo/put/{id} : Update single Todo item
POST /todo/{id} : Create new todo item
DELETE /todo/delete/{id} : Delete a todo item
**AuthController**
POST /auth/register : Register a new user
POST /auth/login : Login with existing user
Authorization
Access to TodoController endpoints is protected by authorization headers managed by AuthController. Only authenticated users will have access to TodoController. There are two roles:

**User:** Can get a list of todo items. Accessing other APIs results in a HTTP 401: Unauthorized error.
**Admin:** Has access to all APIs.
JWT Token
Upon successful login, a JWT token is returned in the response. The token contains the following encoded fields:

First Name
Last Name
Email
IsActive
Roles
