![[Fourier Series#Fourier Series Basic Fact 1]] 
![[Fourier Series#Parseval's Identity]]

#### Fourier Transform
Given a complex-valued function $f(x)$ of a real variable, define the **Fourier Transform** of $f$, denoted $\mathcal{F}f$  of $\hat{f}$, by
$$\mathcal{F}f(\xi)=\int_{\mathbb{R}^n}f(x)e^{ix\xi}\;dx$$
and
$$\mathcal{F}^{-1}f(\xi)=\frac{1}{(2\pi)^n}\int_{\mathbb{R}^n}f(x)e^{-ix\xi}\;dx$$

where $\mathcal{F}^{-1}(\mathcal{F}f)=f$  and  $\mathcal{F}(\mathcal{F}^{-1}f)=f$ 

> [!warning] 
> There is no general agreement on whether to put the minus sign with $\mathcal{F}f$ or $\mathcal{F}^{-1}f$, or on what to do with $\frac{1}{2\pi}$. Dr. Hagstrom splits the factor of $1/2\pi$ into $\frac{1}{\sqrt{2\pi}}$. He also puts the minus sign on the inverse fourier transform.
>> [!TIP]+ Dr.Hagstrom Fourier Series convention
>> $$\hat{f}(\xi,t)=\mathcal{F}f(\xi,t)=\frac{1}{(2\pi)^n}\int_{\mathbb{R}^n}f(x,t)e^{-i\xi\cdot x}\;dx$$
>> $$f(x,t)=\mathcal{F}^{-1}f(x,t)=\int_{\mathbb{R}^n}\mathcal{F}f(\xi,t)e^{i\xi\cdot x}\;d\xi$$
#### Plancherel formula
$$\int_{-\infty}^{\infty}|f(x)|^2\;dx=\frac{1}{2\pi}\int_{-\infty}^{\infty}|\mathcal{F}(\xi)|^2\;d\xi$$   
For this formulation we require that $f(x)$ tend to zero sufficiently rapidly. 

#### rapidly decreasing function
1. We say a function is <u>rapidly decreasing</u> if there are constants $M_n$ such that $|f(x)|\le M_n|x|^{-N}\;\text{as}\;x\rightarrow \infty$,  for $N=1,2,3,...$ 
2. We say a function is <u>rapidly decreasing</u> if after multiplication by any polynomial $p(x),\; p(x)f(x)$  still goes to zero as $x\rightarrow\infty$. A $C^\infty$ function is a class $\mathcal{S}(\mathbb{R}^n)$ if $f$ and all its partial derivatives are rapidly decreasing. $\mathcal{S}(\mathbb{R}^n)$ is called "the Schwartz class". 
$$\mathcal{D}(\mathbb{R}^n)\subset\mathcal{S}(\mathbb{R}^n)$$
A typical function in $\mathcal{S}(\mathbb{R}^n)$ is $e^{-|x|^2}$; this function does not have bounded support so it is not in $\mathcal{D}(\mathbb{R}^n)$. To see that $e^{-|x|^2}\in\mathcal{S}(\mathbb{R}^n)$  note that any derivative is a polynomial times $e^{-|x|^2}$, and $e^{-|x|^2}$ decreases fast enough as $x\rightarrow\infty$ that it beats out the growth of any polynomial. 
#### Elementary properties of the class $\mathcal{S}(\mathbb{R}^n)$ 
1. $\mathcal{S}(\mathbb{R}^n)$ is a vector space; it is closed under linear combinations
2. $\mathcal{S}(\mathbb{R}^n)$ is an algebra; the product of functions in $\mathcal{S}(\mathbb{R}^n)$ also belongs to $\mathcal{S}(\mathbb{R}^n)$ (this follows from Leibniz formula for derivatives of products)
3. $\mathcal{S}(\mathbb{R}^n)$ is closed under multiplication by polynomials
4. $\mathcal{S}(\mathbb{R}^n)$ is closed under differentiation
5. $\mathcal{S}(\mathbb{R}^n)$ is closed under translations and multiplication by complex exponentials $e^{ix\cdot \xi}$ 
6. $\mathcal{S}(\mathbb{R}^n)$ functions are integrable: $\int_{\mathbb{R}^n}|f(x)|\;dx<\infty$ for $f\in\mathcal{S}(\mathbb{R}^n)$. 
7. $f\in\mathcal{S}(\mathbb{R}^n)\Rightarrow\mathcal{F}f\in\mathcal{S}(\mathbb{R}^n)$ 

Below we will derive fundamental properties of Fourier transform
###### Translation
$$
\begin{aligned}
\tau_y f(x) &= f(x+y)\\
&=\int_{\mathbb{R}^n}f(x+y)e^{ix\cdot\xi}\;dx\\
&\;\;\;\;\;x\mapsto x-y\\
&=\int_{\mathbb{R}^n}f(x)e^{i(x-y)\cdot\xi}\;dx\\
\end{aligned}
$$
$e^{i(x-y)\cdot\xi}=e^{-iy\cdot\xi}e^{ix\cdot \xi}$
$$
\therefore \mathcal{F}(\tau_y f)(\xi) = e^{-iy\cdot \xi}\mathcal{F}f(x)
$$
Therefore translation by the vector y in real space results in multiplication by the exponential $e^{-iy\cdot\xi}$ in Fourier space. 
##### Differentiation
Recall the limit definition of derivatives. It a limit applied to translation. Therefore we would expect differentiation to have a similar form to translation.
$$
\begin{aligned}
\mathcal{F}\left(\frac{\partial}{\partial x_k}f\right)(\xi)&=\int e^{ix\cdot\xi}\frac{\partial f}{\partial x_k}(x)\;dx\\
&=-\int f(x)\frac{\partial}{\partial x_k}(e^{ix\cdot\xi})\;dx\\
&=-i\xi_k \int f(x)e^{ix\cdot \xi}\;dx\\
&=-i\xi_k \mathcal{F}f(\xi)\\
\end{aligned}
$$
##### Convolution
Suppose $f,g\in\mathcal{S}$ define convolution $f*g$ by  
$$
f*g\;(x) = \int f(x-y)g(y)\;dy
$$ 
By a change of variables $y \rightarrow x-y$  is equal to $\int f(y)g(x-y)\;dy$  so $f*g=g*f$ 
under a Fourier transform a convolution becomes a multiplication in frequency space.
$$\mathcal{F}(f*g)(\xi)= \mathcal{F}f(\xi)\mathcal{F}g(\xi)$$
### Fourier transformation table
|Function ($x$)| Fourier Tranform $(\xi)$|
|---------|-----------|
|$f(x)$|$\mathcal{F}f(\xi)$|
|$f(x+y)$|$e^{-iy\cdot\xi}\mathcal{F}f(\xi)$|
|$e^{ix\cdot y}f(x)$|$\mathcal{F}f(\xi+y)$|
|$\frac{\partial}{\partial x_k}f(x)$|$-i\xi_k \mathcal{F}f(\xi)$|
|$p(\frac{\partial}{\partial x})f(x)$|$p(-i\xi_k)\mathcal{F}f(\xi)$|
|$x_kf(x)$|$-i\frac{\partial}{\partial\xi_k}\mathcal{F}f(\xi)$|
|$p(x)f(x)$|$p(-i\frac{\partial}{\partial\xi})\mathcal{F}f(\xi)$|
|$f(x)*g(x)*$|$\mathcal{F}f(\xi)\mathcal{F}g(\xi)$|
|$f(x)g(x)*$|$\frac{1}{(2\pi)^n}\mathcal{F}f(\xi)*\mathcal{F}g(\xi)$|

Moving forward in the course material we combine this Fourier Tranform theory with the theory of [[Generalized Functions]]. This theory is the [[Fourier Transform of Tempered Distributions]]
