#pde #hagstrom #salsa 
the maximum principle is a useful tool for showing that elliptic and parabolic equations are a [[Well Posed Problem]]. An example of this is shown in the [[Maximum Principles#Results and corollaries| Results and corollaries section]]
### Maximum principles for Diffusion Equation
For the following sections $Q_T = \Omega\times(0,T]$ and $\partial_p Q_T$ is the union of the base and the lateral boundary of $Q_T$
Let $w\in C^{2,1}(Q_T)\bigcap C(\bar{Q}_T)$ such that $$w_t-D\Delta w = q(x,t)\le 0\;\;\;\;\;\; (resp. \ge 0)$$ Then w attains is maximum (resp. minimum) on $\partial_p Q_T$ 
$$\max\limits_{\bar{Q}_T} w = \max\limits_{\partial_p Q_t} \;\;\;\;\;\;\left(resp.\;\; \min\limits_{\bar{Q}_T} = \min\limits_{\partial_p Q_T}\right)$$

We will prove the maximum principle the minimum principle is identical.

### Results and corollaries
1. If a solution does attain its maximum on the interior of $\partial_p Q_T$ then the solution is constant on $Q_T$ 
2. the maximum and minimum principles are useful for proving continuous dependence on data as seen below
		The following is from page 38 of salsa
		Let $v,w\in C^{2,1}(Q_T)\bigcap C(\bar{Q}_T)$ be solutions of $$w_t-\Delta w = f_1\;\;\;\text{and}\;\;\;v_t-\Delta v=f_2$$
		with $f_1,f_2$ bounded in $Q_T$. 
		$$\max\limits_{\bar{Q}_T}|v-w|\le \max\limits_{\partial_p Q_T}|v-w|+T\sup\limits_{\bar{Q}_T}|f_1-f_2|$$
		This is inequality is considered a uniform pointwise stability estimate. These are powerful for showing stability of solution w.r.t. the data. as follows. Suppose $v=g_1, \; w= g_2\;\; x\in \partial_p Q_T$ and
		$$\max\limits_{\partial_p Q_T}|g_1-g_2|\le \epsilon\;\;\;\;\text{and}\;\;\;\;\sup\limits_{\bar{Q}_T}|f_1-f_2|\le \epsilon$$
		We can conclude
		$$\max\limits_{\bar{Q}_T}|v-w|\le \epsilon(1+T)$$
		Therefore a small uniform distance between the data implies small information distance between corresponding solutions.
	
#### Proof
Let $q\le 0$, 
Case 1: First assume that $w\in C^2(\bar{Q}_T)$ and that $q(x,t)< 0$ for all $(x,t)\in \bar{Q}_T$    
We will start by way of contradiction. Suppose that $w$ attains its maximum at a point $(x_0,t_0)\not\in \partial_p Q_T$ . Therefore  
$$\Delta w(x_0, t_0)\le 0$$
we can also conclude that either 
$$w_t(x_0,t_0)=0\;\;\; \text{or}\;\;\; w_t(x_0,T)\ge 0$$
In either case we get the contradiction $0\le w_t(x_0,x_t) - D\Delta w(x_0,t_0) = q(x_0,t_0)<0$  

Case 2: Seconds assume that $w\in C^2(Q_T)\bigcap C(\bar{Q}_T)$ and $q\le0$ in $\bar{Q}_T$ 
- This case is an extension of case 1 where we don't enforce as much continuity along the space time boundary. this proof is found on page 37 of the salsa textbook
