From https://inst.eecs.berkeley.edu/~ee127/sp21/livebook/def_pseudo_inv.html

$A$ is a $m$ x $n$ matrix

$$\begin{eqnarray}
A &amp;=&amp;
U
\left[ \begin{array}{cc}
S &amp; 0 \\
0 &amp; 0
\end{array} \right]&nbsp;V^T\\
A^\dagger &amp;=&amp;
V
\left[ \begin{array}{cc}
S^{-1} &amp; 0 \\
0 &amp; 0
\end{array} \right]&nbsp;U^T\\
\end{eqnarray} $$

If $rank(A)$ = $n \leq m$ then $A$ is full column rank
so
$A^TA$ is not singular
and $A^\dagger$ is a left inverse of $A$
as $A^{\dagger}A = I_n$

$A^{\dagger} = (A^TA)^{-1}A^T$

If $rank(A)$ = $m \leq n$ then $A$ is full row rank
so
$AA^T$ is not singular
and $A^\dagger$ is a right inverse of $A$
as $AA^{\dagger} = I_m$

$A^{\dagger} = A^T(AA^T)^{-1}$

If $m = n$ and $A$ is invertible, then $A^{\dagger} = A^{-1}$
