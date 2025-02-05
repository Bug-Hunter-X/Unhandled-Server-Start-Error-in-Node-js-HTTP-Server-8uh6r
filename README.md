# Unhandled Server Start Error in Node.js

This repository demonstrates a common error in Node.js HTTP servers: the lack of proper error handling during server startup.  The `server.listen()` method can throw errors (e.g., `EADDRINUSE` if the port is already in use), and without handling these, the application might fail silently.

The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version with error handling.

## How to reproduce:

1. Clone this repository.
2. Run `node server.js`.
3. Try running `node server.js` again immediately;  you won't see a clear error message indicating the port is already in use.
4. Run `node serverSolution.js` to see the improved error handling.