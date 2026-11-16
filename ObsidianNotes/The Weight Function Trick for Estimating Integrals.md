#Analysis #Harmonic-Analysis  
#### Extracting Factors
Let $g\in L^1(\mathbb{R}^n)$, our goal is to estimate $||g||_1$ by some supreme relating $g$. To do so, we introduce a weight function $w$, such that
1. $w\cdot g\in L^1(\mathbb{R}^n)$ (This is often guaranteed by $w\in L^{\infty}(\mathbb{R}^n)$.)
2. $w>0$ and $w^{-1}\in L^1(\mathbb{R}^n)$
Then we can write$$
\begin{align}
||g||_1&=\int_{\mathbb{R}^n}\frac{wg}{w}\,dx\\
&\leq||wg||_{\infty}\int_{\mathbb{R}^n}\frac{dx}{w}=C||wg||_{\infty}
\end{align}
$$$w=(1+|x|^2)^k$ with $2k>n$ is a common choice. Here's an example:
**Proposition.** The Fourier transformation on Schwartz functions is a continuous linear map from $\mathcal{S}(\mathbb{R}^n)$ to itself.
**Proof.** Recall the semi-norms of $\mathcal{S}(\mathbb{R}^n)$ are$$
p_{\alpha,\beta}(f):=\sup_{x\in\mathbb{R}^n}|x^{\alpha}D^{\beta}f(x)|.
$$And these induce a sequence of norms$$
||f||_{(k)}:=\sup_{|\alpha|+|\beta|\leq k}p_{\alpha,\beta}(f).
$$Clearly for any $f\in\mathcal{S}(\mathbb{R}^n)$, $\hat{f}$ is smooth. Next we estimate $p_{\alpha,\beta}(\hat{f})$. Denote all constants by $C$.$$
\begin{align}
p_{\alpha,\beta}(\hat{f})&\leq C||D^{\alpha}(x^{\beta}f)||_1\\
&\leq C||(1+|x|^2)^{n+1}D^{\alpha}(x^{\beta}f)||_{\infty}\\
&\leq C||f||_{(2n+2+|\alpha|+|\beta|)}
\end{align}
$$Hence $\hat{f}\in\mathcal{S}(\mathbb{R}^n$). Furthermore, suppose $f_k\to f\text{ in }\mathcal{S}(\mathbb{R}^n)$, then $p_{\alpha,\beta}(\hat{f}_k-\hat{f})\to 0$. So $f\mapsto\hat{f}$ is continuous.$$\tag*{$\square$}$$This can be generalized to $g\in L^p(\mathbb{R}^n)$, where $p\in [1,\infty)$.$$
\begin{align}
||g||_p^p&=\int_{\mathbb{R}^n}|\frac{w\cdot g}{w}|^p\,dx\\
&\leq||w\cdot g||_{\infty}^p\int_{\mathbb{R}^n}\frac{dx}{w^p}
\end{align}
$$so $||g||_p\leq C||w\cdot g||_{\infty}$.

#### Combine With Cauchy-Schwartz
(More generally, Holder.)
In the first section we actually used Holder for (1,$\infty$), but in general we could use any pair. In particular, it's very often to consider (1/2,1/2). Moreover, we have Plancherel for inequity $L^2$.
e.g. $\mathcal{D}_N:=\{\varphi\in C^{\infty}(R^n):\mathrm{supp}\,\varphi\subset B,||D^{\alpha}\varphi||_{\infty}\leq1,0\leq|\alpha|\leq N\}$, where $B$ is the unit ball and $N>n/2$. Then $\sup_{\varphi\in \mathcal{D}_N}||\hat{\varphi}||_1<\infty$.
In the first place, it came to me that we have a pointwise estimation$$|x^{\alpha}\widehat{\varphi}|=|\widehat{D^{\alpha}\varphi}|\leq\int_B|D^{\alpha}\varphi|\leq|B|.$$But we only have $N>n/2$, so this is not good enough. (In contrast, $L^2$ with Plancherel inequity could give us a overall estimation.)
This suggests that we need to introduce a square. (Here's also a small trick, instead of considering $|x|^a$, it's more convenient to consider $(1+|x|^2)^{a/2}$ so we don't need to write explicitly the integral into two parts.)$$||\widehat{\varphi}||_1\leq||(1+|\xi|^2)^{-N/2}||_2||(1+|\xi|^2)^{N/2}\widehat{\varphi}||_2$$The first term converges since $N>n/2$. The square of the second term is$$\int_{\mathbb{R}^n}(1+|\xi|^2)^N\widehat{\varphi}^2(\xi)\,d\xi\leq C\sum_{|\alpha|=0}^N\int_{\mathbb{R}^n}|\xi^{\alpha}|^2\widehat{\varphi}^2(\xi)\,d\xi$$
**Remark.** Gemini says that this is a special case of a Sobolev embedding theorem.