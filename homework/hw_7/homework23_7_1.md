r，g，b是RGB彩色空间沿R,G,B轴的单位向量，定义向量$\mathrm{u}=\frac{\partial R}{\partial x}r+\frac{\partial G}{\partial x}g+\frac{\partial B}{\partial x}b$和$\mathbf{v}=\frac{\partial R}{\partial y}r+\frac{\partial G}{\partial y}g+\frac{\partial B}{\partial y}b$，$g_{xx},g_{yy},g_{xy}$定义为这些向量的点乘
$$
\begin{gathered}
\begin{aligned}g_{xx}&=\mathbf{u}\cdot\mathbf{u}=\mathbf{u}^T\mathbf{u}=\left|\frac{\partial R}{\partial x}\right|^2+\left|\frac{\partial G}{\partial x}\right|^2+\left|\frac{\partial B}{\partial x}\right|^2\end{aligned} \\
\begin{aligned}g_{yy}&=\mathbf{v\cdot v}=\mathbf{v^T}\mathbf{v}=\left|\frac{\partial R}{\partial y}\right|^2+\left|\frac{\partial G}{\partial y}\right|^2+\left|\frac{\partial B}{\partial y}\right|^2\end{aligned} \\
g_{xy}=\mathbf{u}\cdot\mathbf{v}=\mathbf{u}^{T}\mathbf{v}=\frac{\partial R}{\partial x}\frac{\partial R}{\partial y}+\frac{\partial G}{\partial x}\frac{\partial G}{\partial y}+\frac{\partial B}{\partial x}\frac{\partial B}{\partial y}
\end{gathered}
$$

推导出最大变换率方向$\theta$和$(\mathbf{x},\mathbf{y})$点在$\theta$方向上变化率的值$F(\mathbf{\theta})$




$$
\begin{aligned}
|u\cos\theta+v\sin\theta|^2
&=u^2\cos^2\theta+uv\cos\theta\sin\theta+v^2\sin^2\theta\\
&=g_{xx}\cos^2\theta+g_{xy}\cos\theta\sin\theta+g_{yy}\sin^2\theta\\
&=g_{xx}\frac{\cos2\theta+1}2+g_{yy}\frac{1-\cos2\theta}2+g_{xy}\sin2\theta\\
&=\frac12\left[\left(\mathrm{g_{xy}+g_{yy}}\right)+\left(\mathrm{g_{xx}-g_{yy}}\right)\cos2\theta+2\mathrm{g_{xy}sin2\theta}\right]
\end{aligned}
$$
所以：
$$
F({\theta})=\left\{\frac{1}{2}\Big[(g_{xx}+g_{yy})+\big(g_{xx}-g_{yy}\big)\cos2\theta(x,y)+2g_{xy}\sin2\theta(x,y)\Big]\right\}^{\frac{1}{2}}
$$


当$\frac\partial{\partial\theta}\left|u\cos\theta+v\sin\theta\right|^2=0$时$|u\cos\theta+v\sin\theta|^2$取得最大值，解得
$$
\theta=\frac12\arctan\left[\frac{2g_{xy}}{g_{xx}-g_{yy}}\right]
$$
