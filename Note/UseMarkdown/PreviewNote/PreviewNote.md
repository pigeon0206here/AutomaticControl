# Preview NOte of Course Automation Control
(算是那什么tex版本的outline)(或者随便什么)

## 拉氏变换
拉氏变换与傅氏变换之间很有意思的一点,就是拉氏变换相当于把要变换的函数乘以一个指数项后,再进行傅氏变换.
> 补充一下傅氏变换与拉氏变换的公式:
> $$F(\omega)=\mathscr{F}[f(t)]=\int_{-\infty}^{\infty}f(t)e^{-j\omega t}\,\mathrm{d} t $$
> $$F(s)=\mathscr{L}[f(t)]=\int_{-\infty}^{\infty}f(t)e^{-st}\,\mathrm{d}t $$

> 那什么的拉普拉斯变换符号:
> - `\mathscr{L}`: $\mathscr{L}$
> - `\mathcal{L}`: $\mathcal{L}$
> 
> 那什么的微分算符:
> - 知乎老哥的讨论:[关于 LaTeX 中的微分算符 d](https://zhuanlan.zhihu.com/p/413407561)
> - 直接用 `\,\mathrm{d}` : $\,\mathrm{d}$
> - (注: `\`, 是用来保持前面的空格的,效果大概是: $x\,\mathrm{d} x$)

例:

对于单位阶跃函数$f(t)=1(t)$的傅氏变换,可以得到:
$$F(\omega) = \mathscr{L}[f(t)] = \int_{-\infty}^{\infty} f(t)e^{-j\omega t} \,\mathrm{d} t = \frac{1}{\omega}(\sin \omega t+\cos \omega t) \bigg|_{0}^{\infty} $$

根据傅氏变换,由于在对单位阶跃函数积分时,会有 $\int_{-\infty }^{\infty }|f(t)|  \,\mathrm{d}t$ 不存在,无法满足狄利克雷的第三条件, $F(\omega)$无法计算出来.
> 狄利克雷的条件们:
> 
> 前提: $f(t)$是周期为$T$的任一周期函数.
>   1. 在一个周期内只有有限个不连续点;
>   2. 在一个周期内只有有限个极大和极小值;
>   3. 积分$\int_{-\frac{T}{2}}^{\frac{T}{2}}|f(t)|\,\mathrm{d}t$存在.
> 说人话就是,能够使用傅里叶变换的函数要有**有限个间断点,有限个极值,以及在$\mathbb{R}$上绝对可积**.

~~于是为了解决这个问题,就有人天才的想到,把$1(t)$给换掉,换成近似是这个函数但是在$\mathbb{R}$上绝对可积的函数.同小信号模型类似,在这里,先人们再一次使用了*近似替代*的思想.~~

 
`找了些视频来看,发现拉氏变换不是简单的把被变换函数进行变形使之能够满足傅氏变换的条件,而是将傅氏变换的结果,直接进行了从实数域到复数域的扩充.拉普拉斯非常天才的一个人.`

贴个视频链接:[【数形结合】拉普拉斯变换](https://www.bilibili.com/video/BV1sJ411i75s/?spm_id_from=333.999.0.0&vd_source=68d8620341ca4ad2fdc113a5c58f1f5e)
$\scriptsize{\leftarrow\color{grey}{这个视频从二维拓展到三维,数形结合地展示了拉普拉斯变换的过程.}}$
> 做些视频内容的笔记:
> - 傅氏变换展现了函数中含有哪些正弦波,拉氏变换则展现了函数中有哪些正弦波与衰减函数.二者呈现出包含关系,也就是有:$\scriptsize{傅氏变换\subseteq 拉氏变换}$
> - 

拉氏变换中,$f(t)$后所乘的数从$e^{-j\omega t}$变为了$e^{-s t}$,在这之中,$s=\alpha+j\omega$.