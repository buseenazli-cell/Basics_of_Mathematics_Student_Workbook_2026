# Exercise 11

## Question

Let

$$
A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} a & b \\ c & d \end{pmatrix}
$$

Find all matrices $B$ that commute with $A$, that is, all $B$ with $AB = BA$.

## Solution

### Method

We compute $AB$ and $BA$ by pairing rows with columns. Two matrices are equal exactly when all corresponding entries are equal, so we set each entry of $AB$ equal to the matching entry of $BA$ and solve for $a, b, c, d$.

### The two products

$$
AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} a & b \\ c & d \end{pmatrix}
= \begin{pmatrix} a + c & b + d \\ c & d \end{pmatrix}
$$

For example, $(AB)_{11} = 1\cdot a + 1\cdot c = a + c$.

$$
BA = \begin{pmatrix} a & b \\ c & d \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
= \begin{pmatrix} a & a + b \\ c & c + d \end{pmatrix}
$$

For example, $(BA)_{12} = a\cdot 1 + b\cdot 1 = a + b$.

### Comparing entries

| Entry | $AB$ | $BA$ | Condition |
|:-----:|:----:|:----:|:---------:|
| (1,1) | $a + c$ | $a$ | $c = 0$ |
| (1,2) | $b + d$ | $a + b$ | $d = a$ |
| (2,1) | $c$ | $c$ | none |
| (2,2) | $d$ | $c + d$ | $c = 0$ |

From the (1,1) entry, $a + c = a$ gives $c = 0$. From the (1,2) entry, $b + d = a + b$ gives $d = a$. The other two entries give no new condition or repeat $c = 0$.

### Answer

The parameters $a$ and $b$ are arbitrary, and

$$
B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}
$$

These are exactly the matrices commuting with $A$.
