#pde #hagstrom #salsa 
$$
\begin{cases}
&w_t-D\Delta w = f(x,t)\;\;\;&x\in\mathbb{R}\times(0,\infty)\\
&w(x,0) = g(x)&x\in\mathbb{R}\\
\end{cases}
$$

This is the global Dirichlet problem whose solution is found by a superposition of solutions from the following two problems 

$$
u(x,t)=\int_\mathbb{R} \Gamma_D(x-y,t)g(y)\;dy + \int_0^t\int_\mathbb{R}\Gamma(x-y,t-s)f(y,s)\;dyds
$$

on the r.h.s the leftmost term is the solution to the Global homogenous Cauchy problem solved by a superposition of the [[Fundamental Solutions|fundamental solution]]. The Right term is the global non-homogenous Dirichlet problem solved via Duhamel's Method.

#### Global non-homogenous Dirichlet problem 
$$
\begin{cases}
&v_t-D\Delta v = f(x,t)\;\;\;&x\in\mathbb{R}\times(0,\infty)\\
&v(x,0) = 0&x\in\mathbb{R}\\
\end{cases}
$$
The differential operator $\partial_t-D\partial_{xx}$  measures instantaneous density production rate. For our non-homogenous Dirichlet problem there will be non-zero instantaneous density production around the support of our forcing term. This is understood as an addition (or removal) of heat/mass external to the conserved system. such a system lacks mass conservation due to the forcing.

#### Duhamel's Method Formulation
Suppose that from time t=0 until a certain time $s>0$ no mass is present and that at time s a unit mass at the point $y$ appears. We know we can model this kind of source term as $\delta(x-y,t-s)$. This leads us to the hon-homogeneous equation $p_t - Dp_{xx}=\delta(x-y,t-s)$ with $p(x,0)=0$  as initial condition. Until t=s nothing happens and after s we have $\delta(x-y,t-s)=0$ therefore it is like starting from time $t=s$ and solving the problem
$$
\begin{cases}
&p-Dp_{xx}=0,&x\in\mathbb{R},\;t>s\\
&p(x,s)=\delta(x-y,t-s)\\
\end{cases}
$$
When $s=0$ we know that the solution is $\Gamma_D(x-y,t)$. We can translate this solution such that $p(x,t)=\Gamma_D(x-y,t-s)$ is a solution when $s>0$

$$
w(x,t,s) = \int_\mathbb{R} \Gamma_D(x-y,t-s)\;f(y,s)\;dy
$$
is a solution to:
$$
\begin{cases}
&w-Dw_{xx}=0,&x\in\mathbb{R},\;t>s\\
&w(x,s,s)=f(x,s) &x\in\mathbb{R}\\
\end{cases}
$$
We have created an initial value problem for some time step $s\in(0,t)$. This solution $w(x,t,s)$ solves the equation for a single moment in that time interval. We then integrate our solutions across the time interval to aggregate solutions through time. Which follows below. 
Now
$$
v(x,t) = \int_0^t w(x,t,s)\;ds = \int_0^t \int_\mathbb{R} \Gamma_D(x-y,t-s)f(y,s)\;dyds
$$
is a solution to
$$
\begin{cases}
&v_t-D\Delta v = f(x,t)\;\;\;&x\in\mathbb{R}\times(0,\infty)\\
&v(x,0) = 0&x\in\mathbb{R}\\
\end{cases}
$$

<u>Steps</u>
1. Construct a family of solutions ($w(x,t,s)$) of homogenous Cauchy problems, with variable initial time $s>0$, and initial data $f(x,s)$. 
2. Integrate the above family with respect to s, over $(0,t)$


#### Global homogenous Cauchy Problem
$$
\begin{cases}
&v_t-D\Delta v = 0\;\;\;&x\in\mathbb{R}\times(0,\infty)\\
&v(x,0) = g(x)&x\in\mathbb{R}\\
\end{cases}
$$
In [[Diffusion Equation]] we found that the solution of the above equation is ![[Diffusion Equation#^fa57ce]]
where $\Gamma_D(x-y,t)$ solves
![[Fundamental Solutions#^140a3a]]