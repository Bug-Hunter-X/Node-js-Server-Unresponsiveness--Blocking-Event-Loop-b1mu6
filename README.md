# Node.js Server Unresponsiveness: Blocking Event Loop

This repository demonstrates a common issue in Node.js applications where a long-running synchronous operation blocks the event loop, causing the server to become unresponsive.  The `server.js` file contains the problematic code. The solution is provided in `server-solution.js`.

## Problem
The server uses a `while` loop to simulate a time-consuming task within the request handler. This blocks the event loop, preventing it from processing other requests and potentially leading to timeouts or connection issues.

## Solution
The solution involves using asynchronous operations or offloading long-running tasks to worker threads or a message queue to avoid blocking the event loop.