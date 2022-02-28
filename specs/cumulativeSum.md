**Name**: cumulativeSum

**Description**: Returns an array where each element is the sum of the preceding elements.

**Subject type (optional)**: Matrix

**Example:**
```
x = [ 1, 2, 3; 4, 5, 6 ] # A 2x3 matrix
y = x.cumulativeSum() # y is now equal to: [ 1, 3, 6, 10, 15, 21 ]
```

**Function spec written in Python, Swift or pseudocode:**
```python
def cumulativeSum(matrix):
    flattened = []
    for row in matrix:
        flattened += row
    result = []
    for i in range(len(flattened)):
        result.append(sum(flattened[0:i+1]))
    return result
```

**Preconditions:**
- All elements must be numeric.
