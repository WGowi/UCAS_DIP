证明：
$$
f(x,y)e^{j2\pi(u_ox/M+v_0y/N)}\Leftrightarrow F(u-u_0,v-v_0)\\
f(x-x_0,y-y_0)\Leftrightarrow F(u,v)e^{-j2\pi(ux_0/M+vy_0/N)}
$$
当$x_0=u_0=M/2$和$y_0=v_0=N/2$时，
$$
f(x,y)(-1)^{(x+y)}\Leftrightarrow F(u-M/2,v-N/2)\\
f(x-M/2,v-N/2)\Leftrightarrow F(u,v)(-1)^{(u+v)}
$$




对于离散型傅里叶变换：
$$
\begin{aligned}
f(x,y)&\Rightarrow F(u,v)\\
&=\sum_{x=0}^{M-1}\sum_{y=0}^{N-1}f(x,y)e^{-j2\pi(\frac{u}{M}x+\frac{v}{N}y)}
\end{aligned}
$$
对于离散型傅里叶逆变换：
$$
\frac{1}{MN}\sum_{u=0}^{M-1}\sum_{v=0}^{N-1}F(u,v)e^{j2\pi(\frac{u}{M}x+\frac{v}{N}y)}\Rightarrow f(x,v)
$$
由此计算$f(x,y)e^{j2\pi(u_ox/M+v_0y/N)}$ 的傅里叶变换
$$
\begin{aligned}
f(x,y)e^{j2\pi(u_ox/M+v_0y/N)}
&\Rightarrow \sum_{x=0}^{M-1}\sum_{y=0}^{N-1}f(x,y)e^{j2\pi(u_ox/M+v_0y/N)}e^{-j2\pi(\frac{u}{M}x+\frac{v}{N}y)}\\
&=\sum_{x=0}^{M-1}\sum_{y=0}^{N-1}f(x,y)e^{-j2\pi(\frac{u-u_0}{M}x+\frac{v-v_0}{N}y)}\\
&=F(u-u_0,v-v_0)
\end{aligned}
$$
由此计算$F(u-u_0,v-v_0)$ 的逆傅里叶变换，

令$G(u,v)=F(u-u_0,v-v_0)$，令$u'=u-u_0,v'=v-v_0$，所以$u=u'+u_0,v=v'+v_0$所以
$$
\begin{aligned}
F(u-u_0,v-v_0)&\Rightarrow\sum_{u=0}^{M-1}\sum_{v=0}^{N-1}G(u,v)e^{j2\pi(\frac{u}{M}x+\frac{v}{N}y)}\\
&=\sum_{u=u_0}^{M-1}\sum_{v=v_0}^{N-1}F(u-u_0,v-v_0)e^{j2\pi(\frac{u}{M}x+\frac{v}{N}y)}\\
&=\sum_{u'=0}^{M-1}\sum_{v'=0}^{N-1}F(u',v')e^{j2\pi(\frac{u'+u_0}{M}x+\frac{v'+v_0}{N}y)}\\
&=\sum_{u'=0}^{M-1}\sum_{v'=0}^{N-1}F(u',v')e^{j2\pi(\frac{u'}{M}x+\frac{v'}{N}y)}e^{j2\pi(\frac{u_0}{M}x+\frac{v_0}{N}y)}\\
&=f(x,y)e^{j2\pi(\frac{u_0}{M}x+\frac{v_0}{N}y)}
\end{aligned}
$$
所以$f(x,y)e^{j2\pi(u_ox/M+v_0y/N)}\Leftrightarrow F(u-u_0,v-v_0)$

由此当$x_0=u_0=M/2$和$y_0=v_0=N/2$时，$f(x,y)e^{j2\pi(u_ox/M+v_0y/N)}=f(x,y)e^{j\pi(x+y)}$，在利用欧拉公式$e^{\theta j}=\cos \theta+\sin \theta \cdot j$，所以$e^{j\pi}=-1$，由此$f(x,y)(-1)^{(x+y)}\Leftrightarrow F(u-M/2,v-N/2)$

计算$f(x-x_0,y-y_0)$的傅里叶变换，令$x'=x-x_0,y'=y-y_0$，所以$x=x'+x_0,y=y'+y_0$
$$
\begin{aligned}
f(x-x_0,y-y_0)&\Rightarrow\sum_{x'=0}^{M-1}\sum_{y'=0}^{N-1}f(x',y')e^{-j2\pi(\frac{u}{M}x+\frac{v}{N}y)}\\
&=\sum_{x'=0}^{M-1}\sum_{y'=0}^{N-1}f(x',y')e^{-j2\pi(\frac{u}{M}(x'+x_0)+\frac{v}{N}(y'+y_0))}\\
&=\sum_{x'=0}^{M-1}\sum_{y'=0}^{N-1}f(x',y')e^{-j2\pi(\frac{u}{M}x'+\frac{v}{N}y')}e^{-j2\pi(\frac{u}{M}x_0+\frac{v}{N}y_0)}\\
&= F(x,y)e^{-j2\pi(\frac{u_0}{M}x+\frac{v_0}{N}y)}
\end{aligned}
$$
计算$F(u,v)e^{j2\pi(\frac{u_0}{M}x+\frac{v_0}{N}y)}$的逆傅里叶变换，令$u'=u+u_0,v'=v+v_0$
$$
\begin{aligned}
F(u,v)e^{j2\pi(u_ox/M+v_0y/N)}&\Rightarrow \frac{1}{MN}\sum_{u=0}^{M-1}\sum_{v=0}^{N-1}F(u,v)e^{j2\pi(\frac{u_0}{M}x+\frac{v_0}{N}y)}e^{j2\pi(\frac{u}{M}x+\frac{v}{N}y)}\\
&=\frac{1}{MN}\sum_{u=0}^{M-1}\sum_{v=0}^{N-1}F(u,v)e^{j2\pi(\frac{u+u_0}{M}x+\frac{v+v_0}{N}y)}\\
&=\frac{1}{MN}\sum_{u=0}^{M-1}\sum_{v=0}^{N-1}F(u'-u_0,v-v_0)e^{j2\pi(\frac{u'}{M}x+\frac{v'}{N}y)}\\
&=f(x-x_0,y-y_0)
\end{aligned}
$$
当$x=u_0=M/2$和$y=v_0=N/2$时

$f(x-\frac{M}{2},y-\frac{M}{2})\Leftrightarrow F(u,v)e^{j\pi(x+y)}=F(u,v)(-1)^{(u+v)}$



