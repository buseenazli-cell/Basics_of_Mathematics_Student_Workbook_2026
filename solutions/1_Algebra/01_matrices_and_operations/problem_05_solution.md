import numpy as np

def main():
    # Define matrix A and vector x
    A = np.array([
        [2, -1],
        [1,  3]
    ])
    
    x = np.array([4, 2])
    
    print("=" * 50)
    print("LINEAR ALGEBRA: MATRIX-VECTOR MULTIPLICATION & LINEAR COMBINATION")
    print("=" * 50)
    
    # 1. Standard Matrix Multiplication (Ax)
    Ax_standard = A @ x
    print(f"1. Standard Multiplication (Ax): {Ax_standard}")
    
    # 2. Linear Combination of Columns
    c1 = A[:, 0]  # Column 1: [2, 1]
    c2 = A[:, 1]  # Column 2: [-1, 3]
    
    Ax_linear_comb = x[0] * c1 + x[1] * c2
    print(f"2. Linear Combination: {x[0]} * {c1} + {x[1]} * {c2} = {Ax_linear_comb}")
    
    # Verification
    is_equal = np.allclose(Ax_standard, Ax_linear_comb)
    print("-" * 50)
    print(f"Do both methods yield the same result?: {is_equal}")
    print("=" * 50)

if __name__ == "__main__":
    main()
