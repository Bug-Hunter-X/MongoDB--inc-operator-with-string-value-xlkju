# MongoDB $inc operator with string value
This repository demonstrates an uncommon error in MongoDB update operations using the `$inc` operator.  The problem arises from providing a string value instead of a numeric value to the `$inc` operator, resulting in a silent failure and incorrect data modification.

The `bug.js` file contains the problematic code, while `bugSolution.js` provides the correct implementation.

## How to reproduce
1. Clone the repository.
2. Run the `bug.js` script. Observe that the `field` value will not be incremented.
3. Run the `bugSolution.js` script. The `field` value will be correctly incremented.

## How to fix
Ensure that the value provided to the `$inc` operator is a valid number. Avoid using strings.