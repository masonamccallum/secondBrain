## Definition 
An operator T is compact on a Hilbert space V if for every bounded sequence $f_1,f_2,...$ in V, the sequence $Tf_1,Tf_2,...$ has a convergent subsequence. The collection of compact operators on V is denoted by $\mathbb{C}(V)$ 

- Every compact operator on a Hilbert space is a bounded operator.
- Bounded operators with finite-dimensional range are compact

> [!note] Bounded operators with finite-dimensional range are compact
> If T is a bounded operator on a Hilbert space and range T is finite-dimensional then T is compact
>> [!tip] Proof
 >>Suppose T is a bounded operator on a Hilbert space V and range T is finite-dimensional. Suppose $e_1,e_2,...,e_m$   is an orthonormal basis of range T. Now suppose $f_1,f_2,...$ is a bounded sequence in V. For each $n\in\mathbb{Z}^{+}$, we have 
 >>$$Tf_n=\braket{Tf_n,e_1}e_1+...+\braket{Tf_n,e_m}e_m$$ Via the [[Cauchy-Schwarz inequality]] we have that $|\braket{Tf_n,e_j}|\le||T||\sup\limits_{k\in\mathbb{Z}^+}||f_k||$ for every $n\in\mathbb{Z}^+$ and $j\in\{1,...,m\}$. Thus there exists a subsequence $f_{n_1},f_{n_2},...$ such that $\lim\limits_{k\rightarrow\infty}\braket{Tf_{n_k},e_j}e_j$ exists in $\mathbb{F}$  for each $j\in\{1,...,m\}$. This implies that $\lim\limits_{k\rightarrow\infty}Tf_{n_k}$  exists in V. Thus T is compact