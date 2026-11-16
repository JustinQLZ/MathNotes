#Algebraic-Geometry 
This summarizes some results from Hartshorne relating subsheaves with support and cohomolog with supports. Materials are from Hartshorne's exercises II.1.20, III.2.3, III.3.3 and III.3.4.

Basic definition follows trivially by the name and we refer to [[Basic Category Theory for Algebraic Geometry]]. Let $Z$ be the closed subset of a topological space $X$ and $U=X-Z$. Denote $i$ the closed immersion and $j$ the open one. Let $\mathcal{F}$ be an abelian sheaf on $X$.

**A**. we have a short exact sequence:$$0\longrightarrow \mathcal{H}_Z^0(\mathcal{F})\longrightarrow\mathcal{F}\longrightarrow j_*(\mathcal{F}|_U)$$Furthermore, if $\mathcal{F}$ is flasque, then it's also exact on the right.

**B**. $\Gamma_Z(X,\cdot)$ is a left exact functor and we denote its right derived functors $H_Y^i(X,\cdot)$. Suppose we are given an exact sequence of abelian sheaves:$$0\longrightarrow \mathcal{F}'\longrightarrow\mathcal{F}\longrightarrow \mathcal{F}''\longrightarrow0$$with $\mathcal{F}'$ flasque, then by $3\times3$ lemma the sequence$$0\longrightarrow \Gamma_Z(X,\mathcal{F}')\longrightarrow\Gamma_Z(X,\mathcal{F})\longrightarrow\Gamma_Z(X, \mathcal{F}'')\longrightarrow0.$$
**C**. If $\mathcal{F}$ is flasque then $H_Y^i(X,\mathcal{F})=0$ for all $i>0$ and the sequence$$0\longrightarrow \Gamma_Z(X,\mathcal{F})\longrightarrow\Gamma(X,\mathcal{F})\longrightarrow\Gamma(U, \mathcal{F})\longrightarrow0$$is exact.

**D**. Applying **C** to the injective resolution of $\mathcal{F}$, we get a long exact sequence$$
\begin{align}
0&\longrightarrow \Gamma_Z(X,\mathcal{F})\longrightarrow\Gamma(X,\mathcal{F})\longrightarrow\Gamma(U, \mathcal{F})\\
&\longrightarrow H_Z^1(X,\mathcal{F})\longrightarrow H^1(X,\mathcal{F})\longrightarrow H^1(U, \mathcal{F}|_U)\\
&\longrightarrow H_Z^2(X,\mathcal{F})\longrightarrow H^2(X,\mathcal{F})\longrightarrow H^2(U, \mathcal{F}|_U)\longrightarrow\cdots
\end{align}
$$
**E**. (Excision) Let $V$ be an open subset of $X$ containing $Z$. There're natural functorial isomorphisms, for all $i$ and $\mathcal{F}$,$$H_Z^i(X,\mathcal{F})\cong H_Z^i(V,\mathcal{F}|_V).$$
**F**. (Mayer-Vietoris Sequence) Let $Z_1, Z_2$ be two closed subsets of $X$. Then there is a long exact sequence of cohomolog with supports$$
\begin{align}
\cdots &\longrightarrow H^i_{Z_1\cap Z_2}(X,\mathcal{F})\longrightarrow H^i_{Z_1}(X,\mathcal{F})\oplus H_{Z_2}^i(X,\mathcal{F})\longrightarrow H^i_{Z_1\cup Z_2}(X,\mathcal{F})\\
&\longrightarrow H^{i+1}_{Z_1\cap Z_2}(X,\mathcal{F})\longrightarrow\cdots
\end{align}
$$
Now suppose further that $X=\mathrm{Spec}\,A$ is a noetherian affine scheme, $Z$ is a closed subscheme with ideal $\mathfrak{a}$ and $\mathcal{F}=M\,\tilde{}$ is quasi-coherent. Define $\Gamma_{\mathfrak{a}}(M)=\{m\in M\,:\,\mathfrak{a}^nm=0 \text{ for some } n>0\}$, then we have $\mathcal{H}_Z^0(\mathcal{F})=\Gamma_{\mathfrak{a}}(M)\,\tilde{}$. Then we can show that on any noetherian scheme $X$, if $\mathcal{F}$ is quasi-coherent (resp. coherent) then $\mathcal{H}_Z^0(F)$ is also quasi-coherent (resp. coherent).

**A**. $\Gamma_{\mathfrak{a}}(\cdot)$ is a left-exact functor from the category of $A$-modules to itself. And we denote its right derived functors, calculated in $\mathcal{Mod}_A$, by $H_{\mathfrak{a}}^i(\cdot)$.

**B**. For an $A$-module $M$, $H_{\mathfrak{a}}^i(M)=H_Y^i(X,M\,\tilde{}\,)$. And for any $i$, $\Gamma_{\mathfrak{a}}(H^i_{\mathfrak{a}}(M))=H_{\mathfrak{a}}^i(M)$.

**C**. By this notation, we give the cohomological interpretation of depth. Let $\mathrm{depth}_{\frak{a}}M$ be the maximum length of an $M$-regular sequence $x_1,\dots,x_r$, with all $x_i\in\mathfrak{a}$.
Assume that $A$ is noetherian. If $\mathrm{depth}_{\mathfrak{a}}M\geq1$, then $\Gamma_{\mathfrak{a}}(M)=0$, and the converse is true if $M$ is finitely generated. The key of the converse is that when $M$ is finitely generated, both conditions are equivalent to saying that $\mathfrak{a}$ is not contained in any associated prime of $M$.
By induction, for $M$ finitely generated, for an $n\geq 0$, the following conditions are equivalent:
1. $\mathrm{depth}_{\mathfrak{a}}M\geq n;$
2. $H_{\mathfrak{a}}^i(M)=0$ for all $i<n$.

