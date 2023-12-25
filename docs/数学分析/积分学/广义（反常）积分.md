---
comments: true
---
# 广义积分
## 无穷区间上的广义积分
### 无穷区间广义积分定义
>[!note] 定义：广义（反常）积分收敛
>设函数 $f(x)$ 在 $[a,+\infty)$ 上有定义，对任何实数 $A>a$ 函数在 $[a,A]$ 上可积，如果极限
> $$ \lim_{A\to +\infty}\int_{a}^A f(x)\mathrm{d}x=I $$
>存在，则称 $f(x)$ 在 $[a,+\infty)$ 上的**广义（或反常）积分收敛**，并称 $I$ 为广义积分的值，记为
> $$ \int_{a}^{+\infty}f(x)\mathrm{d}x=\lim_{A\to +\infty}\int_a^A f(x)\mathrm{d}x=I $$
>否则称广义积分发散，若 $\displaystyle\lim_{A\to +\infty}\int_a^A f(x)\mathrm{d}x=+\infty$ 或者 $-\infty$ 时，则称发散到 $+\infty$ （或者 $-\infty$）.



>[!note] 定义：$(-\infty,+\infty)$ 上的广义积分
>设对任何满足 $A'<A$ 的实数 $A$ 和 $A'$ ，函数 $f(x)$ 都在 $[A',A]$ 上可积，如果**存在实数** $a$，使得广义积分 $\displaystyle\int_{-\infty}^a f(x)\mathrm{d}x$ 和 $\displaystyle\int_{a}^{+\infty} f(x)\mathrm{d}x$ **都收敛**，则称广义积分 $\displaystyle\int_{-\infty}^{+\infty}f(x)\mathrm{d}x$ 收敛，且有
> $$ \int_{-\infty}^{+\infty} f(x)\mathrm{d}x=\int_{-\infty}^{a}f(x)\mathrm{d}+\int_{a}^{+\infty} f(x)\mathrm{d}x. $$
>否则，当上式右端两个广义积分**至少有一个发散**，就称广义积分 $\displaystyle\int_{-\infty}^{+\infty}f(x)\mathrm{d}x$ 发散。


### 无穷区间广义积分性质
#### 线性运算
>[!note] 定理：收敛广义积分可线性运算
>如果广义积分 $\displaystyle\int_{a}^{+\infty} f(x)\mathrm{d}x$ 和 $\displaystyle\int_{a}^{+\infty}g(x)\mathrm{d}x$ 都收敛，$\lambda,\mu\in \mathbb{R}$ ，则广义积分 $\displaystyle\int_{a}^{+\infty}[\lambda f(x)+\mu g(x)]\mathrm{d}x$ 也收敛，且有
> $$ \int_{a}^{+\infty}[\lambda f(x)+\mu g(x)]\mathrm{d}x=\lambda \int_{a}^{+\infty}f(x)\mathrm{d}x+\mu \int_{a}^{+\infty}g(x)\mathrm{d}x. $$

>[!note] 定理：广义积分积分域可加
>设实数 $a<b$ 则广义积分 $\displaystyle\int_a^{+\infty}f(x)\mathrm{d}x$ 和 $\displaystyle\int_b^{+\infty} f(x)\mathrm{d}x$ 同时收敛或同时发散，收敛时有
> $$ \int_{a}^{+\infty}f(x)\mathrm{d}x=\int_a^b f(x)\mathrm{d}x+\int_{b}^{+\infty}f(x)\mathrm{d}x $$


#### 微积分基本公式和分部积分公式
>[!note] 定理：广义积分的Newtom-Leibniz公式
>设对任何实数 $A>a$ 函数 $f(x)$ 都在 $[a,A]$ 上可积，$F(x)$ 是 $f(x)$ 在 $[a,+\infty]$ 上的一个原函数，则广义积分 $\displaystyle\int_a^{+\infty}f(x)\mathrm{d}x$ 收敛当且仅当 $F(+\infty)$ 存在，且广义积分收敛或或 $F(+\infty)$ 存在时，有
> $$ \int_{a}^{+\infty}f(x)\mathrm{d}x=F(+\infty)-F(a) $$


>[!note] 定理：分部积分公式
>设 $F(x)$ 和 $g(x)$ 都在 $[a,+\infty]$ 上连续可导，且 $F'(x)=f(x)$. 如果下面的等式中有两项存在，则第三项存在且有
> $$ \int_{a}^{+\infty}f(x)g(x)\mathrm{d}x=[F(x)g(x)]\bigg|_a^{+\infty}-\int_a^{+\infty}F(x)g'(x)\mathrm{d}x $$

我们此处还没有说明广义积分的换元，因此还没有 $f(x)\mathrm{d}x = \mathrm{d}F(x)$ 的写法. 在后续说明了之后，就能换成习惯的写法了.



### 积分第二中值定理
在进行敛散性判定法的记录之前，先考虑积分第二中值定理：
>[!note] 定理：积分第二中值定理
>设 $f(x)$ 在 $[a,b]$ 上可积：
>1. 若 $g(x)$ 在 $[a,b]$ 上非负递增，则存在 $\xi\in[a,b]$ 使得 $$ \int_a^bf(x)g(x)\mathrm{d}x=g(b)\int_\xi^bf(x)\mathrm{d}x $$
>2. 若 $g(x)$ 在 $[a,b]$ 上非负递减，则存在 $\xi\in[a,b]$ 使得 $$ \int_a^bf(x)g(x)\mathrm{d}x=g(a)\int_a^\xi f(x)\mathrm{d}x $$
>3. 若 $g(x)$ 在 $[a,b]$ 上单调，则存在 $\xi\in[a,b]$ 使得 $$ \int_a^bf(x)g(x)\mathrm{d}x=g(b)\int_\xi^bf(x)\mathrm{d}x+g(a)\int_a^\xi f(x)\mathrm{d}x $$

积分第二中值定理在之后将会发挥和 Abel 求和公式类似的作用。

首先考虑 (1) 的证明：

$$
\begin{aligned}
\int_a^b f(x)g(x)\mathrm{d}x &= \sum\limits_{k=1}^n\int_{x_{k}}^{x_{k+1}}f(x)g(x)\mathrm{d}x\\\\
&=\sum\limits_{k=1}^n g(x_k)\int_{x_k}^{x_{k+1}}f(x)\mathrm{d}x+\\\\
&\sum\limits_{k=1}^n \int_{x_k}^{x_{k+1}}f(x)[g(x)-g(x_k)]\mathrm{d}x
\end{aligned}
$$

其中第二项为误差，估计误差有

$$
\begin{aligned}
\sum\limits_{k=1}^n \int_{x_k}^{x_{k+1}}f(x)[g(x)-g(x_k)]\mathrm{d}x &\leqslant \sum\limits_{k=1}^n\int_{x_k}^{x_{k+1}}|f(x)|\cdot|g(x)-g(x_k)|\\\\
&\leqslant L\sum\limits_{k=1}^n \omega_k \Delta x_k
\end{aligned}
$$

由于 $g(x)$ 可积，上面的误差自然趋于0.

对于第一项，设 $F(x)=\displaystyle\int_{x}^b f(x)\mathrm{d}x$ ，那么 $\displaystyle\int_{x_k}^{x_{k+1}}f(x)\mathrm{d}x=F(x_{k})-F(x_{k+1})$ . 利用 Abel 求和公式有 

$$
\begin{aligned}
\sum\limits_{k=1}^n g({x_k})\int_{x_k}^{x_{k+1}} f(x)\mathrm{d}x& =\sum_{k=1}^ng(x_k)[F(x_{k-1})-F(x_k)]  \\\\
&=g(x_1)F(x_0)+\sum_{k=1}^{n-1}[g(x_{k+1})-g(x_k)]F(x_k).
\end{aligned}
$$

由于 $F(x)$ 连续，必有最小值 $m$ 和最大值 $M$ ，从而有：

$$
mg(b)\leqslant \sum\limits_{k=1}^n g({x_k})\int_{x_k}^{x_{k+1}} f(x)\mathrm{d}x\leqslant Mg(b)
$$

利用介值定理，存在 $\xi\in [a,b]$ 使得
$$
\int_a^b f(x)g(x)\mathrm{d}x= F(\xi) g(b)= g(b)\int_\xi ^b f(x)\mathrm{d}x
$$

从而 (1) 成立。

### 无穷区间广义积分敛散性判定
上面的无穷区间广义积分的运算性质很大程度上要依赖于广义积分收敛，因此判断广义积分收敛性就成为必须要面对的一个问题。
首先是应用较广的 Cauchy 收敛原理：

>[!note] 定理：Cauchy收敛原理
>广义积分 $\displaystyle\int_a^{+\infty}f(x)\mathrm{d}x$ 收敛的充要条件是：对任何 $\varepsilon>0$ 都存在 $M>a$ 使得当 $A'>A>M$ 时就有
> $$ \left|\int_{A}^{A'}f(x)\mathrm{d}x\right|<\varepsilon $$

从级数的 Cauchy 收敛的应用范围来看， Cauchy 收敛原理还是需要重点关注的。

#### 比较判别法

>[!note] 定理：比较判别法
>设对于任何 $A>a$ 函数 $f(x)$ 和 $g(x)$ 都在 $[a,A]$ 上可积，且存在 $b\geqslant a$ 使得 $g(x)\geqslant f(x)\geqslant 0(\forall x\geqslant b)$ ，那么有：
>1. 若 $\displaystyle\int_{a}^{+\infty} g(x)\mathrm{d}x$ 收敛，则 $\displaystyle\int_{a}^{+\infty}f(x)\mathrm{d}x$ 也收敛；
>2. 若 $\displaystyle\int_{a}^{+\infty} f(x)\mathrm{d}x$ 发散则 $\displaystyle\int_{a}^{+\infty}g(x)\mathrm{d}x$ 也发散。

这里和级数的敛散性非常类似，简单概括就是：对于非负函数广义积分，小于收敛积分则积分收敛，大于发散积分则积分发散.

#### 柯西判别法
>[!note] 定理：Cauchy判别法
>设函数 $f(x)$ 在 $[a,+\infty)$ 上非负且对任何 $A>a,f(x)$ 在 $[a,A]$ 上可积，那么：
>1. 若存在 $p>1$ 和 $C>0$，使得在 $[a,+\infty)$ 上有 $\displaystyle0\leqslant f(x)\leqslant \frac{C}{x^p}$ ，则广义积分 $\displaystyle\int_a^{+\infty}f(x)\mathrm{d}x$ 收敛；
>2. 若存在 $0<p\leqslant 1$ 和 $C>0$ ，使得在 $[a,+\infty)$ 上有 $\displaystyle0\leqslant \frac{C}{x^p}\leqslant f(x)$ 则广义积分 $\displaystyle\int_a^{+\infty}f(x)\mathrm{d}x$ 发散.

实质上，这就是阶的判别法，也就是利用 $p$-积分的敛散性进行比较判别。

#### 级数判别法
对于级数而言，我们曾使用积分判别法来判断[[数项级数]]是否发散，积分判别法可以等价为如下的内容：

>[!note] 定理：级数收敛性的积分判别法（广义积分陈述）
>设函数 $f(x)$ 在区间 $[1,+\infty)$ 上**非负且递减**，则级数 $\displaystyle\sum\limits_{n=1}^\infty f(n)$ 与广义积分 $\displaystyle\int_1^{+\infty}f(x)\mathrm{d}x$ 同时收敛或同时发散。

当然，现在从广义积分的视角来看，我们似乎也能利用这样的性质倒推为级数进行敛散性判别。

>[!note] 定理：级数判别法
>设函数 $f(x)$ 在 $[a,+\infty)$ 上**非负**且对任何 $A>a,f(x)$ 都在 $[a,A]$ 上**可积**，又设有**严格递增**数列 $\{A_n\}:A_0=a,A_n\to+\infty(n\to\infty)$. 令
> $$ u_n=\int_{A_{n-1}}^{A_n}f(x)\mathrm{d}x,n=1,2\cdots $$  
>则正项级数 $\displaystyle\sum\limits_{n=1}^\infty u_n$ 与广义积分 $\displaystyle\int_{a}^{+\infty}f(x)\mathrm{d}x$ 同时收敛或同时发散。

需要注意的是，尽管我们利用这个判别法将级数和广义积分建立了联系，但是广义积分的性质还是有所不同。例如对于级数而言，如果级数 $\displaystyle\sum\limits_{n=1}^\infty a_n$ 收敛，则有必要条件 $\displaystyle\lim_{n\to \infty}a_n=0$ ，但是对于广义积分而言，如果
$$
\int_{a}^{+\infty}f(x)\mathrm{d}x
$$
收敛，那么 $\displaystyle\lim_{x\to+\infty}f(x)=0$ 是**不一定成立**的（但是加上一致连续的条件后是成立的，见NKU习题15(A)T2、T3）。可以看下例：



>[!faq] NKU课本例8
>讨论广义积分
> $$ \int_0^{+\infty}\frac{x^p}{1+x^q\sin^2 x}\mathrm{d}x(p>0,q>0) $$的收敛性。

记 $f(x)=\displaystyle\frac{x^p}{1+x^q\sin^2{x}}$ ，当 $n\pi\leqslant x\leqslant (n+1)\pi$ 的时候有：
$$
\frac{(n\pi)^p}{1+[(n+1)\pi]^q\sin^2x}\leqslant f(x)\leqslant \frac{[(n+1)\pi]^p}{1+(n\pi)^q\sin^2 x}
$$
因为：
$$
\int_{n\pi}^{(n+1)\pi}\frac{\mathrm{d}x}{1+A\sin^2x}=\frac{\pi}{\sqrt{1+A}}
$$
所以利用上述不等式，有：
$$
\frac{n^p\pi^{p+1}}{\sqrt{1+(n+1)^q\pi^q}}\leqslant\int_{n\pi}^{(n+1)\pi}f(x)\mathrm{d}x\leqslant\frac{(n+1)^p\pi^{p+1}}{\sqrt{1+n^q\pi^q}}
$$

上式说明 $\displaystyle\int_{n\pi}^{(n+1)\pi}f(x)\mathrm{d}x$ 为 $\displaystyle\frac{1}{n^{\frac{q}{2}-p}}$ 的同阶无穷小，从而令 $A_n=n \pi$ 由于级数判别法可知在 $q>2p+2$ 的时候收敛，在 $q\leqslant 2p+2$ 的时候发散. $\rule{3pt}{10pt}$

>[!note] Remark.
>对于级数判别法，上面启发我们有如下的基本流程：
>
>- 找到合适的单调递增数列；
>- 如果相应的积分对应的级数已经好判断敛散性，直接判断完毕；
>- 如果不是，利用夹逼的方式简化积分结构，同时求出无穷小的阶。

同样，反过头来，对于判断级数的敛散性，利用广义积分也是一个比较合适的选择。


#### Abel判别法
>[!note] 定理：Abel判别法
>若广义积分 $\displaystyle\int_a^{+\infty}f(x)\mathrm{d}x$ **收敛**，函数 $g(x)$ 在 $[a,+\infty)$ 上**单调有界**，则广义积分 $\displaystyle\int_a^{+\infty}f(x)g(x)\mathrm{d}x$ 收敛。



#### Dirichlet判别法
>[!note] 定理：Dirichlet判别法
>若 $F(A)=]\displaystyle\int_a^A f(x)\mathrm{d}x$ 在 $[a,+\infty)$ 上有界，函数 $g(x)$ 在 $[a,+\infty)$ 上单调且 $\displaystyle\lim_{x\to+\infty}g(x)=0$，则广义积分
>$$\int_a^{+\infty}f(x)g(x)\mathrm{d}x$$收敛。



## 有限区间上无界函数的广义积分
### 奇点
引入奇点的概念来研究无界函数：
>[!note] 定义：奇点
>如果对于点 $x_0\in[a,b]$ 的任何空心邻域 $B_{\delta}^{\circ}(x_0)$ ， $f(x)$ 都在 $B_{\delta}^{\circ}(x_0)\cap [a,b]$ 中无界，则称点 $x_0$ 为 $f(x)$ 的一个**奇点**（或**瑕点**）。


奇点可以简单理解为无界的点，在这样的点周围的 Riemann 积分需要扩展为广义积分进行计算。

也可利用可积性判断奇点：
>[!note] 定理：可积性判断奇点
>设对任意 $\delta\in (0,b-a)$ ，函数 $f(x)$ 都在 $[a,b-\delta]$ 上可积，但 $f(x)$ 在 $[a,b]$ 上不可积，则 $b$ 是 $f(x)$ 的一个奇点。

这个定理的证明方法是利用 Riemann 和进行拆解，在 $[a,b-\delta]$ 上 Riemann 和小于 $\varepsilon$ ，而在 $[b-\delta,b]$ 上假如不为奇点，则有界，可以利用 Riemann 和导出可积性，从而生成矛盾。

下面来看**可去奇点**，这种奇点并不是真正的奇点，因为实际上它仅仅只是无定义，但其邻域内通常是有界的，例如对于下面的积分：
$$
\int_0^{+\infty}\frac{\sin x}{x}\mathrm{d}x
$$
可以知道 $0$ 的时候该函数无定义，但是极限显然为 $1$ ，从而可以说这是一个**可去奇点**。
### 无界函数的广义积分
#### 无界函数广义积分定义
>[!note] 定义：无界函数的广义积分
>设 $b$ 是 $f(x)$ 在 $[a,b]$ 上的唯一奇点，且对任何 $\delta\in (0,b-a)$ ，则 $f(x)$ 都在 $[a,b-\delta]$ 上可积，如果函数极限 $$ \lim_{\delta\to 0^+}\int_a^{b-\delta}f(x)\mathrm{d}x=I $$
>存在，则称 $f(x)$ 从 $a$ 到 $b$ 的**广义积分（瑕积分）收敛**，并称实数 $I$ 为此广义积分的值，记为 $$ \int_a^bf(x)\mathrm{d}x=\lim_{\delta\to 0^+}\int_a^{b-\delta}f(x)\mathrm{d}x=I $$ 否则就称广义积分 $\displaystyle\int_a^b f(x)\mathrm{d}x$ **发散**。如果极限值为 $+\infty$ 或 $-\infty$ ，称广义积分发散到 $+\infty$ 或 $-\infty$ .

如果 $c\in (a,b)$ 是区间上的唯一奇点，则定义：
$$
\int_a^bf(x)\mathrm{d}x=\int_a^cf(x)\mathrm{d}x+\int_c^b f(x)\mathrm{d}x
$$
右端两个积分都收敛时，左端的广义积分收敛，否则左端的广义积分发散。

无界函数的广义积分的性质：线性可加，区间可加，Newton-Leibniz 公式依然成立，不再进行证明。

#### 无界函数广义积分的计算
除 Newton-Leibniz 公式之外，此处我们引入广义积分的换元公式：
>[!note] 定理：广义积分换元公式
>设 $f(x)$ 在 $[a,b)$ 上连续，$b$ 是 $f(x)$ 的唯一奇点或 $b=+\infty$，$x=\varphi(t)$ 在 $[\alpha,\beta)$ 上**严格递增且连续可导** ($\beta$ 可以是 $+\infty$) ，$\varphi(\alpha)=a,\displaystyle\lim_{t\to \beta}\varphi(t)=b$，那么广义积分 $\displaystyle\int_a^bf(x)\mathrm{d}x$ 与 $\displaystyle\int_\alpha^\beta f(\varphi(t))\varphi'(t)\mathrm{d}t$ 同时收敛或同时发散，且在收敛时有： $$ \displaystyle\int_a^bf(x)\mathrm{d}x=\displaystyle\int_\alpha^\beta f(\varphi(t))\varphi'(t)\mathrm{d}t $$

当然，对于上述定理，$\varphi(t)$ 严格递减也可，但是如果不严格单调，换元公式可能会出现问题。
利用换元积分，我们可以将所有的瑕积分换为无界的广义积分，现考虑下面的瑕积分：
$$
\lim_{\varepsilon\to 0^+}\int_a^{b-\varepsilon}f(x)\mathrm{d}x
$$
其中 $b$ 为唯一奇点，那么作换元 $x=\displaystyle b-\frac{1}{y}$ 有

$$
\begin{aligned}
\lim_{\varepsilon\to 0^+}\int_a^{b-\varepsilon}f(x)\mathrm{d}x&=\lim_{\varepsilon\to 0^+}\int_{\frac{1}{b-a}}^{\frac{1}{\varepsilon}}f(b-\frac{1}{y})\frac{1}{y^2}\mathrm{d}y \\\\
&=\int^{+\infty}_{\frac{1}{b-a}}f(b-\frac{1}{y})\frac{1}{y^2}\mathrm{d}y
\end{aligned}
$$

从而瑕积分转变为了无穷区间的积分。

#### 无界函数广义积分敛散性判别
本部分的判别法可直接扩展无穷区间广义积分的敛散性判别法，以下直接进入例题：
>[!faq] 例题：Beta函数和Gamma函数的敛散性
>讨论收敛性：
>1. Beta函数： $$ \mathrm{B}(a,b)=\int_0^1 x^{a-1}(1-x)^{b-1}\mathrm{d}x $$
>2. Gamma函数： $$ \Gamma(p)=\int_0^{+\infty}x^{p-1}\mathrm{e}^{-x}\mathrm{d}x $$


先考察奇点状况，当 $a<1$ 时，$0$ 为奇点，当 $b<1$ 时，$1$ 为奇点，广义积分 $\displaystyle\int_0^1 x^{a-1}(1-x)^{b-1}\mathrm{d}x$ 收敛当且仅当 $\displaystyle\int_0^{\frac{1}{2}}$ 和 $\displaystyle\int_\frac{1}{2}^1$ 两段收敛。

而由于 $x^{a-1}(1-x)^{b-1}\sim x^{a-1}\quad(x\to 0)$ 且 $x^{a-1}(1-x)^{b-1}\sim (1-x)^{b-1}\quad (x\to 1)$ ，由阶的估计法可知必须要 $1-a<1$ 且 $1-b<1$ ，故 $a>0$ 且 $b>0$ 为Beta函数收敛的充要条件。

对于 Gamma 函数可分为两段： $\displaystyle\int_0^1$ 与 $\displaystyle\int_1^{+\infty}$ ，对于第一段，在 $p<1$ 的时候 $0$ 为奇点，考虑 $x^{p-1}\mathrm{e}^{-x}\sim x^{p-1}\quad(x\to 0)$ ，则 $p>0$ 的时候第一段收敛。对第二段， $x^{p-1}\mathrm{e}^{-x}=o(x^{-2})$ ，因此第二段必收敛，从而有 $p>0$ 时收敛，$p\leqslant 0$ 时发散. $\rule{3pt}{10pt}$



