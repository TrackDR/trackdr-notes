# Align two 3D vectors using Euler Angles 

Euler Angles: $$\alpha_x,\alpha_y,\alpha_z$$

Assume there are&nbsp;two 3D vectors $p$ and $q$ and $p$ needs to be aligned (point in the same direction as) to $q$.

First, let's extract the&nbsp;<strong>axis-angle representation</strong> $k$ and $\theta$:

$$
\begin{eqnarray}
k &amp;=&amp; p \times q \\
k &amp;=&amp; \frac{k}{||k||} \\
p &amp;=&amp; \frac{p}{||p||} \\
q &amp;=&amp; \frac{q}{||q||} \\
\theta &amp;=&amp; cos^{-1}(p \cdot q)
\end{eqnarray} $$

Convert axis-angle ($k$ and $\theta$) to a matrix $R$

$$\begin{eqnarray}
K &amp;=&amp;
\left[ \begin{array}{ccc}
0 &amp; k(3) &amp; k(2) \\
k(3) &amp; 0 &amp; -k(1) \\
-k(2) &amp; k(1) &amp; 0
\end{array} \right]&nbsp;\\
R &amp;=&amp; e^{\theta K} \\
R &amp;=&amp; I +sin(\theta)K + (1-cos(\theta))K^2
\end{eqnarray} $$

Convert matrix $R$ to Euler angles ($\alpha_x,\alpha_y,\alpha_z$)

$$\begin{eqnarray}
\alpha_x &amp;=&amp; atan2(R(3,2), R(3,3)) \\
\alpha_y &amp;=&amp; atan2(-R(3,1), \sqrt{R(3,2)^2 + R(3,3)^2}) \\
\alpha_z &amp;=&amp; atan2(R(2,1), R(1,1))
\end{eqnarray} $$

Verify Results

$$\begin{eqnarray}
M_x &amp;=&amp;
\left[ \begin{array}{ccc}
1 &amp; 0 &amp; 0 \\
0 &amp; cos(\alpha_x) &amp; -sin(\alpha_x) \\
0 &amp; sin(\alpha_x) &amp; cos(\alpha_x)
\end{array} \right]&nbsp;\\
M_y &amp;=&amp;
\left[ \begin{array}{ccc}
cos(\alpha_y) &amp; 0 &amp; sin(\alpha_y) \\
0 &amp; 1 &amp; 0 \\
-sin(\alpha_y) &amp; 0 &amp; cos(\alpha_y)
\end{array} \right]&nbsp;\\
M_z &amp;=&amp;
\left[ \begin{array}{ccc}
cos(\alpha_z) &amp; -sin(\alpha_z) &amp; 0 \\
sin(\alpha_z) &amp; cos(\alpha_z) &amp; 0 \\
0 &amp; 0 &amp; 1
\end{array} \right]&nbsp;\\
p_{rot} &amp;=&amp; M_zM_yM_xp \\
p_{rot} &amp;=&amp; \frac{p_{rot}}{||p_{rot}||} \\
q &amp;=&amp; \frac{q}{||q||} \\
metric &amp;=&amp; atan2(||p_{rot} \times q||, p_{rot} \cdot q)
\end{eqnarray} $$

Metric should be zero.
