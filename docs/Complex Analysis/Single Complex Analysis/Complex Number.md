---
comments: true
---
# 复数及其性质
## 复数的定义与代数运算
>[!note] 定义：复数
>设 $x,y$ 为实数，则 $z=x+yi$ 为**复数**，其中 $i$ 为**虚数单位**，满足 $i^2=-1$ .

对于一个复数，记 $\mathrm{Re} z$ 为 $z$ 的**实部**，$\mathrm{Im}z$ 为 $z$ 的**虚部**，这里符号来源于英文 Real Part 和 Imaginary Part. 复数全体记为 $\mathbb{C}$ .

>[!example] 复数的性质
>+ 交换律（加法与乘法）
>+ 结合律（加法与乘法）
>+ 分配律

>[!example] 复数相关的定理
>- 存在加法零元0与乘法单位元1.
>- 存在加法相反数 $-z$ .
>- 存在乘法逆元 $z^{-1}$ 使得 $zz^{-1}=1$ .
>- 若 $z_1z_2=0$ 则 $z_1=0$ 或 $z_2=0$ .



## 复数的几何意义、模、共轭复数

从几何意义上来看，一个复数对应了复平面上的一个点 $z=x+y \mathrm{i} \to (x,y)$ . 这也就是说可以利用向量的观点看待复数。

复数的模定义如下：

>[!note] 复数的模
>复数 $z$ 的**模**或者**绝对值**定义为 $|z|=\sqrt{x^2+y^2}$ .

有的教材也会直接定义为：
$$
|z| = \sqrt{z\overline{z}}
$$

有了模的概念就可以考虑定义复数列的极限，从而为复分析打下基础：
>[!note] 复数列的极限
>若 $a$ 和 $\{z_n\}_{n\geqslant1}$ 都是复数并且  $$ \lim_{n\to\infty}|z_n-a|=0 $$ 则称 $\{z_n\}_{n\geqslant1}$ 收敛于 $a$ . 记为 $\displaystyle\lim_{n\to\infty}z_n=a$ 或者 $z_n\to a$ .

尝试改写为 $\varepsilon-N$ 语言：对于 $\forall\varepsilon>0$ , $\exists N>0$ , $\forall n>N$ , 有 $|z_n-a|<\varepsilon$ . 

和实数列一样，收敛复数列必**有界**，用符号表示为：如果 $\{z_n\}_{n\geqslant 1}$ 收敛，那么存在 $\exists M>0$ 使得对于 $\forall n\geqslant1$ 都有 $|z_n|\leqslant M$ .

下面定义共轭复数：
>[!note] 共轭复数
>对于一个复数 $z=x+y \mathrm{i}$ ，那么其共轭复数为 $\bar{z}=x-y \mathrm{i}$ .

在几何意义上，这两个复数关于 $x$ 轴对称。

共轭复数有下面的计算性质：
>[!example] 共轭复数的运算性质
>-  $$ \begin{aligned}\overline{z_1\pm z_2}=\overline{z_1}\pm\overline{z_2},\overline{z_1z_2}=\overline{z_1}\overline{z_2},\overline{\left(\frac{z_1}{z_2}\right)}=\frac{\overline{z_1}}{\overline{z_2}}\end{aligned} $$ 
>-  $$ \mathrm{Re}\,z=\frac{1}{2}(z+\overline{z}),\mathrm{Im}\,z=\frac{z-\overline{z}}{2\mathrm{i}}=\frac{-\mathrm{i}}{2}(z-\overline{z}) $$ 
>-  $$ |z|^2=z \overline{z} $$ 
>-  $$ |z_1z_2|=|z_1||z_2|,\left|\frac{z_1}{z_2}\right|=\frac{|z_1|}{|z_2|} $$ 
>-  $$ ||z_1|-|z_2||\leqslant|z_1+z_2|\leqslant|z_1|+|z_2| $$ 

## 复数的极坐标表示
### 三角形式和Euler公式
利用极坐标 

$$ 
\begin{cases}x=r\cos\theta \\
y=r\sin\theta\end{cases}
$$

有复数的三角形式：$z=r(\cos\theta+\mathrm{i}\sin\theta)$ . 在教材上，作者随后引出了欧拉公式：

