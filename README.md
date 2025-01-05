# Express.js: Handling Empty or Invalid JSON Request Bodies

This repository demonstrates a common issue in Express.js applications where the server fails to correctly handle empty or invalid JSON request bodies.  The provided code will log the request body and respond with 'Data received' regardless of whether valid JSON data was provided. This can lead to unexpected behavior and silent errors.

The solution provided addresses this issue by implementing proper error handling and validation. 

## Bug

The `bug.js` file contains the faulty Express.js code. When you send an empty request body or an invalid JSON body to the `/data` POST endpoint, the server will not throw an error and will log an empty object. This can be hard to debug, leading to unexpected behaviour in your application.

## Solution

The `bugSolution.js` file shows the improved implementation.  It uses a try...catch block to handle parsing errors and sends an appropriate error response to the client if the request body is not valid JSON.  This provides a more robust and user-friendly experience.