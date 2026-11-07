# Exercise 11. When Do Matrices Commute?

## Question

Given

$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}a&b\\c&d\end{pmatrix}.$$

Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

## Solution

**Method.** We calculate $AB$ and $BA$ by pairing rows with columns. Two matrices are equal exactly when all their corresponding entries are equal, so we then require each pair of corresponding entries to agree and solve the resulting equations.

**The product $AB$.**

$$AB=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix}=\begin{pmatrix}a+c&b+d\\c&d\end{pmatrix}.$$

For example, $(AB)_{11}=1\cdot a+1\cdot c=a+c$ and $(AB)_{21}=0\cdot a+1\cdot c=c$.

**The product $BA$.**

$$BA=\begin{pmatrix}a&b\\c&d\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}a&a+b\\c&c+d\end{pmatrix}.$$

For example, $(BA)_{12}=a\cdot1+b\cdot1=a+b$ and $(BA)_{22}=c\cdot1+d\cdot1=c+d$.

**Equating entries.**

| Position | $AB$ | $BA$ | Condition |
|---|---|---|---|
| $(1,1)$ | $a+c$ | $a$ | $a+c=a\ \Rightarrow\ c=0$ |
| $(1,2)$ | $b+d$ | $a+b$ | $b+d=a+b\ \Rightarrow\ d=a$ |
| $(2,1)$ | $c$ | $c$ | always true |
| $(2,2)$ | $d$ | $c+d$ | $d=c+d\ \Rightarrow\ c=0$ |

Subtracting $a$ from both sides of $a+c=a$ gives $c=0$. Subtracting $b$ from both sides of $b+d=a+b$ gives $d=a$. The $(2,2)$ condition gives $c=0$ again, so no new information appears.

**Result.** $AB=BA$ if and only if $c=0$ and $d=a$, while $a$ and $b$ are arbitrary. Therefore

$$B=\begin{pmatrix}a&b\\0&a\end{pmatrix},\qquad a,b\in\mathbb{R}\ \text{arbitrary},$$

which can also be written as $B=aI+b\begin{pmatrix}0&1\\0&0\end{pmatrix}$.

**Check.** For $B=\begin{pmatrix}a&b\\0&a\end{pmatrix}$ both products equal $\begin{pmatrix}a&a+b\\0&a\end{pmatrix}$.
