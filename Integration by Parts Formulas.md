#pde #salsa #hagstrom
TODO: Dr.Hagstrom uses a variant of these formula which is not in the salsa book. Find and derive his formulation. used in lectures

Let $\Omega\subset\mathbb{R}^n$ , be a $C^1$ - domain. For vector fields $\mathbf{F}=(F_1,F_2,...,F_n): \Omega\rightarrow\mathbf{R}^n$
with $\mathbf{F}\in C^1(\bar{\Omega})$, The Gauss Divergence formula holds:
$$\int_\Omega \nabla\cdot\mathbf{F} dx = \int_{\partial\Omega} \mathbf{F}\cdot \nu d\sigma \tag{1.1}$$
Where $\nu$ denotes the outward normal unit vector to $\partial\Omega$. The core useful identities for analyzing PDE's can be derived using (1.1). 

#### Integration by parts
Apply (1.1) to $v\mathbf{F}$, with $v\in C^1(\bar{\Omega})$ and recalling $div(v\mathbf{F})=v\;div\mathbf{F} + \nabla v\cdot\mathbf{F}$

$$\int_\Omega v\;div(\mathbf{F})\;dx= \int_{\partial\Omega}v\;\mathbf{F}\cdot\nu\; d\sigma - \int_{\Omega}\nabla v\cdot\mathbf{F}\;dx \tag{1.2}$$

#### First Green's Identity
Choosing $\mathbf{F}=\nabla u, \; u\in C^2(\Omega)\bigcap C^1(\bar{\Omega})$, since $div\nabla u = \Delta u$ and $\nabla u\cdot \nu= \partial_\nu u$, the following greens identity follows:

$$\int_\Omega v\Delta u\; dx = \int_{\partial\Omega} v\partial_\nu u \;d\sigma - \int_\Omega \nabla v\cdot \nabla u\; dx \tag{1.3}$$
#### Seconds Green's Identity
If also $v\in C^2(\Omega)\bigcap C^1(\bar{\Omega})$, Interchanging the roles of u and v in (1.2) and subtracting, we get the following
$$\int_\Omega (v\Delta u - u\Delta v)\; dx = \int_{\partial\Omega}(v\partial_\nu u - u\partial_\nu v)\;d\sigma \tag{1.4}$$
