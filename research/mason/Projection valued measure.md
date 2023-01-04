Let X be a set and $\Omega$ a $\sigma$-algebra in X. A map $\mu:\Omega\rightarrow\mathcal{B}(H)$ is called a projection-valued measure if the following properties hold 
1. For each $E\in\Omega$, $\mu(E)$ is an orthogonal projection
2. $\mu(\emptyset)=0$  and $\mu(X)=I$ 
3. If $E_1,E_2,...$ in $\Omega$ are disjoint, then for all $v\in H$, we have $$\mu\left(\bigcup\limits_{j=1}^{\infty}E_j \right)v=\sum\limits_{j=1}^{\infty}\mu(E_j)v$$
4. For all $E_1,E_2\in\Omega$, we have $\mu(E_{1}\cap E_{2})=\mu(E_1)\mu(E_2)$

## Operator Valued Measure 
w.r.t projection valued measure
Observe that, for any projection valued measure $\mu$ and $\psi\in H$, we can form an ordinary real-valued measure $\mu_\psi$ by setting $$\mu_\psi(E)=\braket{\psi,\mu(E)\psi}$$
more formally  

let $\Omega$ be a $\sigma$-algebra in X and let $\mu:\Omega\rightarrow\mathcal{B}(H)$ be a projection-valued measure. Then there exists a unique linear map, denoted $f\mapsto \int_{\Omega}fd\mu$, from the space of bounded, measurable, complex-valued functions on $\Omega$ into $\mathcal{B}(H)$ with the property that $$\braket{\psi,\left(\int_{X} f\;d\mu\right)\psi}=\int_{X}f\; d\mu_\psi$$
for all $f$ and all $\psi\in H$, where $\mu_\psi(E)=\braket{\psi,\mu(E)\psi}$