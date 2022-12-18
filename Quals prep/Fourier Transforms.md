![[Fourier Series#Fourier Series Basic Fact 1]] 
![[Fourier Series#Parseval's Identity]]

#### Fourier Transform
Given a complex-valued function $f(x)$ of a real variable, define the **Fourier Transform** of $f$, denoted $\mathcal{F}f$  of $\hat{f}$, by
$$\mathcal{F}f(\xi)=\int_{\mathbb{R}^n}f(x)e^{ix\xi}\;dx$$
and
$$\mathcal{F}^{-1}f(\xi)=\frac{1}{(2\pi)^n}\int_{\mathbb{R}^n}f(x)e^{-ix\xi}\;dx$$

where $\mathcal{F}^{-1}(\mathcal{F}f)=f$  and  $\mathcal{F}(\mathcal{F}^{-1}f)=f$ 
Additional notes:
	==Warning== 
	There is no general agreement on whether to put the minus sign with $\mathcal{F}f$ or $\mathcal{F}^{-1}f$, or on what to do with $\frac{1}{2\pi}$. Dr. Hagstrom splits the factor of $1/2\pi$ into $\frac{1}{\sqrt{2\pi}}$. 
	==Dr.Hagstrom convention==
	$$\mathcal{F}f(\xi)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}f(x)e^{ix\xi}\;dx$$
	$$\mathcal{F}^{-1}f(\xi)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}f(x)e^{-ix\xi}\;dx$$
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
###### Translation
##### Differentiation
##### Convolution
