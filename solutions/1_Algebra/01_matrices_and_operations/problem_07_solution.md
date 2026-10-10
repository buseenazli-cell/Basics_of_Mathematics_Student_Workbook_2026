# Elementary Row Operations

Let

$$
A=\begin{pmatrix}1&2&-1\\2&4&1\\-1&1&3\end{pmatrix}
$$

Perform, in order:

1. $R_2 \leftarrow R_2 - 2R_1$
2. $R_3 \leftarrow R_3 + R_1$
3. $R_2 \leftrightarrow R_3$

## Step-by-step solution

### Step 1: $R_2 \leftarrow R_2 - 2R_1$

$(2,4,1) - 2(1,2,-1) = (0,0,3)$

$$
\begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix}
$$

### Step 2: $R_3 \leftarrow R_3 + R_1$

$(-1,1,3) + (1,2,-1) = (0,3,2)$

$$
\begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix}
$$

### Step 3: $R_2 \leftrightarrow R_3$

$$
\begin{pmatrix}1&2&-1\\0&3&2\\0&0&3\end{pmatrix}
$$

## Summary

$$
A \;\xrightarrow{R_2 \leftarrow R_2-2R_1}\;
\begin{pmatrix}1&2&-1\\0&0&3\\-1&1&3\end{pmatrix}
$$

$$
\xrightarrow{R_3 \leftarrow R_3+R_1}\;
\begin{pmatrix}1&2&-1\\0&0&3\\0&3&2\end{pmatrix}
$$

$$
\xrightarrow{R_2 \leftrightarrow R_3}\;
\begin{pmatrix}1&2&-1\\0&3&2\\0&0&3\end{pmatrix}
$$

## Inverse operations

| Step | Operation | Inverse operation |
|:---:|:---:|:---:|
| 1 | $R_2 \leftarrow R_2 - 2R_1$ | $R_2 \leftarrow R_2 + 2R_1$ |
| 2 | $R_3 \leftarrow R_3 + R_1$ | $R_3 \leftarrow R_3 - R_1$ |
| 3 | $R_2 \leftrightarrow R_3$ | $R_2 \leftrightarrow R_3$ (self-inverse) |

> To undo the whole sequence, apply the inverses in **reverse order**: 3 → 2 → 1.
