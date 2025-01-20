# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler blocks the event loop, causing the server to become unresponsive.  The `bug.js` file contains the problematic code, and `bugSolution.js` provides a corrected version using asynchronous operations.

## Bug
The server uses a `while` loop to simulate a 5-second delay, blocking the event loop and preventing it from processing other requests.  This makes the server unresponsive during this time.

## Solution
The solution utilizes asynchronous operations to avoid blocking the event loop. This is crucial for maintaining responsiveness in Node.js servers.