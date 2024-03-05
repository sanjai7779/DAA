def multiply_matrices(matrix1, matrix2):
    rows1, cols1 = len(matrix1), len(matrix1[0])
    rows2, cols2 = len(matrix2), len(matrix2[0])

    # Check if the matrices can be multiplied
    if cols1 != rows2:
        print("Cannot multiply matrices. Invalid dimensions.")
        return None

    # Initialize the result matrix with zeros
    result = [[0 for _ in range(cols2)] for _ in range(rows1)]

    # Perform matrix multiplication
    for i in range(rows1):
        for j in range(cols2):
            for k in range(cols1):
                result[i][j] += matrix1[i][k] * matrix2[k][j]

    return result

# Example usage:
matrix_a = [
    [2, 3, 4],
    [5, 6, 7],
    [8, 9, 10]
]

matrix_b = [
    [11, 12],
    [13, 14],
    [15, 16]
]

result_matrix = multiply_matrices(matrix_a, matrix_b)

if result_matrix:
    print("Matrix A:")
    for row in matrix_a:
        print(row)

    print("\nMatrix B:")
    for row in matrix_b:
        print(row)

    print("\nResultant Matrix:")
    for
