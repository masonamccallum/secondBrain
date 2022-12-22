$\epsilon,\mu>0$
$$
\begin{cases}
&\epsilon\frac{\partial E}{\partial t} = \nabla\times H,\;\;\;\;\;\;E,H,x\in\mathbb{R}^3\\
&\mu\frac{\partial H}{\partial t}=-\nabla\times E\\
&E(x,0)=E_0(x)\\
&H(x,0)=H_0(x)\\
\end{cases}
$$
Fourier Tranform
$$
\begin{cases}
&\epsilon\frac{\partial \hat{E}}{\partial t} = -i\xi\times \hat{H}\\
&\mu\frac{\partial \hat{H}}{\partial t}=-i\xi\times \hat{E}\\
\end{cases}
$$
This equation in Matrix form is the following

$$\begin{pmatrix}
\epsilon I & 0  \\
0 & \mu I  \\
\end{pmatrix}\frac{\partial}{\partial t}
\begin{pmatrix} \hat{E}\\ \hat{H}\\ \end{pmatrix}
=i\begin{pmatrix}0_{3\times 3}&(\xi x)\\(-\xi x)&0_{3\times 3}\\\end{pmatrix}\begin{pmatrix}\hat{E}\\\hat{H}\end{pmatrix}
$$
where
$$
(\xi x) = 
\begin{pmatrix}
0 & -\xi_3 & \xi_2 \\
\xi_3 & 0 & -\xi_1 \\
-\xi_2 & \xi_1 & 0 \\
\end{pmatrix}
$$
