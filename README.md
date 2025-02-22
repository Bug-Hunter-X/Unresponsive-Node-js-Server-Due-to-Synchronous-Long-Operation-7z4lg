# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler blocks the event loop, causing the server to become unresponsive.  The solution showcases how to address this using asynchronous operations.

## Bug

The `server.js` file contains a Node.js HTTP server.  A synchronous `while` loop simulates a long-running operation (5 seconds), blocking the event loop and preventing the server from handling subsequent requests.  This leads to unresponsiveness.

## Solution

The `server-solution.js` file demonstrates the solution.  The long-running operation is replaced with asynchronous functionality using `setTimeout` or promises, allowing the event loop to remain responsive while the operation completes.