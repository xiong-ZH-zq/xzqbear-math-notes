---
comments: true
---
# 幂级数
## 幂级数的性质与求和

### 幂级数的定义与收敛半径

>[!note] 定义：幂级数
>形如
> $$  \displaystyle\sum\limits_{n=0}^\infty a_n(x-x_0)^n = a_0+a_1(x-x_0)+\cdots+a_n(x-x_0)^n+\cdots $$  
>的函数项级数称为幂级数，其中 $a_0,a_1,\cdots$ 都是常数，称为该幂级数的系数，$x_0$ 为一个固定点.

需要注意的是，默认 $(x-x_0)^0=1$ ，也就是说我们并不会考虑 $0^0$ 的问题.

幂级数的收敛域比较简单，它总是一个以 $x_0$ 为中心的区间，需要探讨的只是半径，设
 $$  
\rho =\varlimsup_{n\to \infty}\sqrt[n]{|a_n|}
 $$  
那么有收敛半径
 $$  
R = 
\begin{cases}+\infty,&\rho=0\\\\ \displaystyle\frac{1}{\rho},& 0<\rho<+\infty, \\\\ 0, & \rho=+\infty.\end{cases}
 $$  
对于收敛域内外的敛散性，有如下定理：
>[!note] 定理：Cauchy-Hadamard定理
>幂级数 $\displaystyle\sum\limits_{n=0}^\infty a_n(x-x_0)^n$ 在 $|x-x_0|<R$ 时**绝对收敛**，在 $|x-x_0|>R$ 时**发散**.

利用 Cauchy 根值判别法即可。

幂级数的收敛域是单点集 $\{x_0\}$ 或者一个区间，因此幂级数的收敛域也称为幂级数的收敛区间。在端点处我们目前不能确定是否收敛。

利用达朗贝尔判别法可以导出如下收敛半径的计算公式：

$$  
\lim_{n\to \infty}\left|\frac{a_n}{a_{n+1}}\right|
$$

如果上述极限存在或发散到 $+\infty$ ，则它就是幂级数的收敛半径。


>[!faq] 例题1
>求幂级数
> $$  \displaystyle\sum\limits_{n=0}^\infty\frac{(2n)!}{(n!)^2}x^n $$  
>的收敛区间.

记 $a_n = \displaystyle\frac{(2n)!}{(n!)^2}$ ，那么利用达朗贝尔判别法求收敛半径有

$$  
R = \lim_{n\to \infty} \frac{a_n}{a_{n+1}}=\frac{1}{4}
$$  

考虑端点，当 $x=\displaystyle-\frac{1}{4}$ 时，有

$$  
\displaystyle\sum\limits_{n=0}^\infty a_n \left(-\frac{1}{4}\right)^n
$$

为交错级数，且 $\displaystyle\frac{a_n}{4^n}$ 单调减，再证其趋于 $0$ ：由比较判别法可知 $\displaystyle\sum\limits_{n=1}^\infty \ln \left(1-\frac{1}{2n}\right)=-\infty$ ，从而有

$$  
\lim_{n\to \infty} \frac{a_n}{4^n} = \prod_{n=1}^\infty \left(1-\frac{1}{2n}\right) = 0.
$$

进而由 Leibniz 判别法可知该级数收敛.

对于 $x=\displaystyle\frac{1}{4}$ ，由 Wallis 公式可知

$$  
\frac{a_n}{4^n} = \frac{(2n-1)!!}{(2n)!!}\sim \displaystyle\frac{1}{\sqrt{\displaystyle\left(n+\frac{1}{2}\right)\pi}}
$$

从而级数发散. $\rule{3pt}{10pt}$




### Abel定理
>[!note] 定理：Abel定理
>幂级数 $\displaystyle\sum\limits_{n=0}^\infty a_n(x-x_0)^n$ 在其收敛区间上内闭一致收敛.

证明：仅需讨论 $a<x_0<b$ ，分别证明幂级数在 $[a,x_0]$ 和 $[x_0,b]$ 上一致收敛，当 $x\in [x_0,b]$ 时，注意到
 $$  
