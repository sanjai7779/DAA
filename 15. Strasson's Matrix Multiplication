import numpy as np

def strassen_matrix_multiply(A, B):
    if len(A) == 1:
        return A * B

    # Divide matrices into four submatrices
    a, b, c, d = np.hsplit(A, 2)
    e, f, g, h = np.hsplit(B, 2)

    # Calculate seven products recursively
    p1 = strassen_matrix_multiply(a, f - h)
    p2 = strassen_matrix_multiply(a + b, h)
    p3 = strassen_matrix_multiply(c + d, e)
    p4 = strassen_matrix_multiply(d, g - e)
    p5 = strassen_matrix_multiply(a + d, e + h)
    p6 = strassen_matrix_multiply(b - d, g + h)
    p7 = strassen_matrix_multiply(a - c, e + f)

    # Calculate the four quadrants of the result matrix
    result_upper_left = p5 + p4 - p2 + p6
    result_upper_right = p1 + p2
    result_lower_left = p3 + p4
    result_lower_right = p1 + p5 - p3 - p7

    # Combine the four quadrants into the final result matrix
    result = np.vstack((np.hstack((result_upper_left, result_upper_right)),
                        np.hstack((result_lower_left, result_lower_right))))

    return result

# Example usage:
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

result = strassen_matrix_multiply(A, B)
print("Matrix A:")
print(A)
print("\nMatrix B:")
print(B)
print("\nResultant Matrix (using Strassen's algorithm):")
print(result)
