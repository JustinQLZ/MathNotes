#Algebraic-Geometry 
###### 1. About the Exponential Exact Sequence of Holomorphic Functions
Let $X=\mathbb{C}$ with the usual topology, $\mathcal{O}_X$ the sheaf of holomorphic functions, and let $\mathcal{F}$ be the presheaf of holomorphic functions admitting a logarithm.
```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\usepackage{amsmath}
\begin{document}
\begin{tikzcd}

	0\ar[r]&\underline{\mathbb{Z}}\ar[r,"\times2\pi i",]&\mathcal{O}_X\ar[r,"\exp"]&\mathcal{F}\ar[r]&0

\end{tikzcd}
\end{document}
```
This is an exact sequence of presheaves. (Notice that a sequence of presheaves is exact iff it's sequence of sections on every open set is exact.) $\mathcal{F}$ is clearly not a sheaf, due to failure of the gluability axiom.
Also, here's another exact sequence of sheaves of  abelian groups:
```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\usepackage{amsmath}
\begin{document}
\begin{tikzcd}

	0\ar[r]&\underline{\mathbb{Z}}\ar[r,"\times2\pi i",]&\mathcal{O}_X\ar[r,"\exp"]&\mathcal{O}_X^*\ar[r]&1

\end{tikzcd}
\end{document}
```
$\mathcal{O}_X^*$ is the sheaf of invertible holomorphic functions and is precisely the sheafification of $\mathcal{F}$.
###### 2. A surjective morphism may NOT be surjective on every open set.
Notice that this failure comes from the topological obstruction of the space. Imagine a sequence of compatible germs along a closed path around a hole such that the initial and the final elements fail to be compatible.
Consider the second sequence of item 1 on $U=X-{0}$ and $g(z)=z$, then $g\in\Gamma(U,\mathcal{O}_X^*)$. However, we know that $g$ doesn't admit a global logarithm. Suppose $\exists f\in\Gamma(U,\mathcal{O}_X)$ such that $g=\exp f$, then $g'(z)=f'(z)z=1$, so $f'(z)=1/z$. However,  $$
\oint_{|z|=1}\frac{dz}{z}=2\pi i\neq0
$$so $1/z$ doesn't admit an original function on $U$.
###### 3. A closed point may NOT be mapped to a closed point.
For example, the morphism induced by $k[t]\subset k(t)$ maps the unique point of $\mathrm{Spec}\,k(t)$ to the generic point of $k[t]$. However, a closed point IS mapped to a closed point when the morphism is proper, because a proper morphism is (universally) closed by definition. In algebraic language, this corresponds to the problem that when is the contraction of a maximal ideal $\mathfrak{m}$ along $f:A\rightarrow B$ is maximal. More generally, $f^*$ being closed is related to the going-up property (equivalent when $B$ is Noetherian and only $\Rightarrow$ if not.)