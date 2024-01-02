完美重建滤波器的双正交性的数学定义是什么？请证明其中的第二个式子与课本中第四个式子

因为
$$
\left.\left[\begin{array}{c}{G_{0}(z)}\\{G_{1}(z)}\\\end{array}\right.\right]=\frac{2}{\det(\mathbf{H}_{m}(z))}\begin{bmatrix}{H_{1}(-z)}\\{-H_{0}(-z)}\\\end{bmatrix}
$$
可得:
$$
G_0(z)=\frac{2}{\det(H_m(z))}H_1(-z)\\
G_1(z)=\frac{-2}{\det(H_m(z))}H_0(-z)\\
H_0(-z)=-\frac{\det(H_m(z))}{2}G_1(z)\\
H_1(-z)=\frac{\det(H_m(z))}{2}G_0(z)
$$
可得：
$$
H_0(z)G_0(z)=\frac{2}{\det(H_m(z))}H_1(-z)H_0(z)=P(z)\\
H_1(z)G_1(z)=\frac{-2}{\det(H_m(z))}H_1(z)H_0(-z)=P(-z)\\
$$
又因为$\det(\mathbf{H}_{m}(z))=-\det(\mathbf{H}_{m}(-z))$

所以存在$G_{0}(z)H_{0}(z)=P(z)=G_{1}(-z)H_{1}(-z)$

因为完美重建滤波器应满足
$$
\begin{aligned}H_0(-z)G_0(z)+H_1(-z)G_1(z)&=0\\\\H_0(z)G_0(z)+H_1(z)G_1(z)&=2\end{aligned}
$$
所以存在
$$
H_1(z)G_1(z)+G_{1}(-z)H_{1}(-z)=2
$$
对其采用逆Z变换：
$$
\begin{aligned}
2\delta(n)
&=Z^{-1}[H_1(z)G_1(z)+G_{1}(-z)H_{1}(-z)]\\
&=\sum_kh_1(k)g_1(n-k)+g_1(n-k)h_1(-k)\\
&=\sum_kh_1(k)g_1(n-k)+(-1)^ng_1(n-k)h_1(k)
\end{aligned}
$$
当n为偶数时$(-1)^n=1$
$$
h_1(k)g_1(n-k)+(-1)^ng_1(n-k)h_1(k)=2g_1(n-k)h_1(k)
$$
当n为奇数时$(-1)^n=-1$
$$
h_1(k)g_1(n-k)+(-1)^ng_1(n-k)h_1(k)=0
$$
于是可以简化为
$$
\sum_kg_1(k)h_1(2n-k)=<g_1(k),h_1(2n-k)>=\delta(n)
$$

同理

可以使用$H_0$与$G_0$表示成$H_1$与$G_0$的函数可得
$$
\langle g_{1}(k),h_{0}(2n-k)\rangle=0
$$
