**Name**: readCSV

**Description**: Reads the file as a UTF-8 Comma-Separated Values file, and automatically parses the values where possible (e.g. numbers).

**Subject type (optional)**: File

**Example:**
```
# F is a CSV file with the contents:
# Day,Value
# 1,0.71
# 2,0.98
# 3,0.72
# 4,0.6
# 5,0.89
y = F.readCSV()
print(y) # This will print [ [ \"Day\", \"Value\" ], [ 1, 0.71 ], [ 2, 0.98 ], [ 3, 0.72 ], [ 4, 0.6 ], [ 5, 0.89 ] ]
```

**Function spec written in Python, Swift, pseudocode, or explained in words:**
```
When this function is called on a variable holding a CSV file, it should read each line of the CSV file. For each line it should create an array containing the comma separated elements. If possible it should try to parse the elements to the appropriate types. The result should be an array of arrays.     
```

**Preconditions:**
- The file must be a CSV file.
