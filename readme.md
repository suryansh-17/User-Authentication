# User Authenticator

This is a simple user authentication service built with Node.js and Express.js. It provides endpoints for user registration, login, logout, token refresh, and password change. This service uses JWT (JSON Web Tokens) for securing routes.

## Features

- User registration
- User login
- User logout (secured route)
- Token refresh
- Change password (secured route)

## Prerequisites

- Node.js (v12.x or higher)
- npm (v6.x or higher)

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/suryansh-17/User-Authentication.git
    ```

2. Navigate to the project directory:

    ```sh
    cd User-Authentication
    ```

3. Install dependencies:

    ```sh
    npm install
    ```

## Running the Server

1. Start the server:

    ```sh
    npm run dev
    ```

2. The server will run on `http://localhost:3000`.

## Routes

### User Registration

- **URL**: `/users/register`
- **Method**: `POST`
- **Description**: Registers a new user.
- **Request Body**:
    ```json
    {   
        "username":"usernname",
        "email":"exampleEmail",
        "fullName":"exampleName",
        "password":"examplePassword"
    }
    ```

### User Login

- **URL**: `/users/login`
- **Method**: `POST`
- **Description**: Logs in an existing user.
- **Request Body**:
    ```json
    {
        "email": "exampleUser",
        "password": "examplePassword"
    }
    ```

### User Logout

- **URL**: `/users/logout`
- **Method**: `POST`
- **Description**: Logs out the current user. (Secured route)
- **Headers**: 
    ```json
    {
        "Authorization": "Bearer <token>"
    }
    ```

### Change Password

- **URL**: `/users/change-password`
- **Method**: `POST`
- **Description**: Changes the current password of the user. (Secured route)
- **Headers**: 
    ```json
    {
        "Authorization": "Bearer <token>"
    }
    ```
- **Request Body**:
    ```json
    {
        "oldPassword": "oldPassword",
        "newPassword": "newPassword"
    }
    ```

