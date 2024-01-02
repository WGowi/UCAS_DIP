说明尺度函数：
$$
\varphi(x)=\begin{cases}1&{0.25}\leqslant x<0.75\\0&\text{其他}\\\end{cases}
$$
并未满足多分辨率分析的第二个要求。

简单尺度函数应符合多分辨率分析的四个条件

1.  **MRA要求1：**其中对于不同整数平移的简单尺度函数应是正交的
2.  **MRA要求2：**低尺度函数跨越的子空间应嵌入到高尺度跨越的子空间内
3.  **MRA要求3：**唯一对于所有$V_j$的通用的函数是$f(x)=0$
4.  **MRA要求4：**任何函数都可以任意精度表示

若$\varphi(x)$满足MRA 2，即低分辨率的尺度函数可以用高分辨率的尺度函数表示。即存在如下表达
$$
\varphi(x)=\sum_{n}h_{\varphi}(n)\sqrt{2}\varphi(2x-n)
$$
可得
$$
\sqrt{2}\varphi(2x)=\begin{cases}\sqrt{2}&{0.125}\leqslant x<0.375\\0&\text{其他}\\\end{cases}
$$

$$
\sqrt2\varphi(2x-1)=\begin{cases}\sqrt{2}&{0.625}\leqslant x<0.875\\0&\text{其他}\\\end{cases}
$$



但是无法构造函数$h_{\varphi}(n)$使得$\varphi(x)=\sum_{n}h_{\varphi}(n)\sqrt{2}\varphi(2x-n)$成立，所以尺度函数$\varphi(x)$未满足多分辨率分析的第二个要求