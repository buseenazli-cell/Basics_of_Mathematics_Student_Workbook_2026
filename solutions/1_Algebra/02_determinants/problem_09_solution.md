# Problem Statement

The vectors 

$$u=\begin{pmatrix}3\\1\end{pmatrix},\qquad v=\begin{pmatrix}1\\4\end{pmatrix}$$ 

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

---

## Solution

### 1. Computation of Area using Determinant

The geometric area of a parallelogram spanned by two 2D vectors $u$ and $v$ is given by the absolute value of the determinant of the matrix formed by placing the vectors as its columns (or rows):

$$\text{Area} = \left| \det \begin{pmatrix} u & v \end{pmatrix} \right|$$

Constructing the matrix $M_1 = \begin{pmatrix} u & v \end{pmatrix} = \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix}$:

$$\det(M_1) = \det \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix} = (3)(4) - (1)(1) = 12 - 1 = 11$$

Taking the absolute value gives the geometric area:

$$\text{Area} = |\det(M_1)| = |11| = 11$$

---

### 2. Reversing the Order of Vectors

Now, we reverse the order of the vectors to construct matrix $M_2 = \begin{pmatrix} v & u \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix}$.

Computing its determinant:

$$\det(M_2) = \det \begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix} = (1)(1) - (3)(4) = 1 - 12 = -11$$

Computing the geometric area with the reversed order:

$$\text{Area} = |\det(M_2)| = |-11| = 11$$

---

### 3. Explanation of What Changes and What Does Not

* **What Changes in the Determinant:**  
  The **sign of the determinant** changes from $+11$ to $-11$. This occurs because swapping two columns of a matrix multiplies its determinant by $-1$. Mathematically and geometrically, the signed determinant encodes the **orientation (handedness)** of the vector pair:
  * $\det(u, v) = +11 > 0$ indicates that turning from $u$ to $v$ follows a **counterclockwise** direction (a standard positive/right-handed orientation).
  * $\det(v, u) = -11 < 0$ indicates that turning from $v$ to $u$ follows a **clockwise** direction (a negative orientation).

* **What Does Not Change in the Area:**  
  The **magnitude (geometric area)** remains strictly unchanged ($\text{Area} = 11$). Area is a physical magnitude representing spatial region coverage and is inherently non-negative. Because area is calculated using the absolute value of the determinant ($\text{Area} = |\det M|$), reversing the order of the spanning vectors alters only the directional orientation sign while leaving the absolute physical size of the parallelogram invariant.
