# Exercise 3. When Can Matrices Be Multiplied?

## Solution

The matrix sizes are

$$
A_{2\times 3},\qquad B_{3\times 4},\qquad C_{4\times 2},\qquad D_{2\times 2}.
$$

**Dimension compatibility condition:** the product $XY$ of an $m\times n$ matrix $X$ and a $p\times q$ matrix $Y$ is defined if and only if $n=p$ (the number of columns of $X$ equals the number of rows of $Y$). If it is defined, the result has size $m\times q$.

### $AB$

$A_{2\times 3}\cdot B_{3\times 4}$: columns of $A$ $=3$, rows of $B$ $=3$. Since $3=3$, the product is **defined**, and $AB$ is $2\times 4$.

### $BA$

$B_{3\times 4}\cdot A_{2\times 3}$: columns of $B$ $=4$, rows of $A$ $=2$. Since $4\neq 2$, the product is **not defined**.

### $BC$

$B_{3\times 4}\cdot C_{4\times 2}$: columns of $B$ $=4$, rows of $C$ $=4$. Since $4=4$, the product is **defined**, and $BC$ is $3\times 2$.

### $CB$

$C_{4\times 2}\cdot B_{3\times 4}$: columns of $C$ $=2$, rows of $B$ $=3$. Since $2\neq 3$, the product is **not defined**.

### $AC$

$A_{2\times 3}\cdot C_{4\times 2}$: columns of $A$ $=3$, rows of $C$ $=4$. Since $3\neq 4$, the product is **not defined**.

### $CA$

$C_{4\times 2}\cdot A_{2\times 3}$: columns of $C$ $=2$, rows of $A$ $=2$. Since $2=2$, the product is **defined**, and $CA$ is $4\times 3$.

### $AD$

$A_{2\times 3}\cdot D_{2\times 2}$: columns of $A$ $=3$, rows of $D$ $=2$. Since $3\neq 2$, the product is **not defined**.

### $DA$

$D_{2\times 2}\cdot A_{2\times 3}$: columns of $D$ $=2$, rows of $A$ $=2$. Since $2=2$, the product is **defined**, and $DA$ is $2\times 3$.

## Answer

| Product | Sizes | Condition | Defined? | Size of result |
|:-------:|:-----:|:---------:|:--------:|:--------------:|
| $AB$ | $2\times 3$ and $3\times 4$ | $3=3$ | Yes | $2\times 4$ |
| $BA$ | $3\times 4$ and $2\times 3$ | $4\neq 2$ | No | — |
| $BC$ | $3\times 4$ and $4\times 2$ | $4=4$ | Yes | $3\times 2$ |
| $CB$ | $4\times 2$ and $3\times 4$ | $2\neq 3$ | No | — |
| $AC$ | $2\times 3$ and $4\times 2$ | $3\neq 4$ | No | — |
| $CA$ | $4\times 2$ and $2\times 3$ | $2=2$ | Yes | $4\times 3$ |
| $AD$ | $2\times 3$ and $2\times 2$ | $3\neq 2$ | No | — |
| $DA$ | $2\times 2$ and $2\times 3$ | $2=2$ | Yes | $2\times 3$ |
