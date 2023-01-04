#pde #salsa #hagstrom  
## Fundamental Solution of Diffusion equation 
The fundamental solution is one that will allow us to construct many other solutions. 
#### Invariant transformations
The homogeneous diffusion equation has simple but important properties. Let $u=u(x,t)$ be a solution of $$u_t-D\Delta u=0$$
$v(x,t) = u(x,-t)$, this equation is the solution to the adjoint or backward equation
$$v_t+D\Delta v = 0$$
This transformation $t\mapsto -t$ shows us an aspect of time irreversibility for the diffusion equation.  Symmetries and invariant transformations characterize the space of solutions for a given PDE.   
We look for solutions of the form $u^*(x,y)=cu(ax,bt)$. We find that $b=a^2$ $\therefore\;x\mapsto ax$ and  $t\mapsto a^2 t$. Under this transformation the following quantity is unchanged $\frac{|x|^2}{Dt}$

#### Similarity solutions
given this dimensionless quantity we will look for solutions of the form. We will look for the function $U(\xi)$ such that $u^*$ is a solution to the PDE. A solution of this form is one that scales some function $U(\xi)$  through time and space to map our solution. a one space dimension, self-similar solution has the general form $u(x,t)=a(t)F(x/b(t))$ where $u/a$ and $x/b$ are dimensionless quantities. Our self-similar solution is of the form.
$$u^*(x,t)=\frac{q}{\sqrt{Dt}}U\left(\frac{x}{\sqrt{Dt}}\right)$$
We also require a total mass condition. Namely
$$1=\frac{1}{\sqrt{Dt}} \int_\mathbb{R} U\left(\frac{x}{\sqrt{Dt}}\right)\;dx=\int_{\epsilon=x/\sqrt{Dt}} U(\xi)\;dx$$ 
Plugging in $u^*$  into our PDE we find the following ODE. 
$$u^*_t-Du_{xx}^t = -\frac{q}{t\sqrt{Dt}}\left[ U''(x)+\frac{1}{2}\xi U'(\xi)+\frac{1}{2}U(\xi) \right]$$
We get the following:
$$U''(x)+\frac{1}{2}\xi U'(\xi)+\frac{1}{2}U(\xi)=0 $$
because $U\ge 0$ and has an area of 1 we know that $U(-\infty)=U(\infty)=0$. 
The ODE above can be written in the form
$$U'(\xi)+\frac{1}{2}\xi U(\xi)=C,\;\;\;C\in\mathbb{R}$$
Who has general solution of the form
$$U(\xi)=c_0e^{\frac{-\xi^2}{4}}$$
Now we just select $c_0$ based on the constant mass condition to find that $c_0=(4\pi)^{-1/2}$ 
$\therefore$
#### Fundamental Solution (n=1)
$$u^*(x,t)=\frac{q}{\sqrt{4\pi Dt}}e^{-\frac{x^2}{4Dt}},\;\;\; x\in\mathbb{R},t>0$$

Where $\int_\mathbb{R}u^*(x,t)dx=q, t>0$

#### Fundamental Solution (n>1)
$$\Gamma_D(x,t)=\frac{1}{(4\pi Dt)^{n/2}}exp\left(\frac{-|x|^2}{4Dt}\right)$$
This is the general fundamental solution of the diffusion equation.
For fixed y, the fundamental solution $\Gamma_D(x-y,t)$ is the unique solution of the 
#### Global Cauchy problem 
$$
\begin{cases}
	&u_t-D\Delta u = 0 &x\in\mathbb{R}^n, t>0\\
	&u(x,0)=\delta (x-y) &x\in\mathbb{R}^n\\
\end{cases}
$$

^140a3a

### Discussion
#strichartz 
consider the classical problem: $\Delta u=f$
Now suppose we could solve the following distributional problem. $\Delta P=\delta$.
then
$$
\Delta(P*f)=\Delta P * f=\delta*f=f
$$
this works if P is a tempered distribution and $f\in\mathcal{S}$ 

