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