\displaystyle\sum\limits_{n=0}^\infty a_n(x-x_0)^n = \displaystyle\sum\limits_{n=0}^\infty a_n(b-x_0)^n \left(\frac{x-x_0}{b-x_0}\right)^n
 $$  
其中 $\displaystyle\sum\limits_{n=0}^\infty a_n (b-x_0)$ 为收敛的数项级数，因而是一致收敛的，而由 $\displaystyle0\leq \frac{x-x_0}{b-x_0}\leq 1$ 可知，函数列 $\left\{\left(\displaystyle\frac{x-x_0}{b-x_0}\right)^n\right\}$ 在 $[x_0,b]$ 上一致有界，并且对每个 $x\in[x_0,b]$ 是单调递减的，根据一致收敛的Abel判别法可知，$\displaystyle\sum\limits_{n=0}^\infty a_n(x-x_0)^n$ 在 $[x_0,b]$ 上一致收敛.

同理可证 $[a,x_0]$ 上也一致收敛，因此在 $[a,b]$ 上一致收敛. $\rule{3pt}{10pt}$

从这个部分我们可以看出幂级数的一个非常重要的性质：我们一定能保证幂级数的**内闭一致收敛**的性质，但是对于端点处，由于我们在判断收敛区间的时候就需要单独判断，所以不能保证整个区间上的一致收敛性。



由 Abel 定理可以导出如下性质：
>[!note] 性质1
>设幂级数 $\displaystyle\sum\limits_{n=1}^\infty a_n(x-x_0)^n$ 的收敛区间为 $I$ ，则它的和函数 $S(x)$ 在 $I$ 上连续.

>[!note] 性质2
>设幂级数 $\displaystyle\sum\limits_{n=0}^\infty a_n(x-x_0)^n$ 的收敛区间为 $I$ ，则它的和函数 $S(x)$ 在 $I$ 的任何闭子区间 $[a,b]$ 上都可积，并且可以逐项求积分，即
> $$  \int_a^b S(x)\mathrm{d}x=\displaystyle\sum\limits_{n=0}^\infty \int_a^b a_n(x-x_0)^n \mathrm{d}x. $$  

>[!note] 性质3
>设幂级数 $\displaystyle\sum\limits_{n=0}^\infty a_n(x-x_0)^n$ 的收敛半径 $R>0$ ，收敛区间为 $I$ ，和函数为 $S(x)$. 又设它逐项求导所得的幂级数 $\displaystyle\sum\limits_{n=1}^\infty na_n(x-x_0)^{n-1}$ 的收敛区间为 $I'$，则
>1. $I\supseteq I' \supseteq (x_0-R,x_0+R)$；
>2. 和函数 $S(x)$ 在 $I'$ 上连续可导，且可以逐项求导，即当 $x\in I'$ 时， $$  S'(x)=\displaystyle\sum\limits_{n=1}^\infty n a_n(x-x_0)^{n-1}. $$  

利用上述的性质可以解决很多级数求和的问题。

>[!faq] 例题
>求下列幂级数的和函数：
>1. $\displaystyle\sum\limits_{n=1}^\infty \frac{(-1)^{n-1}}{n}x^n$；
>2. $\displaystyle\sum\limits_{n=0}^\infty \frac{(-1)^n}{2n+1}x^{2n+1}$.

(1) 记和函数为 $S_1(x)$ ，收敛半径显然为 $1$ ，对于任意的 $x\in (-1,1)$ 有
 $$  
S_1'(x)=\displaystyle\sum\limits_{n=1}^\infty(-1)^{n-1}x^{n-1}=\frac{1}{1+x}
 $$  
从而
 $$  
S_1(x) = S_1(0)+\int_0^x\frac{\mathrm{d} t}{1+t}=\ln (1+x), \ \forall x\in(-1,1)
 $$  
考虑到收敛区间为 $(-1,1]$ ，由性质 $1$ 可知 $S_1(x)$ 在 $(-1,1]$ 上连续，而 $\ln (1+x)$ 也在 $(-1,1]$ 上连续，所以和函数为 $\ln(1+x)$ .

(2) 与上题类似，答案为 $\arctan x$ . $\rule{3pt}{10pt}$

从本题可以得到
 $$  
