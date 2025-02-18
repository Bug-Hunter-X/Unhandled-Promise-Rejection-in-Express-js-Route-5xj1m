# Unhandled Promise Rejection in Express.js Route

This repository demonstrates a common error in Express.js applications: unhandled promise rejections within asynchronous route handlers.  Improper error handling can lead to silent failures, application crashes, or unexpected behavior.

## Problem

The `bug.js` file showcases an Express.js route that performs an asynchronous operation (`someAsyncOperation`).  If this operation fails, the error is logged to the console, but Express.js doesn't catch it. This can lead to a silent failure or a crash depending on the nature of the error.

## Solution

The `bugSolution.js` file demonstrates the proper way to handle errors within asynchronous Express.js routes using a `try...catch` block.  This ensures that the server handles errors gracefully and provides a consistent response to the client.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js` and observe the console output (it will log errors to console without proper error handling).
4. Run `node bugSolution.js` and observe the more robust error handling.
