# Missing Error Handling in Express.js POST Request

This repository demonstrates a common error in Express.js applications: missing error handling for POST requests.  The example shows a vulnerable `POST /users` endpoint that lacks proper validation and error handling.  This can lead to unexpected behavior, crashes, or security vulnerabilities.

## Bug

The `bug.js` file contains an Express.js server with a `POST /users` route. This route expects user data in the request body. However, it fails to handle cases where the request body is missing, empty, or contains invalid data.

## Solution

The `bugSolution.js` file provides a corrected version of the server with comprehensive error handling.  It validates the request body, and handles errors gracefully by sending appropriate HTTP status codes and error messages to the client.

## How to Run

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install the required dependencies.
4. Run `node bug.js` (for the buggy version) or `node bugSolution.js` (for the corrected version).
5. Test the endpoint using a tool like Postman or curl.