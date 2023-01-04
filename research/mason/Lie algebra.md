#QM 
A Lie algebra over a field $\mathbb{F}$ is a vector space $\mathbb{g}$ over $\mathbb{F}$, together with a "bracket" map $[\cdot,\cdot]:\mathbb{g}\times\mathbb{g}\rightarrow \mathbb{g}$  having the following properties
1. $[\cdot,\cdot]$ is bilinear
2. $[Y, X] = -[X, Y] \;\;\;\;\forall X,Y\in\mathbb{g}$ 
3. $[X,X]=0\;\;\;\;\forall X\in\mathbb{g}$
4. For all $X,Y,Z\in\mathbb{g}$ we have the **Jacobi identity** $$
 [X,[Y,Z]] + [Y,[Z,X]] + [Z,[X,Y]] = 0
 $$
 ---

## Endomorphism
 an endomorphism is a morphism from one mathematical object to itself. for our purposes in QM the operator M is an element of the Endomorphisms on our space S iff
$M:S\rightarrow S$ 
## Parity of Permutation
When X is a finite set with at least two elements, the permutations of X fall into two classes of equal size. These are the even or odd parity permutations.


## Commutator of Matrices
$$
[B_1,B_2]=B_1B_2-B_2B_1
$$
 ## Demonstration
 $$
\begin{align*}
\mathcal{A} &=\{A\in End(\mathcal{H}):A^*=A\}\\
i\mathcal{A} &=\{B\in End(\mathcal{H}):B^*=-B\}\\
\end{align*}
$$
$i\mathcal{A}$ is known as anti-self adjoint and forms a Lie algebra on the commutator. 

- $i\mathcal{A}\times i\mathcal{A}\rightarrow i\mathcal{A},\;\;\;\;B_1,B_2\in\mathcal{H}$  $[B_1,B_2]^*=(B_1B_2-B_2B_1)^*=B_2^*B_1^*-B_1^*B_2^*=B_2B_1-B_1B_2=-[B_1,B_2]$
- $[B_1,B_2]=-[B_2,B_1],\;\;\;(skew-symmetry)$
- $\text{Cycl}_{1,2,3} [B_1,[B_2,B_3]]=[1,[2,3]]+[2,[1,3]]+[3,[1,2]]=0$
show:  Jacobi Identity, Skew-Symmetry

## Example
$\mathcal{H}\in\mathbb{C}^2$ then let $b_1,b_2,b_3\in\mathcal{A}$ be three observables. Now consider the following three $\frac{ib_1}{2},\frac{ib_2}{2},\frac{ib_3}{2}$ 
$$
[\frac{ib_a}{2},\frac{ib_b}{2}]=-\left(\sum\limits_{c=1}^{3}\epsilon_{a,b,c}\frac{ib_c}{2} \right)
$$
Where $$\epsilon_{a,b,c}=\begin{cases}1,&\text{if (a,b,c) is a positive permutation}\\
-1, &\text{if (a,b,c) is a negative permutation}\\
0,\;\;\;&\text{otherwise}
\end{cases}$$