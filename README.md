# JavaScript NaN Equality Bug

This repository demonstrates a common JavaScript bug related to comparing NaN (Not a Number) values using loose equality (===).  In JavaScript, NaN is unique in that it's not equal to itself.

## Bug Description
The `foo` function aims to check if two numbers are equal. However, due to the nature of NaN, the comparison fails when both inputs are NaN, resulting in an incorrect 'false' return value.

## How to Reproduce
1. Clone this repository.
2. Open `bug.js`.
3. Run the code in a JavaScript environment (e.g., Node.js, browser console).
4. Observe the unexpected output.

## Solution
The solution involves using `Number.isNaN()` to explicitly check for NaN values before making a comparison.

## Additional Notes
This bug highlights the importance of understanding how NaN behaves in JavaScript and the need for careful handling when performing equality checks with potentially undefined or unexpected values.  Strict equality (===) is preferred for most comparisons, but it doesn't provide a direct solution for handling NaN properly.