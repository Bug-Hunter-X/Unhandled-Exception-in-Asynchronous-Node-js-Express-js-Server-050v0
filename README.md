# Unhandled Exception in Asynchronous Node.js Express.js Server
This repository demonstrates a common issue in Node.js applications: unhandled exceptions within asynchronous callbacks. The example uses Express.js to create a simple server that randomly throws an exception.  Without proper error handling, this can lead to the server crashing.

## Bug
The `bug.js` file contains an Express.js server with a route that simulates an asynchronous operation.  If a random number is greater than 0.5, an exception is thrown within the `setTimeout` callback.  This exception is unhandled, causing the server to crash.

## Solution
The `bugSolution.js` file demonstrates how to properly handle this exception using a `try...catch` block within the asynchronous callback. This ensures that the server doesn't crash, even if an error occurs.