 高斯型低通滤波器在频域中的传递函数是
$$
H(u,v)=Ae^{-(u^2+v^2)/2\sigma^2}
$$
根据二维傅里叶性质，证明空间域的相应滤波器形式为
$$
h(x,y)=A2\pi\sigma^2 e^{-2\pi^2\sigma^2(x^2+y^2)}
$$
（这些闭合形式只适用于连续变量情况。）

在证明中假设已经知道如下结论：函数$e^{-\pi(x^2+y^2)}$的傅立叶变换为$e^{-\pi(u^2+v^2)}$。



证明:

令$u=\sqrt{2\pi} u'\sigma,v=\sqrt{2\pi} v'\sigma,x'=\sqrt{2\pi} x\sigma,y'=\sqrt{2\pi} y\sigma$
$$
\begin{aligned}
&\quad\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}Ae^{\frac{-(u^2+v^2)}{2\sigma^2}}\cdot e^{j2\pi(ux+vj)}dudv\\
&=\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}Ae^{\frac{-2\pi(u'^2\sigma^2+v'^2\sigma^2)}{2\sigma^2}}\cdot e^{j2\pi(\sqrt{2\pi} u'\sigma x+\sqrt{2\pi} v'\sigma y)}2\sigma^2\pi du'dv'\\
&=2A\pi\sigma^2\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}e^{-\pi(u'^2+v'^2)}\cdot e^{j2\pi(\sqrt{2\pi} u'\sigma x+\sqrt{2\pi} v'\sigma y)}du'dv'\\
&=2A\pi\sigma^2\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}e^{-\pi(u'^2+v'^2)}\cdot e^{j2\pi(\sqrt{2\pi} u'\sigma x+\sqrt{2\pi} v'\sigma y)}du'dv'\\
&=2A\pi\sigma^2\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}e^{-\pi(u'^2+v'^2)}\cdot e^{j2\pi(u'\sqrt{2\pi}\sigma x+ v'\sqrt{2\pi}\sigma y)}du'dv'\\
&=2A\pi\sigma^2\int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}e^{-\pi(u'^2+v'^2)}\cdot e^{j2\pi(u'x'+ v'y')}du'dv'\\
&=2A\pi\sigma^2e^{-\pi(x'^2+y'^2)}\\
&=2A\pi\sigma^2e^{-\pi(2\pi \sigma^2x^2+2\pi \sigma^2y^2)}\\
&=2A\pi\sigma^2e^{-2\pi^2 \sigma^2(x^2+y^2)}
\end{aligned}
$$
