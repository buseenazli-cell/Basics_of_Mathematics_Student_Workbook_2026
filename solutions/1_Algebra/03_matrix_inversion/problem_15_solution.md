# Exercise 15 — Solving a System Using Two Methods

## 1. Problem Statement

Solve the following system of linear equations using:

1. The inverse matrix method.
2. Gaussian elimination.

\[
2x+y=7
\]

\[
x+3y=8
\]

Compare the two methods.

## 2. Theoretical Background and Concepts

A system of linear equations can be represented in matrix form:

\[
Ax=b
\]

If \(A\) is invertible, the solution is

\[
x=A^{-1}b
\]

Gaussian elimination solves the same system by applying elementary row operations to the augmented matrix.

Both methods should produce the same solution.

## 3. Detailed Step-by-Step Solution

### Method 1: Inverse Matrix Method

Write the system in matrix form:

\[
A=
\begin{pmatrix}
2 & 1\\
1 & 3
\end{pmatrix},
\qquad
b=
\begin{pmatrix}
7\\
8
\end{pmatrix}
\]

First, calculate the determinant:

\[
\det(A)=2(3)-1(1)
\]

\[
\det(A)=6-1=5
\]

Since the determinant is not zero, the inverse exists.

Calculate the inverse:

\[
A^{-1}
=
\frac15
\begin{pmatrix}
3 & -1\\
-1 & 2
\end{pmatrix}
\]

Now calculate the solution:

\[
x=A^{-1}b
\]

\[
x=
\frac15
\begin{pmatrix}
3 & -1\\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
7\\
8
\end{pmatrix}
\]

\[
x=
\frac15
\begin{pmatrix}
21-8\\
-7+16
\end{pmatrix}
\]

\[
x=
\frac15
\begin{pmatrix}
13\\
9
\end{pmatrix}
\]

Therefore,

\[
\boxed{x=\frac{13}{5},\qquad y=\frac95}
\]

### Method 2: Gaussian Elimination

Start with the augmented matrix:

\[
\left[
\begin{array}{cc|c}
2 & 1 & 7\\
1 & 3 & 8
\end{array}
\right]
\]

**Step 1:** Swap the two rows.

\[
R_1\leftrightarrow R_2
\]

\[
\left[
\begin{array}{cc|c}
1 & 3 & 8\\
2 & 1 & 7
\end{array}
\right]
\]

**Step 2:** Eliminate the 2 below the first pivot.

\[
R_2\rightarrow R_2-2R_1
\]

\[
\left[
\begin{array}{cc|c}
1 & 3 & 8\\
0 & -5 & -9
\end{array}
\right]
\]

**Step 3:** Make the second pivot equal to 1.

\[
R_2\rightarrow-\frac15R_2
\]

\[
\left[
\begin{array}{cc|c}
1 & 3 & 8\\
0 & 1 & \frac95
\end{array}
\right]
\]

**Step 4:** Eliminate the 3 above the second pivot.

\[
R_1\rightarrow R_1-3R_2
\]

\[
\left[
\begin{array}{cc|c}
1 & 0 & \frac{13}{5}\\
0 & 1 & \frac95
\end{array}
\right]
\]

Therefore,

\[
\boxed{x=\frac{13}{5},\qquad y=\frac95}
\]

## 4. Verification and Consistency Checks

Substitute the calculated values into the original equations.

First equation:

\[
2\left(\frac{13}{5}\right)+\frac95
=
\frac{26}{5}+\frac95
=
\frac{35}{5}=7
\]

Second equation:

\[
\frac{13}{5}+3\left(\frac95\right)
=
\frac{13}{5}+\frac{27}{5}
=
\frac{40}{5}=8
\]

Both equations are satisfied.

The two methods produce the same result:

\[
\boxed{x=\frac{13}{5},\qquad y=\frac95}
\]

### Comparison of the Methods

- The inverse matrix method is useful when the inverse of the coefficient matrix is already known or needed.
- Gaussian elimination is generally more efficient for larger systems when only the solution is required.
- Both methods give the same solution in this exercise.

Therefore, the solution is verified and consistent.
