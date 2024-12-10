# Type Coercion Bug in JavaScript Addition Function

This repository demonstrates a subtle bug in a JavaScript addition function that arises from type coercion. The function `foo` is designed to return `null` if either of its inputs is `null`. However, it does not handle the case where one of the inputs is 0 (zero) correctly.

## The Bug

The issue lies in how JavaScript handles loose comparisons (`==`) and the implicit type conversion that occurs when using the addition operator (`+`). When 0 is passed as an argument, it leads to unexpected behaviour. If a loose comparison (`==`) was used then it would also have issues with type coercion. 

## The Solution

The solution involves using strict equality (`===`) to check for `null` values and explicitly handling the case where either input is 0.  This ensures that the function behaves as expected in all scenarios.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js` to see the buggy code.
3. Open `bugSolution.js` to see the corrected code.
4. Run both files in a JavaScript environment (e.g., node.js) to observe the different outputs.