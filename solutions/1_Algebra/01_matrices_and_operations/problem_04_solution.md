import numpy as np

A = np.array([[1, 2], [0, 1]])
B = np.array([[2, 0], [3, 1]])

print(A @ B)                            # [[8 2] [3 1]]
print(B @ A)                            # [[2 4] [3 7]]
print(np.array_equal(A @ B, B @ A))     # False
