# Exercise 13. A Recurrence Written in Matrix Form

## Question

Let

$$F=\begin{pmatrix}1&1\\1&0\end{pmatrix}.$$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence

$$0,1,1,2,3,5,8,\ldots$$

and describe the relationship you observe. Then compute

$$F\begin{pmatrix}a\\b\end{pmatrix}$$

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

## Solution

**Computing $F^2$ (row by column).**

$$F^2=\begin{pmatrix}1&1\\1&0\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}
=\begin{pmatrix}1\cdot1+1\cdot1&1\cdot1+1\cdot0\\1\cdot1+0\cdot1&1\cdot1+0\cdot0\end{pmatrix}
=\begin{pmatrix}2&1\\1&1\end{pmatrix}.$$

**A reusable update for later powers.** To get $F^{k+1}=F^kF$, we multiply each row of $F^k$ on the right by $F$. A row $(u,v)$ becomes

$$(u,\ v)\begin{pmatrix}1&1\\1&0\end{pmatrix}=(u\cdot1+v\cdot1,\ u\cdot1+v\cdot0)=(u+v,\ u).$$

So the new row is (sum of the two entries, old first entry).

*Example transition $F^2\to F^3$.* The rows of $F^2$ are $(2,1)$ and $(1,1)$:

$$(2,1)\mapsto(2+1,\ 2)=(3,2),\qquad (1,1)\mapsto(1+1,\ 1)=(2,1),$$

hence $F^3=\begin{pmatrix}3&2\\2&1\end{pmatrix}$.

**The remaining powers (same update).**

$$F^4:\ (3,2)\mapsto(5,3),\ (2,1)\mapsto(3,2)\ \Rightarrow\ F^4=\begin{pmatrix}5&3\\3&2\end{pmatrix},$$

$$F^5:\ (5,3)\mapsto(8,5),\ (3,2)\mapsto(5,3)\ \Rightarrow\ F^5=\begin{pmatrix}8&5\\5&3\end{pmatrix}.$$

**Relationship with the Fibonacci numbers.** With $F_0=0,\ F_1=1,\ F_2=1,\ F_3=2,\ F_4=3,\ F_5=5,\ F_6=8,\dots$ the computed powers have the form

$$F^n=\begin{pmatrix}F_{n+1}&F_n\\F_n&F_{n-1}\end{pmatrix}.$$

For instance, $F^5=\begin{pmatrix}8&5\\5&3\end{pmatrix}=\begin{pmatrix}F_6&F_5\\F_5&F_4\end{pmatrix}$, and $F^1=F=\begin{pmatrix}F_2&F_1\\F_1&F_0\end{pmatrix}$. The entries of the powers of $F$ are exactly consecutive Fibonacci numbers. (We observe this pattern from the computed cases; a separate proof of the general formula is not required here.)

**One recurrence step.**

$$F\begin{pmatrix}a\\b\end{pmatrix}=\begin{pmatrix}1\cdot a+1\cdot b\\1\cdot a+0\cdot b\end{pmatrix}=\begin{pmatrix}a+b\\a\end{pmatrix}.$$

If $a$ and $b$ are two consecutive terms, $a=F_{k+1}$ and $b=F_k$, then the first component $a+b=F_{k+2}$ is the next term (the sum of the two consecutive terms), and the second component keeps $a=F_{k+1}$ for the next step. So

$$F\begin{pmatrix}F_{k+1}\\F_k\end{pmatrix}=\begin{pmatrix}F_{k+2}\\F_{k+1}\end{pmatrix},$$

and each multiplication by $F$ moves the pair of consecutive terms one position forward.
