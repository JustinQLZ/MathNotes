#Algebraic-Geometry #Commutative-Algebra 
In short words: Hartshorne doesn't define what is a injective/surjective morphism of schemes! Not even the composition of schemes. But Hartshorne uses these terms occasionally, see Example II.3.3.1 for example. This passage is intended to sort out different possible meanings.

Their are two reasonable meanings:
1. Categorical definitions (Caution: Which category? $\mathfrak{Sch}$, $\mathfrak{Sch}(k)$ or others? For injectivity, this is irrelevant, but the problem occurs for surjectivity. The reason is purely categorical. Namely, the forgetful functor preserves and reflects injectiviy.) But more strictly speaking, these should be called monomorphisms and epimorphisms.
2. Referring to the underlying continuous map between spaces

Being a monomorphism relates to the diagonal morphism! Powerful $\Delta$! See also [[About the Diagonal in M Square]] although irrelevant.
**Lemma.** A morphism $f:X\rightarrow Y$ of schemes is a monomorphism if and only if the diagonal morphism $\Delta:X\rightarrow X\times_Y X$ is an isomorphism of schemes.
**Proof.** This is purely categorical.
($\Rightarrow$) 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

    X\times_Y X
    \arrow[drr, bend left, "p_2"]
    \arrow[ddr, bend right, "p_1"]
    \arrow[dr, dotted, "?" description] & & \\
    & X \times_Y X \arrow[r, "p_1"] \arrow[d, "p_2"]
    & X \arrow[d, "f"] \\
    & X \arrow[r, "f"]
    & Y

\end{tikzcd}
\end{document}
```
$p_1\circ\Delta=1_X$. Since $f$ is injective, we obtain $p_1=p_2$ from the commutativity of the square and hence there exists a unique morphism such that the whole diagram is commutative. Notice that both $\Delta\circ p_i$ and $1_{X\times_Y X}$ are suitable candidates for this morphism. So $\Delta\circ p_1=1_X$ and $\Delta$ is an isomorphism.
($\Leftarrow$)
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

    Z
    \arrow[drr, bend left, "g_1"]
    \arrow[ddr, bend right, "g_2"]
    \arrow[dr, dotted, "g" description] & & \\
    & X \times_Y X \arrow[r, "p_1"] \arrow[d, "p_2"]
    & X \arrow[d, "f"] \\
    & X \arrow[r, "f"]
    & Y

\end{tikzcd}
\end{document}
```
For any $g_1,g_2:Z\rightarrow X$ such that $f\circ g_1=f\circ g_2$, then there exists a unique morphism $g:Z\rightarrow X\times_Y X$ such that the diagram is commutative. Notice that we always have $p_1\circ\Delta=1_X$. Since $\Delta$ is an isomorphism, we must have $\Delta\circ p_i=1_X$. So $\Delta\circ g_i=\Delta\circ p_i\circ g=g$ and hence $g_1=g_2$.$$\tag*{$\square$}$$**Corollary.** A monomorphism of schemes is separated.
**Lemma.** The property of a morphism being a monomorphism is stable under base extensions.
**Proof.** This is purely categorical. Use the previous lemma.$$\tag*{$\square$}$$See [this Stacks Project page](https://stacks.math.columbia.edu/tag/01L1) for more on monomorphisms. See also EGA IV, 17.2.6., EGA IV, 18.12.6.

Since $\mathbf{CRing}=\mathbf{AffSch}^{op}$, we have a clear correspondence. (But do notice that epimorphism in $\mathbf{CRing}$ are weird and the epimorphisms in $\mathbf{AffSch}$ are not necessarily epimorphisms in $\mathbf{Sch}$.)
