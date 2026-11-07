# Exercise 6. Transpose

## Question

For

$$A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix},\qquad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$(AB)^T=B^TA^T.$$

## Solution

**Transposes.** Transposition turns each row into a column (and each column into a row). For example, the first row $(1,2,3)$ of $A$ becomes the first column of $A^T$. Doing this for every row:

$$A^T=\begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix},\qquad
B^T=\begin{pmatrix}1&2&-1\\0&1&3\end{pmatrix}.$$

**The product $AB$.** $A$ is $2\times3$ and $B$ is $3\times2$, so $AB$ is $2\times2$. Each entry is a row-column sum:

$$\begin{aligned}
(AB)_{11}&=1\cdot1+2\cdot2+3\cdot(-1)=1+4-3=2,\\
(AB)_{12}&=1\cdot0+2\cdot1+3\cdot3=0+2+9=11,\\
(AB)_{21}&=4\cdot1+5\cdot2+6\cdot(-1)=4+10-6=8,\\
(AB)_{22}&=4\cdot0+5\cdot1+6\cdot3=0+5+18=23.
\end{aligned}$$

$$AB=\begin{pmatrix}2&11\\8&23\end{pmatrix},\qquad (AB)^T=\begin{pmatrix}2&8\\11&23\end{pmatrix}.$$

**The product $B^TA^T$.** The identity prescribes the *reversed* order, so we multiply $B^T$ ($2\times3$) by $A^T$ ($3\times2$):

$$\begin{aligned}
(B^TA^T)_{11}&=1\cdot1+2\cdot2+(-1)\cdot3=2, &
(B^TA^T)_{12}&=1\cdot4+2\cdot5+(-1)\cdot6=8,\\
(B^TA^T)_{21}&=0\cdot1+1\cdot2+3\cdot3=11, &
(B^TA^T)_{22}&=0\cdot4+1\cdot5+3\cdot6=23.
\end{aligned}$$

$$B^TA^T=\begin{pmatrix}2&8\\11&23\end{pmatrix}.$$

**Comparison.** Entry by entry, $B^TA^T$ equals $(AB)^T$:

$$(AB)^T=\begin{pmatrix}2&8\\11&23\end{pmatrix}=B^TA^T.$$

So the identity holds in this example. Note that $A^TB^T$ is not even defined here ($3\times2$ times $2\times3$ is defined, but it would be $3\times3$, a different size from $(AB)^T$), which shows why the order must be reversed. This is a check on one example, not a general proof of the theorem.
