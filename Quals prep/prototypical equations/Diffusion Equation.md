This is a linear second order partial differential equation.

$$u_t - D\Delta u=f$$
When $f\equiv 0$ the equation is said to be homogeneous and in this case the [[Superposition principle]] holds. Diffusion can be used to model the dicipation of heat but more generally it is used to discribe the transport of a substance due to the molecular motion of the surrounding medium. The differential operator $\partial_t - D\Delta$  measures the instantaneous density produciton rate throughout our domain. A homogeneous diffusion equation coresponds to no forcing function within our domain. Therefore there shall be no density production rate in our domain. Suppose however we hold a candle near a thin metal plate. This would be an example of density production on the surface of the material. Such a system corisponds to a diffusion equation with a non-zero forcing term.  For this equation to be a [[Well Posed Problem]] we must include additional information such as [[Boundary conditions]] and prescribed initial conditions
($u(x,0)=g(x)$). 

![[Boundary conditions]]

#### prototypical diffusion problem
 given $\Omega\subset\mathbb{R}^n$
$$\begin{cases}
&u_t-D\Delta u = f(x,t)\;\;\;&x\in\Omega_T\\
&u(x,0) = g(x)&x\in\bar{\Omega}\\
&+ \text{boundary conditions} &x\in\partial\Omega\times(0,T]\\
\end{cases}$$
## Global Cauchy Problem (n=1)
$$
\begin{cases}
	&u_t-D u_{xx} = 0 &x\in\mathbb{R}\times(0,\infty)\\
	&u(x,0)=g(x) &x\in\mathbb{R}\\
\end{cases}
$$
This problem models the evolution of the temperature along a very long bar given the initial temperature distribution $g(x)$. 

recall what we know from the fundamental solution of the following
![[Fundamental Solutions#Fundamental Solution (n>1)]]
Where the fundamental solution is considered a unit source solution. Accordingly
$$\Gamma_D(x-y,t)g(y)dy$$ gives the concentration at x at time t, due to the diffusion of the mass $g(y)dy$. Therefore via the [[Superposition principle]] we can compute the solution as the sum of all contributions. Therefore
$$
u(x,t)=\int_\mathbb{R}g(y)\;\Gamma_D(x-y,t)dy=\frac{1}{\sqrt{4\pi Dt}}\int_{\mathbb{R}}g(y)e^{-\frac{(x-y)^2}{4Dt}}dy
$$

^fa57ce

This is a solution to the global Cauchy problem under a boundedness condition on $g(x)$. We require that $|g(x)|\le ce^{ax^2}\;\;\forall x\in\mathbb{R}$ 

![[Duhamel's Method]]