
### intro and perspectives on Spectral Theorem
Suppose $H$ is a finite-dimensional Hilbert space and A is a self-adjoint linear operator on $H$, meaning that $\braket{\phi,A\varphi}=\braket{A\phi,\varphi}$ for all $\phi,\varphi\in H$. Then there exists an orthonormal basis of $H$ consisting of eigenvectors for A with real eigenvalues. This is an application of the [[Spectral Theorem]] to finite-dimensional Hilbert spaces on bounded self-adjoint operators. This becomes more complicated for our unbounded quantum operators. With an appropriate Spectral theory we will have the tools to apply functions to an unbounded operator.
	for example a solution to the time dependent Schrödinger equation is found by setting $\varphi(t)=exp\{\frac{-it\hat{H}}{\hbar}\}\varphi_0$. If $\hat{H}$ has a true set of eigenvectors we can state that 
$$exp\{\frac{-it\hat{H}}{\hbar}\}e_k=exp\{\frac{-it\lambda_k}{\hbar}\}e_k,\;\;\;\;\forall k\in\mathbb{Z}$$
	if $\hat{H}$ does not have a true set of eigenvectors we will employ functional calculus to apply functions to $\hat{H}$.

Secondly we would also like to employ the spectral theorem to provide a probability distribution for the result of measuring a self-adjoint operator A.

![[compact operator]]
## Difficulties of quantum operators
key here is that $H$ is finite-dimensional. This not the case for infinite dimensional operators. our need for orthonormal basis for eigenvectors is met for [[compact operator|compact]] self-adjoint operators, however operators of interest in quantum mechanics are not compact. Another challenge we must face is that the self-adjoint operators on infinite-dimensional Hilbert spaces  are [[Unbounded Operators|unbounded]].  Recall that Compact $\Rightarrow$ boundedness

- On infinite-dimensional Banach spaces, the spectrum of an operator does not necessarily equal the set of eigenvalues.
Recall:
![[Bounded Inverse Theorem]]
##### Bounded Self-Adjoint operators
For $A\in\mathcal{B}(H)$, the **Resolvent set** of A, denoted $\rho(A)$ is the set of all $\lambda\in\mathbb{C}$ such that the operator $(A-\lambda I)$ has a bounded inverse. The spectrum of A, denoted $\sigma(A)$, is the complement in $\mathbb{C}$ of the resolvent set. For $\lambda$ in the resolvent set of A, the operator $(A-\lambda I)^{-1}$ is called the resolvent of A at $\lambda$ 

>[!note] Spectrum definition from MIRA by S.Axler
>Suppose T is a bounded operator on a Banach space V
> - a number $\lambda\in\mathbb{F}$ is called an eigenvalue of T if $T-\lambda I$ is not injective (or one-to-one).
> - A nonzero vector $f\in V$ is called an eigenvector of T corresponding to an eigenvalue $\lambda\in\mathbb{F}$  if $$Tf=\lambda f$$ 
> - The spectrum T is denoted $sp(T)$ and is defined $$sp(T)=\{\lambda\in\mathbb{F}: T-\lambda I \text{ is not invertible}\}$$

if $A\in\mathcal{B}(H)$ is self-adjoint, then the following hold
- The spectrum of A is contained in the real line
- A number $\lambda\in\mathbb{R}$ belongs to the spectrum of A if an only if there exists a sequence $\psi_n$ of non-zero vectors in H such that $$\lim\limits_{n\rightarrow\infty}\frac{||A\psi_{n}-\lambda\psi_n||}{||\psi_n||}=0$$ This states that an element of the spectrum is almost an eigenvalue relative to the size of $\psi$ 
Example: Let $H=L^2([0,1])$ and let $A$ be the operator be the position operator on H defined by $(A\psi)(x)=x\psi(x)$. We have seen that their are no true eigenvalues for this operator. The generalized eigenvalues are delta functions however these are not square integrable functions and therefore are not in our Hilbert space. We will prove that $\sigma(A)=[0,1]$ 
first note that A is bounded and self-adjoint. Given $\lambda\in(0,1)$, consider the functions $\psi_n:=1_{[\lambda,\lambda+1/n]}$ 
> [!warning]
> I think the following sequence works better for this proof. 
$\psi_n:=\left(\sqrt{n}\right)_{[\lambda,\lambda+1/n]}$.  This way $||\psi_n||^2=\frac{1}{n}$  for the proposed sequence in the book I believe $||\psi_n||^2=\frac{1}{n^2}$

$||\psi_n||^2=\frac{1}{n}$ since $|x-\lambda|\le \frac{1}{n}\text{ for}\;\;x\in[\lambda,\lambda+1/n]$.  we have
$$(A-\lambda I)\psi_n=A\psi_{n}-\lambda I\psi_n=x\psi_{n}-\lambda\psi_n=(x-\lambda)\psi_n$$
$$||(A-\lambda I)\psi_n||=|x-\lambda|\;||\psi_n||\le\frac{1}{n}||\psi_n||\le\frac{1}{n\sqrt{n}}$$
$$||(A-\lambda I)\psi_n||^2\le\frac{1}{n^3}$$
Therefore $\lambda$ belongs to the spectrum of A and the spectrum of A is closed. Meanwhile, if $\lambda \not\in [0,1]$, $1/(x-\lambda)$ is bounded on $[0,1]$, so $A-\lambda I$ has bounded inverse.
$(A-\lambda I)(A-\lambda I)^{-1}\psi=\frac{1}{x-\lambda}(A-\lambda I)\psi=\frac{x-\lambda}{x-\lambda}\psi=\psi$     
thus $\sigma(A)=[0,1]$ 

##### Spectral Theory for bounded self-adjoint operators
Given a bounded self-adjoint operator A, we hope to associate with each Borel set $E\subset\sigma(A)$ a closed subspace $V_E$ of H, where we think intuitively that $V_E$ is the closed span of the generalized eigenvectors for for A. with eigenvalues in E. We expect the following properties 
1. $V_{\sigma(A)}=H$ and $V_{\emptyset}=\{0\}$ 
2. If $E$ and $F$ are disjoint, then $V_{E}\perp V_{F}$
3. For any $E$ and $F$, $V_{E\cap F}=V_{E}\cap V_{F}$ 
4. If $E_1,E_2,...$ are disjoint, and $E=\cup_{j}E_j$, then $$V_{E}=\bigoplus\limits_{j}V_{E_j}$$
5. For any E, $V_E$ is invariant under A. 
6. If $E\subset [\lambda_0-\epsilon,\lambda_0+\epsilon]$ and $\psi\in V_{E}$, then $$||(A-\lambda I)\psi||\le\epsilon||\psi||$$
note that given a closed subspace V of H, there exists a unique bounded operator P that equals the identity on V and equals zero on the orthogonal complement $V^\perp$ of V. 
This operator is called an [[Orthogonal Projector]]

![[Projection valued measure]]

##### Spectral Theory for unbounded Self-Adjoint operators
