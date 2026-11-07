# Exercise 3. When Can Matrices Be Multiplied?

## Question

The matrix sizes are

$$A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.$$

For the products

$$AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Solution

**Method.** A product $XY$ of an $m\times n$ matrix $X$ and a $p\times q$ matrix $Y$ is defined exactly when the number of columns of $X$ equals the number of rows of $Y$, that is, $n=p$. In that case the result has size $m\times q$ (rows of $X$, columns of $Y$). So for each product we compare the *second* number of the left factor with the *first* number of the right factor.

| Product | Sizes | Inner numbers | Defined? | Size of result |
|---|---|---|---|---|
| $AB$ | $2\times3$ and $3\times4$ | $3=3$ | yes | $2\times4$ |
| $BA$ | $3\times4$ and $2\times3$ | $4\neq2$ | no | — |
| $BC$ | $3\times4$ and $4\times2$ | $4=4$ | yes | $3\times2$ |
| $CB$ | $4\times2$ and $3\times4$ | $2\neq3$ | no | — |
| $AC$ | $2\times3$ and $4\times2$ | $3\neq4$ | no | — |
| $CA$ | $4\times2$ and $2\times3$ | $2=2$ | yes | $4\times3$ |
| $AD$ | $2\times3$ and $2\times2$ | $3\neq2$ | no | — |
| $DA$ | $2\times2$ and $2\times3$ | $2=2$ | yes | $2\times3$ |

**Justification of each decision.**

- $AB$: $A$ has 3 columns and $B$ has 3 rows, so the product is defined; the result has the rows of $A$ and the columns of $B$, i.e. $2\times4$.
- $BA$: $B$ has 4 columns but $A$ has only 2 rows, so the entries of a row of $B$ cannot be paired with the entries of a column of $A$. Not defined.
- $BC$: $B$ has 4 columns and $C$ has 4 rows, so it is defined, with size $3\times2$.
- $CB$: $C$ has 2 columns but $B$ has 3 rows. Not defined.
- $AC$: $A$ has 3 columns but $C$ has 4 rows. Not defined.
- $CA$: $C$ has 2 columns and $A$ has 2 rows, so it is defined, with size $4\times3$.
- $AD$: $A$ has 3 columns but $D$ has 2 rows. Not defined.
- $DA$: $D$ has 2 columns and $A$ has 2 rows, so it is defined, with size $2\times3$.

**Conclusion.** The defined products are $AB\ (2\times4)$, $BC\ (3\times2)$, $CA\ (4\times3)$ and $DA\ (2\times3)$. The other four are not defined. Note that $AB$ is defined while $BA$ is not, which already shows that matrix multiplication cannot be commutative in general.
