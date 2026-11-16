#Algebra #small-tricks #Algebraic-Topology
As the title suggests, find a subsystem $J$ of a direct system (indexed by) $I$, such that it's cofinal, i.e. $\forall i\in I\,\exists j\in J \enspace i\leq j$. Then the direct limit can be simplified:
$$
\varinjlim_I A_{\bullet} = \varinjlim_J A_{\bullet}
$$
### Examples:
1. Let $A$ be an integral domain and $K=Frac\,A$, then
$$
K=\varinjlim_{M\subset K}\,M=\varinjlim_{M\subset K \text{ and }M\text{ is }f.g.}M=\varinjlim_{\xi\in A}\,A\xi
$$
2. Let $M$ be a smooth manifold of dimension $n$, then the set of open covers of $M$ form a direct system. Say a cover is a good cover if any finite intersection is diffeomorphic to $\mathbb{R}^n$. Then the good covers of $M$ are cofinal, so for any direct system indexed by open covers of $M$, in particular, the system used to define the Čech cohomology, we only need to take the direct limit on good covers.
3. The idea can be used to prove that the pullback functor of sheaves $f^{-1}$ preserves stalks, and therefore $f^{-1}$ is an exact functor. Let $f:X\rightarrow Y$ be a continuous map and $\mathcal{F}$ a sheaf over $Y$, fix $y=f(x)$. Consider $\mathcal{F}_y=\underset{y\in V}{\text{colim}}\,\mathcal{F}(V)$ and $(f^{-1}\mathcal{F})_x=\underset{x\in U}{\text{colim}}\,\underset{f(U)\subset V}{\text{colim}}\,\mathcal{F}(V)$. Since $f$ is continuous, the first index set is cofinal in the second.