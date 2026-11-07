# Exercise 8. Row Operations and Their Reversibility

## Question

For

$$A=\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}$$

perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Solution

**Step 1: $R_2\leftarrow R_2-2R_1$.** Only row 2 changes: $(2,4,1)-2(1,2,-1)=(0,0,3)$.

$$\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}\longrightarrow\begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix}.$$

**Step 2: $R_3\leftarrow R_3+R_1$.** Only row 3 changes: $(-1,1,3)+(1,2,-1)=(0,3,2)$.

$$\begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix}\longrightarrow\begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix}.$$

**Step 3: $R_2\leftrightarrow R_3$.** Rows 2 and 3 exchange places; row 1 is untouched.

$$\begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix}\longrightarrow\begin{pmatrix}1&2&-1\\0&3&2\\0&0&3\end{pmatrix}.$$

**Inverse operations.**

| Operation | Rows that change | Inverse operation |
|---|---|---|
| $R_2\leftarrow R_2-2R_1$ | $R_2$ | $R_2\leftarrow R_2+2R_1$ |
| $R_3\leftarrow R_3+R_1$ | $R_3$ | $R_3\leftarrow R_3-R_1$ |
| $R_2\leftrightarrow R_3$ | $R_2,R_3$ | $R_2\leftrightarrow R_3$ (the same swap) |

**Why they restore the rows.** Each operation changes one row only by adding a multiple of a *different* row, and row 1 is never altered. So the amount that was subtracted (or added) is still available and can be added back (or subtracted). A swap is undone by swapping again.

**Verification.** Undo the steps in reverse order, starting from the last matrix:

- swap $R_2,R_3$: $\begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix}$;
- $R_3\leftarrow R_3-R_1$: $(0,3,2)-(1,2,-1)=(-1,1,3)$, giving $\begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix}$;
- $R_2\leftarrow R_2+2R_1$: $(0,0,3)+(2,4,-2)=(2,4,1)$, giving $\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}=A$.

The original matrix is recovered, so every row operation is reversible.