$$ 
\mathrm{e}^{\mathrm{i}\theta}=\cos\theta+\mathrm{i}\sin\theta
$$

但是并没有给出证明，或者说这个地方本来可以在良定义指数与三角函数之后自然导出，但是你开课程设计导致没办法理解这个东西😅。这个地方在本笔记中使用幂级数进行验证。

考虑 $\mathrm{e}$ 在 0 处的Taylor展开：

$$ 
\mathrm{e}^x=1+x+\frac{x^2}{2}+\cdots+\frac{x^n}{n!}+\cdots
$$

代入 $x=i\theta$ 有：
$$ 
\mathrm{e}^{\mathrm{i}\theta}=1+\mathrm{i}\theta+\frac{(\mathrm{i}\theta)^2}{2!}+\frac{(\mathrm{i}\theta)^3}{3!}+\cdots
$$ 
使用三角函数的幂级数展开即可一一对应。

引入欧拉公式之后，我们从而推得：
>[!NOTE] 复数的极坐标形式
>  $$ z=r \mathrm{e}^{\mathrm{i}\theta}\tag{1} $$ 

公式(1)就是复数的极坐标形式，其中 $r=|z|$ ，$\theta$ 为 $z$ 的幅角（Phase Angle, Argument），记为 $\mathrm{Arg}\,z$ . 我们根据周期性可以发现 $\theta$ 显然不唯一，因此 $\mathrm{Arg}\,z$ 是一个**集合**。为了确定唯一的一个幅角，可以取一个长度为 $2\pi$ 的区间，再取其中的一个幅角，规定为**幅角主值**。

复数计算的几何意义就非常明确了，复数相乘则有对应辐角相加，对应模相乘。

有了 Euler 公式，实际上我们也不需要再对 de Moivre 公式作解释：

$$
(\cos \theta+ \mathrm{i} \sin \theta)^n = \cos n \theta+ \mathrm{i}\sin n \theta
$$

### $n$ 次单位根
对方程
$$
z^n = 1
$$
使用 Euler 公式可以得到 $n$ 个解：

$$
w_k = \exp\left(\mathrm{i}\frac{2k \pi}{n}\right)
$$

那么对于复数的开根，以此类推，如果要对下面的复数开 $n$ 次方根：
$$
z = r\mathrm{e}^{\mathrm{i}\theta} 
$$
那么解其实能直接写出来：
$$
w_k = \sqrt[n]{r}\exp\left(\mathrm{i}\frac{\theta+2k \pi}{n} \right)
$$



## 推广复平面与Riemann球面

![Riemann球面](../../imgs/复数及其性质/复数及其性质-20231218.png){width="500"}

在这里，考虑将 $\infty$ 考虑为一个“数”，那么我们就可以将复平面（复数全体）扩展为 $\mathbb{C}_\infty=\mathbb{C}\cup\{\infty\}$ . 上图表示了其几何意义（Riemann球面）。

设单位球为 $S=\{(u,v,w)|u^2+v^2+w^2=1\}$ ，顶点 $(0,0,1)$ 为 $N$ ，当球面上的任意点 $Z$ 在球面上移动的时候，$NZ$ 与 $uOv$ 平面的交点为 $(x,y,0)$ ，这就与复平面上的一个点**一一对应**了。特殊情形是 $N$ 点与 $\infty$ 对应。这个球面也称为**Riemann球面**。

这种投影的方法又叫**球极投影**。



## 与微分方程之间的联系
在常系数线性微分方程当中，如果我们有如下形式的方程：
$$
a_n y^{(n)}+a_{n-1}y^{(n-1)}+\cdots+a_1y' =0
$$
也就是常系数齐次线性方程，那么我们设函数 $y = \mathrm{e}^{\lambda x}$ ，那么代入有：
$$
\mathrm{e}^{\lambda x}(a_n \lambda^{n-1} +\cdots +a_2 \lambda+a_1 )=0
$$
这里我们发现括号内的是一个 $n-1$ 次的多项式，自然我们可以得到复解：
$$
\mathrm{e}^{\alpha+ \mathrm{i}\beta}, \mathrm{e}^{\alpha- \mathrm{i} \beta}
$$
如果我们想要得到实解，我们利用 Euler 公式展开就能消掉虚部。



