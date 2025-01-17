# Express.js Server Unresponsiveness Bug

This repository demonstrates a common issue in Express.js applications where asynchronous operations within route handlers can cause the server to hang or become unresponsive.  The bug involves a long-running asynchronous operation that blocks the event loop, preventing other requests from being processed.

## Bug Description

The `bug.js` file contains an Express.js server with a route handler that includes a `setTimeout` function simulating a long-running task.  While this task executes, the server is unable to respond to other requests, leading to unresponsiveness and potential timeouts.

## Solution

The `bugSolution.js` file presents a solution using promises or async/await to handle the asynchronous operation without blocking the event loop.  This allows the server to remain responsive to other requests even while the long-running task is in progress.

## How to Reproduce

1. Clone the repository.
2. Navigate to the directory containing `bug.js`.
3. Run the server using `node bug.js`.
4. Open a browser and send multiple requests to the server. Notice the delays and potential unresponsiveness.
5. Repeat with `bugSolution.js` to see the improvement.