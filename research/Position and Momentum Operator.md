Note $\braket{\phi,\psi}=\int{\overline{\psi(x)}\varphi(x)\;dx}$
Consider a particle moving on the real line. $\varphi:\mathbb{R}^1\rightarrow\mathbb{C}$, $|\psi|^2$ is the probability density for the position of the particle. hence the integral over all of $\mathbb{R}^1$. Let $E\subset\mathbb{R}^1$  or stated otherwise $\psi$  is a unit vector in $L^2(\mathbb{R})$. 
$$P(x\in E)=\int_E |\psi|^2\;dx$$
The expected value is clearly
$$\mathbb{E}(x)=\int_{\mathbb{R}}x|\psi|^2\; dx$$
#### Position Operator
$$(X\psi)(x)=x\;\psi(x)$$
Using this notation we can represent the integral for expectation differently. using the fact that 
$\overline{\psi(x)}\psi(x)=|\psi(x)|^2$
$$\mathbb{E}(x)=\braket{\psi,x\psi}=\int_\mathbb{R} x|\psi(x)|^2=\braket{X}_\psi$$

#### Momentum Operator
The momentum of a quantum particle is encoded in the wave functions spacial frequency K. 
$$\psi = e^{ikx-i\omega t}$$ where $k$ is spacial frequency and $\omega$ is temporal frequency