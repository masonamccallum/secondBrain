Also known as Dirac notation. Let H be an appropriate Hilbert space
#### Bra-ket
A vector $\psi\in H$ is referred to as a **ket**  and is denoted $\ket{\psi}$. A continuous linear functional on H is called a **Bra**. For and $\phi\in H$, let $\bra{\phi}$ denote the linear functional (bra) given by
$$\bra{\phi}\;(\varphi)=\braket{\phi,\varphi}$$  
That is to say, $\bra{\phi}$ is the "inner product with $\phi$" functional. The bracket (or bra-ket) of two vectors $\phi, \varphi \in H$ is a result of applying the bra $\bra{\phi}$ to the ket $\ket{\varphi}$, namely the inner product of the $\phi$ and $\varphi$, denoted $\braket{\phi|\varphi}$ 

If A is an operator on H and $\phi$ is a vector in H, then we can form a linear functional $\bra{\phi}A$, which is a linear map $\varphi \mapsto \braket{\phi|A\varphi}$. Physicists generally write an expression of this form as $\braket{\phi|A|\varphi}$. 

#### Ket-Bra
For any $\phi$ and $\varphi$ in H, the expression $\ket{\phi}\bra{\varphi}$ denotes the linear operator on H given by the following
$$(\ket{\phi}\bra{\varphi})(\mathcal{X})=\ket{\phi}\braket{\varphi|\mathcal{X}}= \braket{\varphi|\mathcal{X}}\ket{\phi}$$
This operation ket-bra is interpreted as the vector $\ket{\phi}$ multiplied by the  scaler $\braket{\varphi|\mathcal{X}}$ 

#### Adjoint notation
If A is a [[Bounded Operators|bounded operator]]  on H, then $A^*$ is the unique bounded operator such that 
$$\bra{\psi}\;A=\bra{A^*\psi}$$
This is because the following
$$\begin{aligned}
&\bra{\psi|A}
=\braket{\psi|A|\phi}
= \braket{\psi|A\phi}
= \braket{A^*\psi|\phi}
= \bra{A^*\psi}\\
\end{aligned}
$$

### Decomposition. Basis expansion
This is the orthogonal projection onto the one dimensional subspace spanned by the vector $\ket{n}=\ket{\psi_{n}}$. assuming $\ket{n}$ is a unit vector
$$I=\sum\limits_{n}\ket{\psi_n}\bra{\psi_n}=\sum\limits_{n}\ket{n}\bra{n}$$
#### position wave function
Given an irreducible representation of a canonical commutation relations, and given a vector $\psi$ in the corresponding Hilbert space, a physicist will speak of the position wave function, defined by
$$
\psi(x) = \braket{x|\psi}
$$
Here, $\bra{x}$ is the bra associated with the ket $\ket{x}$, where $\ket{x}$ is supposed to be an eigenvector for the position operator with eigenvalue x.

#### Tensor product basis 
$$\ket{m,\alpha} \rightarrow \ket{m}\otimes\ket{\alpha}\in\mathscr{H}_{external}\otimes\mathscr{H}_{internal}$$ 