\begin{aligned}
&1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\cdots=\ln 2,\\\\
&1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\cdots=\frac{\pi}{4}.
\end{aligned}
 $$  

## Taylor级数
### Taylor级数的定义
将函数表示为幂级数是我们在学习幂级数后自然想要实现的目标，设函数 $f(x)$ 在点 $x_0$ 的一个邻域 $(x_0-\delta,x_0+\delta)$ 内可以表示成幂级数，即当 $x\in (x_0-\delta,x_0+\delta)$ 时，有

$$  
f(x)=\displaystyle\sum\limits_{n=0}^\infty a_n(x-x_0)^n . 
$$  

根据幂级数的性质可知 $f(x)$ 无限次可导，并且对于系数，有如下计算方法：

$$  
a_k =\frac{f^{(k)}(x_0)}{k!}, \ k=1,2,\cdots
$$  

从而有
 $$  
f(x) = \displaystyle\sum\limits_{n=0}^\infty\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n. \tag{1}
 $$  
以上就是 **Taylor 级数**。

以上的级数是否一定收敛到 $f(x)$ ？实际上是不一定的，也就是说 $f(x)$ 能被表示成幂级数是需要条件的，可以参看下面的反例：
>[!faq] 反例：幂级数不总能收敛到 $f(x)$
>考察函数
> $$  f(x)=\begin{cases}\mathrm{e}^{-\frac{1}{x^2}}, &x\neq 0 \\\\ 0, &x=0.\end{cases} $$  
>容易验证，$f(x)$ 在 $(-\infty,+\infty)$ 上任意多次可导，且
> $$  f^{(n)}(0)=0, n=0,1,2,\cdots. $$  
>因此对任何的 $x\neq 0$，
> $$  f(x)\neq \displaystyle\sum\limits_{n=0}^\infty \frac{f^{(n)}(0)}{n!}x^n=0. $$


----

之后，不管收敛半径是否为 $0$ ，也不管是否收敛到 $f(x)$ ，都记
 $$  
f(x)\sim \displaystyle\sum\limits_{n=0}^\infty \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n.
 $$  
我们都称上述的级数为 $x_0$ 处的 **Taylor 级数**，当 $x_0=0$ 时，也称为 **Maclaurin 级数** 。

如果存在 $\delta>0$ 使得 $x\in O_\delta(x_0)$ 都有 $(1)$ 成立，即 $f(x)$ 与 Taylor 级数相等，那么就称 $f(x)$ 在 $(x_0-\delta,x_0+\delta)$ 可展开为 Taylor 级数。

>[!example] 总结：目前已学的余项
>- Peano余项：$R_n(x-x_0)$.
>- Lagrange余项：$\displaystyle\frac{f^{(n+1)}(x_0+\theta(x-x_0))}{(n+1)!}(x-x_0)^{n+1}$ 其中 $(0<\theta<1)$.
>- Cauchy余项：$\displaystyle\frac{f^{(n+1)}(x_0+\nu(x-x_0))}{(n+1)!}(1-\nu)^n(x-x_0)^{n+1}$ 其中 $0<\nu<1$.


### 常见函数的Taylor级数
这里的级数实际上基本都在学习 Taylor 展开的时候接触过了，这里只记录广义二项式定理：
>[!faq] 定理：广义二项式定理
>对二项式函数
> $$  f(x)=(1+x)^\alpha $$  
>进行泰勒展开.

计算并不难，求 $n$ 阶导后有：
 $$  
f^{(n)}(x) = \alpha(\alpha-1)\cdots (\alpha-n+1)(1+x)^{\alpha-n}
 $$  
现在考虑证明 Taylor 级数的存在性，也就是 $R_n(x)$ 趋于 $0$ .

利用 Cauchy 余项：
 $$  
 \begin{aligned}
&R_n(x)=\frac{\alpha(\alpha-1)\cdots (\alpha-n+1)(1+\nu)^{\alpha-n-1}}{n!}(1-\nu)^n x^{n+1} \\\\
&=  \boxed{\frac{\alpha(\alpha-1)\cdots (\alpha-n+1)}{n!} x^{n+1}}\boxed{(1+\nu)^{\alpha-1}}\boxed{\left(\frac{1-\nu}{1+\nu x}\right)^n}
\end{aligned}
 $$  

