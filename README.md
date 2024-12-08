This repository demonstrates a common error encountered when working with JSON request bodies in Express.js applications. The bug involves the failure of the server to properly parse JSON data received from client requests. The solution showcases how to correctly configure middleware to handle JSON parsing and provides a functional example.

## Bug Description

The Express.js server fails to parse incoming JSON requests, resulting in an empty request body. This occurs despite the client sending a valid JSON payload. The issue stems from an incorrect or missing configuration of the middleware responsible for parsing JSON data.

## Solution

The solution involves correctly configuring the `express.json()` middleware to parse JSON request bodies. This middleware must be placed before the route handler that expects JSON data.

## How to reproduce the bug

1. Clone this repository.
2. Install dependencies using `npm install`.
3. Run the server using `node bug.js`.
4. Send a POST request to `/data` with a valid JSON payload using a tool like Postman or curl.
5. Observe that the server logs an empty object for `req.body`, indicating that the JSON body was not parsed correctly.

## How to fix the bug

1. Replace `bug.js` with `bugSolution.js`.
2. Run the server using `node bugSolution.js`.
3. Repeat steps 4 and 5 from the bug reproduction instructions.
4. Observe that the server logs the correctly parsed JSON data, indicating that the issue is resolved.