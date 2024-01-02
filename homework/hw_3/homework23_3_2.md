观察如下所示图像。右边的图像这样得到: (a)在原始图像左边乘以$(-1)^{x+y}$；(b) 计算离散傅里叶变换(DFT); (c) 对变换取复共轭; (d) 计算傅里叶反变换; (d) 结果的实部再乘以$(-1)^{x+y}$  。(用数学方法解释为什么会产生右图的效果。)

![image-20231028162932913](https://gowi-picgo.oss-cn-shenzhen.aliyuncs.com/202310281629220.png)

设源图像为$f(x,y),g(x,y)=(-1)^{x+y}$

(a)：

$f(x,y)\cdot g(x,y)$

(b):

$\mathcal F(f(x,y)\cdot g(x,y))=F(x,y)*G(x,y)$
$$
\begin{aligned}
\mathcal{F}(f(x,y)\cdot g(x,y))
&=\sum_{x=0}^{M-1}\sum_{y=0}^{N-1}f(x,y)\cdot(-1)^{x+y}e^{-j2\pi(\frac{u}{M}x+\frac{v}{N}y)} \\
&=\sum_{x=0}^{M-1}\sum_{y=0}^{N-1}f(x,y)\cdot e^{j\pi(x+y)}e^{-j2\pi(\frac{u}{M}x+\frac{v}{N}y)}\\
&=\sum_{x=0}^{M-1}\sum_{y=0}^{N-1}f(x,y)\cdot e^{-j2\pi[(\frac{u}{M}-\frac{1}{2})x+(\frac{v}{N}-\frac{1}{2})y]}\\
&=\sum_{x=0}^{M-1}\sum_{y=0}^{N-1}f(x,y)\cdot e^{-j2\pi[(\frac{u-\frac{1}{2}M}{M})x+(\frac{v-\frac{1}{2}N}{N})y]}\\
&=F(u-\frac{1}{2}M,v-\frac{1}{2}N)
\end{aligned}
$$
由此实现了频谱中心化

(c)
$$
\begin{aligned}
F^{*}(u-\frac{1}{2}M,v-\frac{1}{2}N)&=F(-(u-\frac{1}{2}M),-(u-\frac{1}{2}N))\\
&=F(\frac{1}{2}M-u,\frac{1}{2}N-v)
\end{aligned}
$$
(d)


$$
IDFT(F(\frac{1}{2}M-u,\frac{1}{2}N-v))=(-1)^{(x+y)}f(-x,-y)
$$

$$
(-1)^{(x+y)}f(-x,-y)\times (-1)^{(x+y)}=f(-x,-y)
$$






