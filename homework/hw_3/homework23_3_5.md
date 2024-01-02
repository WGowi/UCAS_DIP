假设一个信号由低频与高频两部分的信号构成，我们可以通过两个滤波器与原信号进行卷积而分别获得它们。请证明在频域中这两个滤波器存在如下的关系
$$
H_{hp}=1-H_{lp}
$$
设可以将原始图像分成高频和低频两部分，即$f(x,y)=f_h(x,y)+f_l(x,y)$

设原始图像的傅里叶变换为$F(u,v)$，即$\mathfrak F[f(x,y)]=F(u,v)$
$$
\begin{aligned}
\mathfrak F[f(x,y)]
&=\mathfrak{F}[f_h(x,y)+f_l(x,y)]\\
&=\mathfrak{F}[f_h(x,y)]+\mathfrak{F}[f_l(x,y)]\\
&=F_h(u,v)+F_l(u,v)\\
&=F(u,v)*H_{hp}(u,v)+F(u,v)*H_{lp}(u,v)\\
&=F(u,v)*[H_{hp}(u,v)+H_{lp}(u,v)]\\
\end{aligned}
$$
所以存在$H_{hp}(u,v)+H_{lp}(u,v)=1$，即$H_{hp}=1-H_{lp}$

