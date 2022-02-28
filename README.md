# Luminal Function Specs

Help us improve Luminal by contributing a function spec! If the function spec meets our quality guidelines as well as the requirements listed below, we'll add it to Luminal and mention you as the contributor (unless you prefer not to be mentioned). **Before you initiate a pull request**, please read the requirements below.

## Requirements:

Luminal is a platform for engineering calculations, simulations and optimizations. It is not meant as a general purpose programming language. Function specs should be helpful to engineers.

A function spec must include the following:

- A name
- A plain English description of what the function does.
- The type on which the function operates, for example "Matrix", "Number" or "File" (optional).
- An example (this will be shown in the documentation and auto-complete).
- The function spec itself, written in Python, Swift or pseudocode.
- Preconditions specific to the function, if applicable.

**Example spec using Python:**

Name: cumulativeSum<br/>
Description: Returns an array where each element is the sum of the preceding elements.<br/>
Subject type: Matrix

Example:
```
x = [ 1, 2, 3; 4, 5, 6 ] # A 2x3 matrix
y = x.cumulativeSum() # y is now equal to: [ 1, 3, 6, 10, 15, 21 ]
```

Function spec:
```
def cumulativeSum(matrix):
    flattened = []
    for row in matrix:
        flattened += row
    count = len(flattened)
    if count == 0: raise Exception("Matrix must not be empty.")
    result = []
    for i in range(count):
        result.append(sum(flattened[0:i+1]))
    return result
```

Preconditions:
- All elements must be numeric.
- The matrix must not be empty.
