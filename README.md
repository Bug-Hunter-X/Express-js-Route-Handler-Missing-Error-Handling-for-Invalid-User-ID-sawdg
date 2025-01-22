# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer but doesn't handle cases where the `id` is not a number, resulting in a potential crash or unexpected behavior.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides a corrected version with robust error handling.

## Bug

The original code fails to handle non-numeric user IDs, leading to a crash or an incorrect response.  This makes the application vulnerable and unpredictable.

## Solution

The solution adds error handling to check if the `userId` is a number and gracefully handle cases where it's not, sending an appropriate error response to the client.