其中 $0<\nu<1$ ，为证明 $\displaystyle\lim_{n\to \infty} R_n(x)=0$ ，考虑三个因式分别讨论.

对于第一个部分，考虑极限 $\displaystyle\lim_{n\to \infty}\left|\frac{\alpha-n}{n}x\right|=|x|$ ，因此，当 $|x|<1$ 的时候，有
 $$  
\lim_{n\to \infty}\left|\frac{\alpha(\alpha-1)\cdots (\alpha-n+1)}{n!} x^{n+1}\right|  = |\alpha x|\prod_{n=1}^\infty \left|\frac{\alpha-n}{n}x\right|=0
 $$  

对于第二个部分，由于 $0<\nu<1$ ，所以当 $|x|<1$ 的时候成立
 $$  
0<|1-x|\leq |1+ \nu x|\leq 1+|x|.
 $$  

于是有
 $$  
|1+\nu x|^{\alpha-1}\leq \max\{(1-|x|)^{\alpha-1},(1+|x|)^{\alpha-1}\}
 $$  
从而可知关于 $n$ 有界.

最后由于 $0<1-\nu<1+ \nu x$ ，从而
 $$  
\left\\{\left(\frac{1- \nu}{1+ \nu x}\right)^n\right\\}
 $$  
为有界数列，从而综上，在 $n\to \infty$ 时必然有余项趋于 $0$ ，从而有 Taylor 级数：
 $$  
(1+x)^\alpha = \displaystyle\sum\limits_{n=0}^\infty \frac{\alpha(\alpha-1)\cdots (\alpha-n+1)}{n!} x^{n},\ |x|<1
 $$  
$\rule{3pt}{10pt}$

-----
下面再来考虑端点情形的敛散性，这也是教材留作习题的部分。也就是考虑如下级数的敛散性：
 $$  
\displaystyle\sum\limits_{n=0}^\infty\frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!} 
 $$  
以及
 $$  
\displaystyle\sum\limits_{n=0}^\infty\frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!} (-1)^n
 $$  
的敛散性. 其中 $\alpha$ 不为自然数.

现在我们形式上记
 $$  
\frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!}  = \binom{\alpha}{n}
 $$  
(1) 当 $\alpha\leq -1$ 时，此时对于一般项的绝对值：
 $$  
\left|\binom{\alpha}{n}\right|\geq \frac{1\cdot 2\cdot3\cdots n}{n!}=1
 $$  
从而级数 $\displaystyle\sum\limits_{n=0}^\infty\binom{\alpha}{n}$ 和 $\displaystyle\sum\limits_{n=0}^\infty\binom{\alpha}{n}(-1)^n$ 发散. 

(2) 当 $-1<\alpha<0$ . 若 $x=1$ 则原级数为**交错级数**，此时考虑通项本身，由于
 $$  
\left|\binom{\alpha}{n}\right| = \prod_{k=1}^n\left(1-\frac{1+\alpha}{k}\right)\to 0 \quad (n\to \infty)
 $$  
可知收敛.

若 $x=-1$ ，则原级数为正项级数，此时
 $$  
\left|\binom{\alpha}{n}\right| = |\alpha|\cdot \frac{1- \alpha}{1}\cdot \cdots\cdot\frac{n-1-\alpha}{n-1}\cdot\frac{1}{n}>\frac{|\alpha|}{n}
 $$  
从而可知发散.

(3) 当 $\alpha>0$ ，对一般项取绝对值，利用 **Raabe 判别法**，有
 $$  
\lim_{n\to \infty}n\left(\frac{|u_n|}{|u_{n+1}|}-1\right)=\lim_{n\to \infty} \frac{n(1+\alpha)}{n-\alpha} = 1+\alpha>1
 $$  
从而绝对收敛，因此收敛区间为 $[-1,1]$ .

>[!note] Remark.
>归纳可得结果为：$(1+x)^\alpha$ 的收敛区间为
> $$  \begin{cases}(-1,1), &\alpha\leq -1, \\\\ (-1,1], &-1<\alpha<0,\\\\ [-1,1], &\alpha>0.\end{cases} $$  


