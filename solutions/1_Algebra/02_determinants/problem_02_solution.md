# Problem Statement

For 

$$A=\begin{pmatrix}1&2&-1\\0&3&4\\2&1&5\end{pmatrix}$$ 

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

---

## Solution

### 1. Computation using Sarrus' Rule

Sarrus' rule states that for a $3 \times 3$ matrix, the determinant is calculated by extending the matrix by appending its first two columns to the right, then taking the sum of the products along the main diagonals minus the sum of the products along the anti-diagonals.

Writing the extended matrix with the first two columns repeated:

$$\begin{pmatrix} 
1 & 2 & -1 & \mid & 1 & 2 \\ 
0 & 3 & 4 & \mid & 0 & 3 \\ 
2 & 1 & 5 & \mid & 2 & 1 
\end{pmatrix}$$

#### Downward (Main) Diagonals:
* $d_1 = (1) \cdot (3) \cdot (5) = 15$
* $d_2 = (2) \cdot (4) \cdot (2) = 16$
* $d_3 = (-1) \cdot (0) \cdot (1) = 0$

$$\text{Sum of downward products} = 15 + 16 + 0 = 31$$

#### Upward (Anti) Diagonals:
* $u_1 = (2) \cdot (3) \cdot (-1) = -6$
* $u_2 = (1) \cdot (4) \cdot (1) = 4$
* $u_3 = (5) \cdot (0) \cdot (2) = 0$

$$\text{Sum of upward products} = (-6) + 4 + 0 = -2$$

#### Final Determinant Calculation:
$$\det A = (\text{Sum of downward products}) - (\text{Sum of upward products})$$
$$\det A = 31 - (-2) = 31 + 2 = 33$$

---

### 2. Verification using Determinant Properties

To check our result, we can compute $\det A$ using **Cofactor Expansion (Laplace expansion)** along the **first column**, which contains a zero to simplify calculation.

Property: Expanding along column 1 gives:
$$\det A = a_{11} C_{11} + a_{21} C_{21} + a_{31} C_{31}$$

where $C_{ij} = (-1)^{i+j} M_{ij}$, and $M_{ij}$ is the minor determinant obtained by removing row $i$ and column $j$.

1. **For $a_{11} = 1$:**
   $$M_{11} = \det \begin{pmatrix} 3 & 4 \\ 1 & 5 \end{pmatrix} = (3)(5) - (4)(1) = 15 - 4 = 11$$
   $$a_{11} C_{11} = 1 \cdot (+1) \cdot 11 = 11$$

2. **For $a_{21} = 0$:**
   $$a_{21} C_{21} = 0$$

3. **For $a_{31} = 2$:**
   $$M_{31} = \det \begin{pmatrix} 2 & -1 \\ 3 & 4 \end{pmatrix} = (2)(4) - (-1)(3) = 8 - (-3) = 11$$
   $$a_{31} C_{31} = 2 \cdot (+1) \cdot 11 = 22$$

Summing these contributions:
$$\det A = 11 + 0 + 22 = 33$$

Both Sarrus' rule and cofactor expansion yield $\det A = 33$, confirming the result.
