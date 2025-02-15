# Unexpected NaN Handling in JavaScript Function

This repository demonstrates a subtle bug in a JavaScript function related to the handling of NaN (Not a Number) values.  The `foo` function aims to perform conditional checks and return different values based on input, however, it doesn't explicitly address NaN, leading to unexpected outputs.

## The Bug

The `bug.js` file contains the problematic code. Observe that when the function receives `NaN`, it simply returns `NaN` without any special handling. This might not be the desired behavior in many applications where NaN should trigger a specific action (e.g., error handling, default value).

## The Solution

The `bugSolution.js` file provides a corrected version of the function, explicitly checking for `isNaN(x)` and providing a more robust response to such situations. This approach ensures that NaN values do not propagate unexpectedly through the application.

## How to reproduce

1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `node bug.js` to see the original, problematic behavior.
4. Run `node bugSolution.js` to see the improved version in action.
