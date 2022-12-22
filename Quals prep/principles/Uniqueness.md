#pde #salsa #hagstrom 
#### Uniqueness of Diffusion equation
For the following we will show that solutions are unique using the energy method. 
![[Diffusion Equation#prototypical diffusion problem]]

## Proof of uniqueness for diffusion problem
Suppose $u$ and $v$ are solutions of the diffusion problem sharing the same boundary conditions, and let $w=u-v$; we want to show that $w\equiv 0$. First observe
$$\begin{cases}
&w_t-D\Delta w = 0 & x\in Q_t=\Omega\times(0,T)\\
&w(\mathbf{x},0)=0 & x\in \bar{\Omega}\\
&+\text{B.C.} = 0 & x\in \partial\Omega\times (0,T]\\
\end{cases}
$$
Multiply the equation by $w$ and integrate on $\Omega$
$$\int_\Omega ww_t\;dx = D\int_\Omega w \Delta w \; dx$$
notice, 
$$\int_\Omega ww_t\;dx = \frac{1}{2}\frac{d}{dt}\int_\Omega w^2\; dx$$
Now from greens identity ($u=v=w$)
$$\int_\Omega w\Delta w\;dx = \int_{\partial\Omega}\partial_\nu w\;d\sigma - \int_\Omega |\nabla w|^2 dx$$
Let  $$E(t)=\int_\Omega w^2\;dx$$
From the previous integrals it follows that
$$\frac{1}{2}E'(t)= D \int_{\partial\Omega}\partial_\nu w\; d\sigma - D\int_\Omega |\nabla w |^2\; dx$$
Given any of the boundary conditions the first term of the r.h.s is non positive and the second term is a norm which is sign definite. Therefore $E'(t)\le 0 \;\;\text{and}\;\;E(0)=0$ which implies that $w(x,t)\equiv 0$ in $\Omega$ for every $t>0$. Thus $u=v$ and solutions are unique belonging to $C^{2,1}(\bar{Q}_T)$. 
