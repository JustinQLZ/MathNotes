#Algebraic-Geometry #Number-Theory
In the view of classical algebraic geometry, a $K$-rational point of an algebraic subset of $\bar{K}^n$ is a point such that all coordinates lie in $K$.

In the language of schemes, assuming that the structure field $k$ is specified, for a $k$-scheme $X$ and a field extension $K/k$, a $K$-point on $X$ is a $k$-morphism $\mathrm{Spec}\,K\rightarrow X$. In general, for another $k$-scheme $S$, an $S$-point is a $k$-morphism $S\rightarrow X$ and all such morphisms form a set $X(S)$. Notice that a $K$-point is not necessarily a closed point. (See item 3 of [[(Counter)examples in Algebraic Geometry]].) So a $K$-point contains a point $x\in X$ and a field extension $K/k(x)/k$. Base-changing to $K$, a $K$-point with image $x\in X$ is in one-to-one correspondence with a $K$-point (necessarily closed) $x_K\in X_K$ which lie in the fiber over $x$, representing one $k$-embedding of $k(x)$ in $K$. $K$-points on $X_K$ are closed points with residue field $k(x)=K$.

To unify these two views, consider $\mathbb{A}^n_\bar{K}\rightarrow\mathbb{A}^n_K$. Fix a classical point $x=(x_1-a_1,\dots,x_n-a_n)$. If it is a $K$-rational point, then its image in $\mathbb{A}_K^n$ is the maximal ideal $(x_1-a_1,\dots,x_n-a_n$) and is a $K$-point on $\mathbb{A}^n_K$. On the other hand, consider the base change
```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
\begin{tikzcd} {\mathrm{Spec}\,\bar{K}} & {\mathrm{Spec}\,K} \\ {\mathbb{A}_{\bar{K}}^n} & {\mathbb{A}_K^n} \\ {\mathrm{Spec}\,\bar{K}} & {\mathrm{Spec}\,K} \arrow[from=1-1, to=1-2] \arrow[from=1-1, to=2-1] \arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=1-1, to=2-2] \arrow[from=1-2, to=2-2] \arrow[from=2-1, to=2-2] \arrow[from=2-1, to=3-1] \arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=2-1, to=3-2] \arrow[from=2-2, to=3-2] \arrow[from=3-1, to=3-2] \end{tikzcd}
\end{document}
```
We see that the fiber over a $K$-point of $\mathbb{A}^n$ is a $\bar{K}$-point of $\mathbb{A}_\bar{K}^n$, i.e. a classical point $x=(x_1-a_1,\dots,x_n-a_n)$. Also, $a_i$ must lie in $K$. (Let $b_i=\pi(x_i)$, where $\pi:K[x_1,\dots,x_n]\rightarrow K[x_1,\dots,x_n]/\mathfrak{m}_{x}\cong K$. Then $(x_1-b_1,\dots,x_n-b_n)\subset(x_1-a_1,\dots,x_n-b_n)$. So $a_i=b_i\in K$.) So we have shown that $K$-rational points on $\mathbb{A}_{\bar{K}}^n$ and $K$-points on $\mathbb{A}_K^n$ are in one-to-one correspondence. However, do notice that a closed point on $\mathbb{A}_K^n$ may not be a $K$-point since $K$ is not algebraically closed in general and its residue field maybe larger than $K$.

Also, using the fiber product, we see that for any $k$-scheme $X$ and any $L/K/k$, $X(K)$ is in one-to-one correspondence with $K$-points of $X_L\rightarrow\mathrm{Spec}\,L\rightarrow\mathrm{Spec}\,K$. We see that $K$-point splits while the base extends. In other words, different embeddings become points.