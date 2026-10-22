# Exercise 3. When Can Matrices Be Multiplied?

## Question

The matrices have the following sizes:

$$
A:\ 2\times 3, \qquad B:\ 3\times 4, \qquad C:\ 4\times 2, \qquad D:\ 2\times 2
$$

For each of the products $AB$, $BA$, $BC$, $CB$, $AC$, $CA$, $AD$ and $DA$, determine whether it is defined. If it is defined, state the size of the result. Justify each decision using the dimension compatibility condition.

## Solution

### Method

The dimension compatibility condition says that a product $XY$ is defined exactly when the number of columns of $X$ equals the number of rows of $Y$. If $X$ is $m\times n$ and $Y$ is $n\times p$, then $XY$ is defined and has size $m\times p$. If the two inner numbers differ, the rows of $X$ and the columns of $Y$ have different lengths, so the row-by-column sums cannot be formed and the product is undefined.

### Checking each product

**$AB$:** $A$ is $2\times 3$ and $B$ is $3\times 4$. The inner numbers are $3$ and $3$, which are equal. So $AB$ is defined and its size is $2\times 4$.

**$BA$:** $B$ is $3\times 4$ and $A$ is $2\times 3$. The inner numbers are $4$ and $2$, which differ. So $BA$ is not defined.

**$BC$:** $B$ is $3\times 4$ and $C$ is $4\times 2$. The inner numbers are $4$ and $4$, which are equal. So $BC$ is defined and its size is $3\times 2$.

**$CB$:** $C$ is $4\times 2$ and $B$ is $3\times 4$. The inner numbers are $2$ and $3$, which differ. So $CB$ is not defined.

**$AC$:** $A$ is $2\times 3$ and $C$ is $4\times 2$. The inner numbers are $3$ and $4$, which differ. So $AC$ is not defined.

**$CA$:** $C$ is $4\times 2$ and $A$ is $2\times 3$. The inner numbers are $2$ and $2$, which are equal. So $CA$ is defined and its size is $4\times 3$.

**$AD$:** $A$ is $2\times 3$ and $D$ is $2\times 2$. The inner numbers are $3$ and $2$, which differ. So $AD$ is not defined.

**$DA$:** $D$ is $2\times 2$ and $A$ is $2\times 3$. The inner numbers are $2$ and $2$, which are equal. So $DA$ is defined and its size is $2\times 3$.

### Summary

| Product | Sizes | Inner numbers | Defined? | Result size |
|:-------:|:-----:|:-------------:|:--------:|:-----------:|
| $AB$ | $2\times 3$ and $3\times 4$ | $3 = 3$ | Yes | $2\times 4$ |
| $BA$ | $3\times 4$ and $2\times 3$ | $4 \neq 2$ | No | none |
| $BC$ | $3\times 4$ and $4\times 2$ | $4 = 4$ | Yes | $3\times 2$ |
| $CB$ | $4\times 2$ and $3\times 4$ | $2 \neq 3$ | No | none |
| $AC$ | $2\times 3$ and $4\times 2$ | $3 \neq 4$ | No | none |
| $CA$ | $4\times 2$ and $2\times 3$ | $2 = 2$ | Yes | $4\times 3$ |
| $AD$ | $2\times 3$ and $2\times 2$ | $3 \neq 2$ | No | none |
| $DA$ | $2\times 2$ and $2\times 3$ | $2 = 2$ | Yes | $2\times 3$ |

Four of the eight products are defined: $AB$, $BC$, $CA$ and $DA$. In each pair $XY$ and $YX$ above, at most one order is defined here, which shows that matrix multiplication depends on the order of the factors.
