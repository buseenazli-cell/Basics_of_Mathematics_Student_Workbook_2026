# Exercise 12. Formula for a Matrix Power

## Question

Let

$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix}.$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

## Solution

**Computing the powers.** Each power is obtained by multiplying the previous one by $A$:

$$A^2=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1\cdot1+1\cdot0&1\cdot1+1\cdot1\\0\cdot1+1\cdot0&0\cdot1+1\cdot1\end{pmatrix}=\begin{pmatrix}1&2\\0&1\end{pmatrix},$$

$$A^3=A^2A=\begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1&1+2\\0&1\end{pmatrix}=\begin{pmatrix}1&3\\0&1\end{pmatrix},$$

$$A^4=A^3A=\begin{pmatrix}1&3\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}=\begin{pmatrix}1&1+3\\0&1\end{pmatrix}=\begin{pmatrix}1&4\\0&1\end{pmatrix}.$$

**Conjecture.** The diagonal entries stay $1$, the lower-left entry stays $0$, and the upper-right entry equals the exponent:

$$A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}\qquad(n\ge1).$$

**Proof by induction.**

*Base case.* For $n=1$ the formula gives $\begin{pmatrix}1&1\\0&1\end{pmatrix}=A$, which is true.

*Inductive step.* Assume the formula holds for some $n$, i.e. $A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}$. Then

$$A^{n+1}=A^nA=\begin{pmatrix}1&n\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}
=\begin{pmatrix}1\cdot1+n\cdot0&1\cdot1+n\cdot1\\0\cdot1+1\cdot0&0\cdot1+1\cdot1\end{pmatrix}
=\begin{pmatrix}1&n+1\\0&1\end{pmatrix}.$$

This is exactly the formula with $n$ replaced by $n+1$. The calculation did not use any specific value of $n$, so it works for every $n$.

**Conclusion.** The formula holds at $n=1$, and the inductive step carries every case to the next one ($n=1\Rightarrow n=2\Rightarrow n=3\Rightarrow\cdots$). Hence, by induction, $A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}$ holds for every integer $n\ge1$.
