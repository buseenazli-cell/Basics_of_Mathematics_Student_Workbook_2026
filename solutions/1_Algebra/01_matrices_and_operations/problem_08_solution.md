# Exercise 8. Elementary Row Operations and Their Inverses

## Question

Let

$$
A = \begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}
$$

Perform, in order:

1. $R_2 \leftarrow R_2 - 2R_1$,
2. $R_3 \leftarrow R_3 + R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Solution

### Method

An elementary row operation changes one or two rows and leaves the others untouched. In operations 1 and 2 below, a multiple of one row is added to another row, so the entries are updated one by one in the row being changed.

### Step 1: $R_2 \leftarrow R_2 - 2R_1$

Only row 2 changes. Row 1 is $(1, 2, -1)$, so $2R_1 = (2, 4, -2)$.

$$
R_2 - 2R_1 = (2 - 2,\; 4 - 4,\; 1 - (-2)) = (0,\; 0,\; 3)
$$

$$
A_1 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}
$$

### Step 2: $R_3 \leftarrow R_3 + R_1$

Only row 3 changes. Row 1 is still $(1, 2, -1)$.

$$
R_3 + R_1 = (-1 + 1,\; 1 + 2,\; 3 + (-1)) = (0,\; 3,\; 2)
$$

$$
A_2 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}
$$

### Step 3: interchange $R_2$ and $R_3$

Rows 2 and 3 trade places. Row 1 is unchanged.

$$
A_3 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}
$$

The final matrix is upper triangular.

### Inverse operations

| Operation | Rows that change | Inverse operation |
|:---------:|:----------------:|:-----------------:|
| $R_2 \leftarrow R_2 - 2R_1$ | row 2 | $R_2 \leftarrow R_2 + 2R_1$ |
| $R_3 \leftarrow R_3 + R_1$ | row 3 | $R_3 \leftarrow R_3 - R_1$ |
| interchange $R_2$ and $R_3$ | rows 2 and 3 | interchange $R_2$ and $R_3$ again |

**Why they work.**

- In operation 1, row 2 became $R_2 - 2R_1$ while row 1 stayed the same. Adding $2R_1$ to the new row 2 gives $(R_2 - 2R_1) + 2R_1 = R_2$, the original row. This works because row 1 was not changed, so it is still available to add back.
- In operation 2, row 3 became $R_3 + R_1$ while row 1 stayed the same. Subtracting $R_1$ gives $(R_3 + R_1) - R_1 = R_3$.
- Swapping two rows twice puts each row back where it started.

### Undoing the whole sequence

To undo all three steps, apply the inverse operations in the reverse order: first undo step 3, then step 2, then step 1.

Undo step 3 (swap $R_2$ and $R_3$ of $A_3$):

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix} = A_2
$$

Undo step 2 ($R_3 \leftarrow R_3 - R_1$): the new row 3 is $(0 - 1,\; 3 - 2,\; 2 - (-1)) = (-1, 1, 3)$.

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix} = A_1
$$

Undo step 1 ($R_2 \leftarrow R_2 + 2R_1$): the new row 2 is $(0 + 2,\; 0 + 4,\; 3 + (-2)) = (2, 4, 1)$.

$$
\begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix} = A
$$

We are back at the original matrix $A$.

### Conclusion

$$
A \;\to\; A_1 \;\to\; A_2 \;\to\; A_3 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}
$$

Each operation has an inverse operation, and applying the inverses in reverse order returns $A_3$ to $A$.
