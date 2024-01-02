请根据课本中Z变换的定义，证明如下结论。

(1) 若$\mathrm {x(n)}$的Z变换$X(\mathrm z)$，则$(-1)^\mathrm n\mathrm x(n)$的Z变换为$\mathrm {X(-z)}$  

(2) 若$\mathrm {x(n)}$的Z变换$X(\mathrm z)$，则$\mathrm x(\mathrm {-n})$的Z变换为$\mathrm {X(\frac{1}{z})}$  

(3)  若$\mathrm {x(n)}$的Z变换$X(\mathrm z)$，课本280页公式7.1.2 


$$
X(z)=\sum_{-\infty}^\infty x(n)z^{-n}
$$
(1)

设信号$y(n)=(-1)^\mathrm n\mathrm x(n)$，则存在Z变换：
$$
\begin{aligned}
Y(z)
&=\sum_{-\infty}^\infty y(n)z^{-n}\\
&=\sum_{-\infty}^\infty y(n)z^{-n}\\
&=\sum_{-\infty}^\infty(-1)^n x(n)z^{-n}
\end{aligned}
$$
当n=2k+1时，$(-1)^n x(n)z^{-n}=-x(n)z^{-n}=x(n){(-z)}^{-n}$

当n=2k时，$(-1)^n x(n)z^{-n}=x(n){(-z)}^{-n}$

所以:$(-1)^n x(n)z^{-n}=x(n){(-z)}^{-n}$

即：
$$
\begin{aligned}
Y(z)
&=\sum_{-\infty}^\infty y(n)z^{-n}\\
&=\sum_{-\infty}^\infty y(n)z^{-n}\\
&=\sum_{-\infty}^\infty(-1)^n x(n)z^{-n}\\
&=\sum_{-\infty}^\infty x(n){(-z)}^{-n}\\
&=\mathrm {X(-z)}
\end{aligned}
$$


(2)

设信号$y(n)=x(-n)$，则存在Z变换：
$$
\begin{aligned}
Y(z)
&=\sum_{-\infty}^\infty y(n)z^{-n}\\
&=\sum_{-\infty}^\infty x(-n)z^{-n}\\
\end{aligned}
$$
令$t=-n$，则存在：
$$
\begin{aligned}
Y(z)
&=\sum_{-\infty}^\infty y(n)z^{-n}\\
&=\sum_{-\infty}^\infty x(-n)z^{-n}\\
&=\sum_{-\infty}^\infty x(t)z^{-(-t)}\\
&=\sum_{-\infty}^\infty x(t)({\frac{1}{z}})^{(-t)}\\
&=X(\frac{1}{z})
\end{aligned}
$$


(3)

对信号$x(n)$进行下采样处理，则可以得到$x_{\mathrm{dowm}}(n)=x(2n)$

设信号$y(n)=x_{\mathrm{dowm}}(n)$，则存在Z变换：
$$
\begin{aligned}
Y(z)
&=\sum_{-\infty}^\infty y(n)z^{-n}\\
&=\sum_{-\infty}^\infty x_{down}(n)z^{-n}\\
&=\sum_{-\infty}^\infty x(2n)z^{-n}\\
\end{aligned}
$$
令$t=2n$ ，则存在
$$
\begin{aligned}
Y(z)
&=\sum_{-\infty}^\infty x(2n)z^{-n}\\
&=\sum_{-\infty}^\infty x(t)z^{-\frac{t}{2}}
\end{aligned}
$$
因为$t=2n$为偶数，但是此时$t$为所有整数，所以应该保证$t$为奇数是为0

所以构造
$$
\begin{aligned}
Y(z)
&=\frac{1}{2}\left[\sum_{-\infty}^\infty x(t)z^{-\frac{t}{2}} +\sum_{-\infty}^\infty (-1)^{(t)} x(t)z^{-\frac{t}{2}}\right]\\
&=\frac{1}{2}\left[\sum_{-\infty}^\infty x(t)(z^{-\frac{1}{2}})^t +\sum_{-\infty}^\infty (-1)^{(t)} x(t)(z^{-\frac{1}{2}})^t\right]\\
&=\frac{1}{2}\left[\sum_{-\infty}^\infty x(t)(z^{-\frac{1}{2}})^t +\sum_{-\infty}^\infty x(t)((-z)^{-\frac{1}{2}})^t\right]\\
&=\frac{1}{2}[X(z^{\frac{1}{2}})+X(-z^{-\frac{1}{2}})]
\end{aligned}
$$
