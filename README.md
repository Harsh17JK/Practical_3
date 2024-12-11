
# Function to add two matrices
def add_matrices(matrix1, matrix2):
    rows = len(matrix1)
    cols = len(matrix1[0])
    result = [[0 for _ in range(cols)] for _ in range(rows)]
    
    for i in range(rows):
        for j in range(cols):
            result[i][j] = matrix1[i][j] + matrix2[i][j]
    
    return result

# Function to subtract two matrices
def subtract_matrices(matrix1, matrix2):
    rows = len(matrix1)
    cols = len(matrix1[0])
    result = [[0 for _ in range(cols)] for _ in range(rows)]
    
    for i in range(rows):
        for j in range(cols):
            result[i][j] = matrix1[i][j] - matrix2[i][j]
    
    return result

# Function to multiply two matrices
def multiply_matrices(matrix1, matrix2):
    rows1 = len(matrix1)
    cols1 = len(matrix1[0])
    rows2 = len(matrix2)
    cols2 = len(matrix2[0])
    
    if cols1 != rows2:
        raise ValueError("Matrices cannot be multiplied due to incompatible dimensions")
    
    result = [[0 for _ in range(cols2)] for _ in range(rows1)]
    
    for i in range(rows1):
        for j in range(cols2):
            for k in range(cols1):
                result[i][j] += matrix1[i][k] * matrix2[k][j]
    
    return result

# Function to transpose a matrix
def transpose_matrix(matrix):
    rows = len(matrix)
    cols = len(matrix[0])
    result = [[0 for _ in range(rows)] for _ in range(cols)]
    
    for i in range(rows):
        for j in range(cols):
            result[j][i] = matrix[i][j]
    
    return result

# Example matrices
x = [[1, 2], [4, 5]]
y = [[7, 8], [9, 10]]

# Perform matrix addition
print("The element-wise addition of matrices is:")
addition_result = add_matrices(x, y)
for row in addition_result:
    print(row)

# Perform matrix subtraction
print("The element-wise subtraction of matrices is:")
subtraction_result = subtract_matrices(x, y)
for row in subtraction_result:
    print(row)

# Perform matrix multiplication
print("The product of matrices is:")
multiplication_result = multiply_matrices(x, y)
for row in multiplication_result:
    print(row)

# Perform matrix transpose
print("The transpose of the first matrix is:")
transpose_result = transpose_matrix(x)
for row in transpose_result:
    print(row)
```

### Explanation:
1. **Matrix Addition**: The `add_matrices` function adds the corresponding elements of two matrices.
2. **Matrix Subtraction**: The `subtract_matrices` function subtracts the corresponding elements of two matrices.
3. **Matrix Multiplication**: The `multiply_matrices` function multiplies two matrices based on the standard matrix multiplication rule, where each element in the result is the dot product of the corresponding row of the first matrix and column of the second matrix.
4. **Matrix Transpose**: The `transpose_matrix` function swaps the rows and columns of the matrix.

### Output Example:

```
The element-wise addition of matrices is:
[8, 10]
[13, 15]

The element-wise subtraction of matrices is:
[-6, -6]
[-5, -5]

The product of matrices is:
[25, 28]
[73, 82]

The transpose of the first matrix is:
[1, 4]
[2, 5]
```

This code performs all the required operations without using NumPy and with correct indentation.
