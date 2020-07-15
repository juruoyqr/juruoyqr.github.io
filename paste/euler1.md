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

# 欧拉函数是积性函数证明

**证明：**

令 $S(n)$ 为 $1\sim n$ 中与 $n$ 互质的数组成的集合。

分别任取 $S(a),S(b)$ 中的元素 $a_0,b_0$.（ $\gcd(a,b)=1$ ）

考虑线性同余方程组 $\left \{ 
\begin{array}{c}
				x\equiv a_0\pmod {a}\\
				x\equiv b_0\pmod {b}
\end{array}
\right.$,

则有唯一解 $x\equiv c_0\pmod {ab}$.

$\gcd(c_0,a)=\gcd(c_0\bmod a.a)=\gcd(a_0,a)=1$. 同理可得，$\gcd(c_0,b)=1$.

故 $\gcd(c_0,ab)=1,c_0\in S(ab)$.

此为 $S(a)\times S(b)$ 到 $S(ab)$ 的一个单射。

任取 $S(ab)$ 中的元素 $c_0$，令 $a_0=c_0\bmod a,b_0=c_0\bmod b$.

由于 $\gcd(ab,c_0)=1$，故 $a_0\in S(a),b_0\in S(b)$.

此为 $S(ab)$ 到 $S(a)\times S(b)$ 的一个单射。

故 $S(a)\times S(b)$ 到 $S(ab)$ 存在一个双射。

因此 $\|S(ab)\|=\|S(a)\|\|S(b)\|$，即 $\varphi(ab)=\varphi(a)\varphi(b)$。

Q.E.D.
