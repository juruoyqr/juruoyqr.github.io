<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

# 欧拉定理证明

**一些定义：**

**剩余类**：集合 $\{x\mid x\equiv a\pmod m\}$ 称为模 $m$ 的一个剩余类，记为 $ \overline{a}$.	

**完全剩余系**：模 $m$ 的剩余类共有 $m$ 个，为 $\overline{0},\overline{1},\cdots,\overline{m-1}$. 从这 $m$ 个集合中各任取一个数，构成一个大小为 $m$ 的集合，称为模 $m$ 的一个完全剩余系。

**简化剩余系**：模 $m$ 的完全剩余系中所有与 $m$ 互质的数组成的集合称为模 $m$ 的简化剩余系。由于每个剩余类中若有一个数与 $m$ 互质，则这个剩余类中所有数都与 $m$ 互质，且共有 $\varphi(m)$ 个剩余类满足这个性质。故模 $m$ 的简化剩余系有 $\varphi(m)$ 个元素。

下证若 $\gcd(a,m)=1$，且 $A=\{r_1,r_2,\cdots,r_{\varphi(m)}\}$ 是模 $m$ 的一个简化剩余系，则 $B=\{ar_1,ar_2,\cdots,ar_{\varphi(m)}\}$ 也是模 $m$ 的一个简化剩余系。

**引理 1**：$\forall r_i\in A$，$\gcd(a\cdot r_i,m)=1$.

**证明**： 由于 $\gcd(a,m)=\gcd(r_i,m)=1$，故 $\gcd(a\cdot r_i,m)=1$.

引理 1 保证了 $B$ 中的元素都与 $m$ 互质，则只需证 $B$ 中元素模 $m$ 不同余，则 $B$ 一定是模 $m$ 的简化剩余系。

**引理 2**：$\forall ar_i,ar_j(i\ne j)\in B$，$ar_i\not\equiv ar_j\pmod m$.

**证明**：假设 $\exist ar_i,ar_j(i\ne j)\in B$，$ar_i\equiv ar_j\pmod m$.

由于 $\gcd(a,m)=1$，故 $r_i\equiv r_j\pmod m$，矛盾。

故 $B$ 是模 $m$ 的一个简化剩余系，证毕。

故有 $r_1r_2\cdots r_{\varphi(m)}\equiv(ar_1)(ar_2)\cdots(ar_{\varphi(m)})\pmod m$,

即 $r_1r_2\cdots r_{\varphi(m)}\equiv a^{\varphi(m)}r_1r_2\cdots r_{\varphi(m)}\pmod m$.

由于 $\gcd(m,r_1r_2\cdots r_{\varphi(m)})=1$,

故 $a^{\varphi(m)}\equiv 1\pmod m$.

Q.E.D.
