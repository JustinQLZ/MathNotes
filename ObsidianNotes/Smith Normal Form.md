#Commutative-Algebra 
Let $A$ be a PID, recall that every submodule of a free $A$ module is free, so we can define the rank a homomorphism of (finitely generated) $A$-modules as the rank of its image. Furthermore, with isomorphisms $M\cong A^r$ chosen, such a homomorphism corresponds to a matrix.
We consider the equivalence class of such matrixes under elementary row and column transformations. Here by elementary transformation, we mean permutations and matrixes of with left-top $2\times 2$ of corner of the form$$\begin{pmatrix}
r & -b\\
s & a
\end{pmatrix}
$$with $ra+bs=1$ and 1 down on the diagonal.
**Proposition.** If $M$ is an $n\times m$ matrix of rank $r>0$ over a PID $A$, then $M$ is equivalent to a matrix of the form $\mathrm{diag}\,(d_1,\dots,d_r,0,\dots,0)$, where $d_1\mid d_2\mid\cdots\mid d_r$. The ideals $(d_1)\dots,(d_r)$ are uniquely determined by the equivalence class of $A$. In particular, if $n=m$, then elementary transformation preserves determinant, and hence $\det A=d_1\cdots,d_r$.
**Remark.** Considering rows as relations between a set of generators of an abelian group, elementary transformation gives an algorithm too determine the standard form of the abelian group.