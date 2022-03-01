**Name**: sin, ln, abs, etc.

**Description**: Make these basic functions work for matrices, where the result is a matrix with all elements having that function applied

**Subject type (optional)**: N/A

**Example:**
```
x = [ 1, 2, 3; 4, 5, 6 ] # A 2x3 matrix
y = sin(x) # y is now equal to: [ 0.8415, 0.9093, 0.1411; -0.7568, -0.9589, -0.2794 ]
```

**Function spec written in Python, Swift or pseudocode:**
```python
def sin(matrix):
    result = []
    for i, j in matrix:
        result[i, j] = sin(matrix[i, j])
    return result
```

**Preconditions:**
- All elements must be numeric.
