Here we will define a fundamental solution for the Laplace operator in any open set. This is known as the greens function. This function will represent a potential due to a unit charge placed at a point $x\in\Omega$ and equal to zero on $\partial\Omega$. such a function $G(x,y)$ satisfies 
$$\begin{cases} 
  \Delta_{y}G(x,y)=-\delta_x & x\in\Omega \\
  G(x,\sigma)=0, & \sigma\in\partial\Omega
  \end{cases} \\
$$
More explicitly, the greens function can be written in the form
$$G(x,y)=\Phi(x-y)-\varphi(x,y)$$
where $\varphi$ solves
$$
\begin{cases}
  \Delta_{y}\varphi=0  & x\in\Omega \\
  \varphi(x,\sigma)=\Phi(x-\sigma)  & \sigma\in\partial\Omega\\
\end{cases}
$$

## The Method of electrostatic images
in this method $\varphi(x,\cdot)$ is considered the potential due to a imaginary charge q and the point $x^*$, the image of x, in the complement of $\Omega$. The charge q and the point $x^*$ have to be chosen so that $\varphi(x,\cdot)$ on $\partial\Omega$ is equal to the potential created by the unit charge in x.

## Example: upper half plane
Let $\mathbb{R}_+^3=\{(x_1,x_2,x_3):x_3>0\}$
Fix $x=(x_1,x_2,x_3)$  and observe that if we choose $x^*=(x_1,x_2,-x_3)$  then, on $y_3=0$ we have $|x^*-y|=|x-y|$
Thus, if $x\in\mathbb{R}_+^3$, $x^*$ belongs to the complement of $\mathbb{R}_+^3$ , the function $\varphi(x,y)=\Phi(x^*-y)=\frac{1}{4\pi|x^*-y|}$ is harmonic in our domain and $\varphi(x,y)=\Phi(x-y)$ on the plane $y_3=0$ 
therefore our greens function is
$$G(x,y)=\frac{1}{4\pi|x-y|}-\frac{1}{4\pi|x^*-y|}$$
