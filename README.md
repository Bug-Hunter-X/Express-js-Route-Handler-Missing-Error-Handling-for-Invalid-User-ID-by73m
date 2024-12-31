# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. Specifically, the provided code attempts to parse a user ID from a route parameter without verifying that the ID is a valid number.  This can lead to unexpected behavior or crashes.

## Bug
The `bug.js` file contains the erroneous code.  It fails to handle cases where the `userId` parameter is not a valid integer, causing `parseInt(userId)` to return `NaN`, which will result in an error when compared to user IDs in the database.

## Solution
The `bugSolution.js` file provides a corrected version that includes error handling.  It checks if `parseInt(userId)` results in a valid number before proceeding, preventing crashes and providing a more robust solution.