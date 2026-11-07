# Exercise 7. Identity Matrix, Zero Matrix, and Powers

## Question

For

$$A=\begin{pmatrix}2&1\\0&2\end{pmatrix}$$

compute

$$AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## Solution

Here $I=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ and $0=\begin{pmatrix}0&0\\0&0\end{pmatrix}$ are the $2\times2$ identity and zero matrices.

**Neutral elements.**

$$AI=\begin{pmatrix}2\cdot1+1\cdot0 & 2\cdot0+1\cdot1\\ 0\cdot1+2\cdot0 & 0\cdot0+2\cdot1\end{pmatrix}=\begin{pmatrix}2&1\\0&2\end{pmatrix}=A,$$

$$IA=\begin{pmatrix}1\cdot2+0\cdot0 & 1\cdot1+0\cdot2\\ 0\cdot2+1\cdot0 & 0\cdot1+1\cdot2\end{pmatrix}=\begin{pmatrix}2&1\\0&2\end{pmatrix}=A,$$

$$A+0=\begin{pmatrix}2+0&1+0\\0+0&2+0\end{pmatrix}=A.$$

**Roles.** $I$ is the neutral element of multiplication: multiplying by $I$ on either side changes nothing, just as $1\cdot a=a$ for numbers. $0$ is the neutral element of addition: adding it changes nothing, just as $a+0=a$.

**Powers.**

$$A^2=A\cdot A=\begin{pmatrix}2\cdot2+1\cdot0 & 2\cdot1+1\cdot2\\ 0\cdot2+2\cdot0 & 0\cdot1+2\cdot2\end{pmatrix}=\begin{pmatrix}4&4\\0&4\end{pmatrix},$$

$$A^3=A^2\cdot A=\begin{pmatrix}4\cdot2+4\cdot0 & 4\cdot1+4\cdot2\\ 0\cdot2+4\cdot0 & 0\cdot1+4\cdot2\end{pmatrix}=\begin{pmatrix}8&12\\0&8\end{pmatrix}.$$

**Pattern.** The diagonal entries are $2,4,8$, i.e. $2^n$. The upper-right entries are $1,4,12$, i.e. $n\cdot2^{n-1}$ (check: $1\cdot1,\ 2\cdot2,\ 3\cdot4$). So we observe

$$A^n=\begin{pmatrix}2^n & n\,2^{n-1}\\ 0 & 2^n\end{pmatrix}.$$

**How the pattern arises.** Write $A=2I+N$ with $N=\begin{pmatrix}0&1\\0&0\end{pmatrix}$. Then

$$N^2=\begin{pmatrix}0\cdot0+1\cdot0 & 0\cdot1+1\cdot0\\0&0\end{pmatrix}=0.$$

Because $2I$ commutes with $N$, the binomial expansion is valid and all terms with $N^2$ or higher vanish:

$$A^n=(2I+N)^n=2^nI+n\,2^{n-1}N,$$

which is exactly the matrix above. For instance, $A^3=8I+3\cdot4\,N=\begin{pmatrix}8&12\\0&8\end{pmatrix}$, matching the direct computation.
