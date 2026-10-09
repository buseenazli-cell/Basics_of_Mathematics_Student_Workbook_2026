"""
Exercise 1: Matrix Size and Entries
"""
import numpy as np

A = np.array([[2, -1, 3],
              [0,  4, 5]])

B = np.array([[ 1, 0],
              [-2, 3],
              [ 4, 1]])

# 1. Sizes (rows x columns)
print("Size of A:", A.shape)  # (2, 3)
print("Size of B:", B.shape)  # (3, 2)

# 2. Entries (math indices start at 1, Python indices start at 0)
a12 = A[0, 1]
a23 = A[1, 2]
b21 = B[1, 0]
b32 = B[2, 1]
print("a12 =", a12)  # -1
print("a23 =", a23)  # 5
print("b21 =", b21)  # -2
print("b32 =", b32)  # 1

# 3. Second row of A and first column of B
row_A2 = A[1, :]
col_B1 = B[:, 0]
print("Second row of A:", row_A2)    # [0 4 5]
print("First column of B:", col_B1)  # [ 1 -2  4]
