#pde #hagstrom 

$$
\begin{aligned}
\mathcal{F}\left(e^{-\nu|x|^2}\right)&=\frac{1}{(2\pi)^n}\int_{\mathbb{R}^n}e^{-i\xi\cdot x - \nu |x|^2} \;dx\\
&=\frac{1}{(2\pi)^n}\prod_j^n\int_{\mathbb{R}}e^{-i\xi_j x_j - \nu x_j^2} \;dx_j\\
&=\frac{1}{(2\pi)^n}\prod_j^n 
e^{\frac{-1}{4\nu}} \int_{\mathbb{R}}e^{\left(-\nu x_j+\frac{i\xi_j}{2\nu}\right)^2} \;dx_j\\
&=(2\pi)^{-n} \left(\sqrt{\frac{\pi}{\nu}}\right)^n e^{\frac{-1}{4\nu}\xi^2}\\
\end{aligned}
$$
This section is prerequisite to the H.U.P because it shows that a gaussian which is thin in position space is fat in momentum space. and likewise a thin gaussian in momentum space is fat in position space. 

Let $u$ be  a probability distribution $\int |u|^2 = 1$.
$$
\left(\int_\mathbb{R}(x-x_0)^2\;|u|^2\;dx\right)\left(\int_\mathbb{R}(\xi-\xi_0)^2|\hat{u}|^2\;d\xi\right)\ge\frac{1}{8\pi}
$$
If the first factor is really small then the location of a particle in 1d is known with a certain accuracy. We then however get that the accuracy of knowing momentum is inversely related to our knowledge of position.