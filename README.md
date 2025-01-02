# MongoDB $inc Operator with String Value
This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries.  The example showcases how passing a string value instead of a number prevents the correct increment operation.

## Bug Description
The `$inc` operator is used to increment a numerical field. If you provide a string value instead of a number, the operation won't work as expected. The database won't throw an error but will not update the document correctly.  This subtle error can lead to difficult-to-debug inconsistencies in your data.

## How to Reproduce
1. Clone this repository.
2. Run a MongoDB instance.
3. Execute the code in `bug.js`.
4. Check the updated document in your MongoDB collection. The counter will not be incremented correctly.

## Solution
The solution involves ensuring that you always provide a numerical value to the `$inc` operator. The corrected code is in `bugSolution.js`.