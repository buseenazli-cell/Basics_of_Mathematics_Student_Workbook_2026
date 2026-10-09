"""
Exercise 2: Matrix addition, subtraction and linear combination
"""
import numpy as np

A = np.array([[ 1, 2],
              [-1, 3]])

B = np.array([[4, -2],
              [0,  5]])

print("A + B =\n", A + B)          # [[ 5  0] [-1  8]]
print("A - B =\n", A - B)          # [[-3  4] [-1 -2]]
print("3A - 2B =\n", 3 * A - 2 * B)  # [[-5 10] [-3 -1]]

# Why must the sizes be equal? Addition works entry by entry,
# so every entry of A needs a partner entry in B.
C = np.array([[1, 2, 3],
              [4, 5, 6]])  # 2 x 3

try:
    print(A + C)  # 2x2 + 2x3 -> not defined
except ValueError as e:
    print("Error: A (2x2) and C (2x3) cannot be added ->", e)
