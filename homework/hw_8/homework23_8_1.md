对如下基计算二元组$\begin{bmatrix}3,2\end{bmatrix}^{\mathrm{T}}$的展开系数，并写出对应的展开：
(a)在$R^2$上，实数二元组集合的基$\varphi_0=\left[1/\sqrt{2},1/\sqrt{2}\right]^T$ 和$\varphi_1=\left[1/\sqrt{2},-1/\sqrt{2}\right]^T$。
(b)在$R^2$上，基$\varphi_0=[1,0]^\mathrm{T}$ 和$\varphi_1=[1,1]^\mathrm{T}$,及其对偶$\tilde{\varphi}_0=[1,-1]^\mathrm{T}$ 和$\tilde{\varphi}_1=[0,1]^\mathrm{T}$。
(c)在 $R^2$ 上，基$\varphi_0=[1,0]^\mathrm{T},\quad\varphi_1=\begin{bmatrix}-1/2,\sqrt{3}/2\end{bmatrix}^\mathrm{T}$和$\varphi_2=\left[-1/2,-\sqrt{3}/2\right]^\mathrm{T}$,及它们的对偶$\tilde{\varphi}_i=2\varphi_i/3$ ,
 $i=\{0,\:1,2\}$。
 (提示： 必须使用向量内积来代替 7.2.1 节中的内积。)

令$f=\begin{bmatrix}3,2\end{bmatrix}^{\mathrm{T}}$

(a)
$$
\begin{aligned}
\alpha_0
&=f^T\varphi_0\\
&=\begin{bmatrix}3,2\end{bmatrix}\begin{bmatrix}1/\sqrt{2}\\1/\sqrt{2}\end{bmatrix}\\
&=\frac{5}{\sqrt{2}}
\end{aligned}
$$

$$
\begin{aligned}
\alpha_1
&=f^T\varphi_1\\
&=\begin{bmatrix}3,2\end{bmatrix}\begin{bmatrix}1/\sqrt{2}\\-1/\sqrt{2}\end{bmatrix}\\
&=\frac{1}{\sqrt{2}}
\end{aligned}
$$

所以$\begin{bmatrix}3,2\end{bmatrix}^{\mathrm{T}}=\frac{5}{\sqrt{2}}\varphi_0+\frac{1}{\sqrt{2}}\varphi_1$

(b)
$$
\begin{aligned}
\alpha_0
&=f^T\tilde\varphi_0\\
&=\begin{bmatrix}3,2\end{bmatrix}\begin{bmatrix}1\\-1\end{bmatrix}\\
&=1
\end{aligned}
$$

$$
\begin{aligned}
\alpha_1
&=f^T\tilde\varphi_1\\
&=\begin{bmatrix}3,2\end{bmatrix}\begin{bmatrix}0\\1\end{bmatrix}\\
&=2
\end{aligned}
$$

所以$\begin{bmatrix}3,2\end{bmatrix}^{\mathrm{T}}=1\varphi_0+2\varphi_1$

(c)

因为$\tilde{\varphi}_i=2\varphi_i/3$，所以
$$
\tilde\varphi_0=\begin{bmatrix}\frac{2}{3},0\end{bmatrix}^\mathrm{T},
\quad\tilde\varphi_1=\begin{bmatrix}-\frac{1}{3},\frac{\sqrt{3}}{3}\end{bmatrix}^\mathrm{T},
\quad\tilde\varphi_1=\begin{bmatrix}-\frac{1}{3},-\frac{\sqrt{3}}{3}\end{bmatrix}^\mathrm{T}
$$

$$
\begin{aligned}
\alpha_0
&=f^T\tilde\varphi_0\\
&=\begin{bmatrix}3,2\end{bmatrix}\begin{bmatrix}\frac{2}{3}\\0\end{bmatrix}\\
&=2
\end{aligned}
$$

$$
\begin{aligned}
\alpha_1
&=f^T\tilde\varphi_1\\
&=\begin{bmatrix}3,2\end{bmatrix}\begin{bmatrix}-\frac{1}{3}\\\frac{\sqrt{3}}3{}\end{bmatrix}\\
&=-1+\frac{2\sqrt{3}}{3}
\end{aligned}
$$

$$
\begin{aligned}
\alpha_2
&=f^T\tilde\varphi_2\\
&=\begin{bmatrix}3,2\end{bmatrix}\begin{bmatrix}-\frac{1}{3}\\-\frac{\sqrt{3}}3{}\end{bmatrix}\\
&=-1-\frac{2\sqrt{3}}{3}
\end{aligned}
$$

所以$\begin{bmatrix}3,2\end{bmatrix}^{\mathrm{T}}=2\varphi_0+(-1+\frac{2\sqrt{3}}{3})\varphi_1+(-1-\frac{2\sqrt{3}}{3})\varphi_2$

