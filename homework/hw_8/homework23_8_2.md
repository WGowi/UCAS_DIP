式(7.3.5)和式(7.3.6)中的 DWT 是起始尺度 $j_{0}$ 的函数。
(a)令 $j_0= 1( $而不是0$) $重新计算例 7.8 中函数 $f(n)=\{1,4,-3,0\}$ 在区间 0 $\leqslant n\leqslant3$内的一维 DWT。
(b)使用(a)的结果根据变换值计算 $f(1)$。



(a)

易知存在：
$$
f(n)=\frac{1}{\sqrt{M}}\sum_{k}W_{\varphi}(j_{0},k)\varphi_{j_{0},k}(n)+\frac{1}{\sqrt{M}}\sum_{j=j_{0}}^{\infty}\sum_{k}W_{\psi}(j,k)\psi_{j,k}(n)
$$
其中：
$$
\begin{aligned}
W_{\varphi}(j_{0},k)&=\frac{1}{\sqrt{M}}\sum_{n}f(n)\varphi_{j_{0},k}(n)\\
W_{\psi}(j,k)&=\frac{1}{\sqrt{M}}\sum_{n}f(n)\psi_{j,k}(n),\quad j\geq j_{0}
\end{aligned}
$$
已知$M=4,j=2$

 写出$4\times 4$大小的哈尔矩阵 
$$
\left.\boldsymbol{H}_4=\frac{1}{\sqrt{4}}\left[\begin{array}{cccc}1&1&1&1\\1&1&-1&-1\\\sqrt{2}&-\sqrt{2}&0&0\\0&0&\sqrt{2}&-\sqrt{2}\end{array}\right.\right]
$$
因为$j_0= 1$，可得$k\in\{0,1\}$
$$
\begin{aligned}
\varphi_{1,0}(\mathrm{n})&=\sqrt{2}\varphi(2\mathrm{n})=[\sqrt{2},\sqrt{2},0,0]  \\
\varphi_{1,1}(\mathrm{n})&=\sqrt{2}\varphi(2\mathrm{n}-1)=[0,0,\sqrt{2},\sqrt{2}] \\
\mathrm\psi_{1,0}(n)&=\sqrt{2}\psi(2n)=[\sqrt{2},-\sqrt{2},0,0]\\
\psi_{1,1}(\mathrm{n})&=\sqrt2\psi(2\mathrm{n}-1)=[0,0,\sqrt2,-\sqrt2]
\end{aligned}
$$
所以存在
$$
\begin{aligned}
W_{\varphi}(1,0)&=\frac{1}{\sqrt{M}}\sum_{n}f(n)\varphi_{1,0}(n)\\
&=\frac{1}{2}\left[ f(0)\varphi_{1,0}(0)+ f(1)\varphi_{1,0}(1) + f(2)\varphi_{1,0}(2) + f(3)\varphi_{1,0}(3) \right]\\
&=\frac{1}{2}\left[ 1\times \sqrt{2} + 4\times \sqrt{2}-3\times 0+ 0\times0 \right]\\
&=\frac{5\sqrt{2}}{2}
\end{aligned}
$$

$$
\begin{aligned}
W_{\varphi}(1,1)&=\frac{1}{\sqrt{M}}\sum_{n}f(n)\varphi_{1,1}(n)\\
&=\frac{1}{2}\left[ f(0)\varphi_{1,1}(0)+ f(1)\varphi_{1,1}(1) + f(2)\varphi_{1,1}(2) + f(3)\varphi_{1,1}(3) \right]\\
&=\frac{1}{2}\left[ 1\times 0 + 4\times 0-3\times  \sqrt{2}+ 0\times  \sqrt{2} \right]\\
&=-\frac{3\sqrt{2}}{2}
\end{aligned}
$$

$$
\begin{aligned}
W_{\psi}(1,0)&=\frac{1}{\sqrt{M}}\sum_{n}f(n)\psi_{1,0}(n)\\
&=\frac{1}{2}\left[ f(0)\psi_{1,0}(0)+ f(1)\psi_{1,0}(1) + f(2)\psi_{1,0}(2) + f(3)\psi_{1,0}(3) \right]\\
&=\frac{1}{2}\left[ 1\times 0 + 4\times 0-3\times \sqrt{2}+ 0\times-\sqrt{2}\right]\\
&=-\frac{3\sqrt{2}}{2}
\end{aligned}
$$

$$
\begin{aligned}
W_{\psi}(1,1)&=\frac{1}{\sqrt{M}}\sum_{n}f(n)\psi_{1,1}(n)\\
&=\frac{1}{2}\left[ f(0)\psi_{1,1}(0)+ f(1)\psi_{1,1}(1) + f(2)\psi_{1,1}(2) + f(3)\psi_{1,1}(3) \right]\\
&=\frac{1}{2}\left[ 1\times \sqrt{2} + 4\times -\sqrt{2}-3\times 0+ 0\times  0 \right]\\
&=-\frac{3\sqrt{2}}{2}
\end{aligned}
$$



(b)
$$
\begin{array}{rcl}f(x)=&\frac{1}{2}[W_\varphi(1,0)\varphi_{1,0}(x)+W_\varphi(1,1)\varphi_{1,1}(x)+\\&W_\psi(1,0)\psi_{1,0}(x)+W_\psi(1,1)\psi_{1,1}(x)]\end{array}
$$

$$
\begin{aligned}
f\left(1\right)& \begin{aligned}=\quad\frac{\sqrt{2}}{4}\left[(5)(\sqrt{2})+(-3)(0)+(-3)(\sqrt{2})+(-3)(0)\right]\end{aligned}  \\
&=\quad\frac{2(\sqrt{2})^2}4=1.
\end{aligned}
$$

