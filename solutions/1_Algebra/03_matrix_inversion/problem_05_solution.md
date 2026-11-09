# Exercise 5 — Inverse of a 3×3 Matrix

## 1. Problem Statement

Given the matrix

\[
A =
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}
\]

Find its inverse using Gauss-Jordan elimination.

## 2. Theoretical Background and Concepts

Gauss-Jordan elimination can also be used for larger square matrices.

The augmented matrix is formed as

\[
[A \mid I]
\]

Elementary row operations are applied until the left side becomes the identity matrix.

The right side then represents \(A^{-1}\).

## 3. Detailed Step-by-Step Solution

Start with the augmented matrix:

\[
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
1 & 0 & 1 & 0 & 0 & 1
\end{array}
\right]
\]

**Step 1:** Eliminate the first element of the third row.

\[
R_3 \rightarrow R_3-R_1
\]

\[
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & -1 & 1 & -1 & 0 & 1
\end{array}
\right]
\]

**Step 2:** Eliminate the second element of the third row.

\[
R_3 \rightarrow R_3+R_2
\]

\[
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 2 & -1 & 1 & 1
\end{array}
\right]
\]

**Step 3:** Make the third pivot equal to 1.

\[
R_3 \rightarrow \frac{1}{2}R_3
\]

\[
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & -\frac12 & \frac12 & \frac12
\end{array}
\right]
\]

**Step 4:** Eliminate the third element of the second row.

\[
R_2 \rightarrow R_2-R_3
\]

\[
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & -\frac12 & \frac12 & \frac12
\end{array}
\right]
\]

**Step 5:** Eliminate the second element of the first row.

\[
R_1 \rightarrow R_1-R_2
\]

\[
\left[
\begin{array}{ccc|ccc}
1 & 0 & 0 & \frac12 & -\frac12 & \frac12 \\
0 & 1 & 0 & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & -\frac12 & \frac12 & \frac12
\end{array}
\right]
\]

Therefore,

\[
\boxed{
A^{-1} =
\begin{pmatrix}
\frac12 & -\frac12 & \frac12 \\
\frac12 & \frac12 & -\frac12 \\
-\frac12 & \frac12 & \frac12
\end{pmatrix}
}
\]

## 4. Verification and Consistency Checks

Multiply the original matrix by its inverse:

\[
AA^{-1} =
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac12 & -\frac12 & \frac12 \\
\frac12 & \frac12 & -\frac12 \\
-\frac12 & \frac12 & \frac12
\end{pmatrix}
\]

Calculating each row gives

\[
AA^{-1} =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
=I
\]

The result confirms that the inverse is correct.
