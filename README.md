# Unhandled Error in Async Express.js Callback

This repository demonstrates a common error in Node.js applications using Express.js: unhandled errors within asynchronous callbacks.  The `bug.js` file shows an Express.js server that simulates an asynchronous operation.  Sometimes, this operation throws an error, which is not caught, leading to the server crashing. The `bugSolution.js` file provides a corrected version that properly handles this error.

## Problem

The `bug.js` server uses `setTimeout` to simulate an asynchronous task. If the random condition is true, an error is thrown directly within the callback.  Because there's no `try...catch` block around this potentially problematic code, the error is uncaught, resulting in a crash. 

## Solution

The `bugSolution.js` file shows how to properly handle this using a `try...catch` block within the callback. This ensures that even if an error occurs, the server continues running and handles the error gracefully. The error is logged to the console to assist debugging.