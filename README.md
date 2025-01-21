# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js servers: unresponsiveness due to long-running requests.  The `bug.js` file contains a server that simulates a long-running task, causing the server to hang during that time.  `bugSolution.js` provides a solution using asynchronous operations to prevent this issue. 

## Problem

Node.js is single-threaded.  When a request triggers a long-running synchronous operation, the entire server becomes blocked, unable to handle other requests. This leads to poor performance and potentially crashes.

## Solution

The solution involves using asynchronous operations (e.g., `setTimeout`, promises, async/await) to avoid blocking the main thread.  This allows the server to continue processing other requests while the long-running task executes in the background.