#Algebra #Lie-Group-and-Lie-Algebra 
I SUCK AT LIE ALGEBRA BECAUSE MY LIE ALGEBRA TEACHER SUCKS!!!

TBD one day.

Let $\mathfrak{g}$ be a given complex matrix Lie algebra. We use $\mathfrak{g}=\mathfrak{so}(2n+1;\mathbb{C})$ as an example. We mainly use references from Lie Groups - Beyond an Introduction. (abbr. LG-BaI)
## Root System and Dynkin Diagram
### Cartan Subalgebra
Consider the adjoint representation $ad:\mathfrak{g}\rightarrow\mathrm{End}(\mathfrak{g})$. For any $X\in\mathfrak{g}$, suppose$$
\det(tI-ad_X)=t^d+a_{d-1}t^{d-1}+\cdots+a_r(X)t^r,
$$where $d=\dim\mathfrak{g}$ and $r=\dim\mathfrak{g}_{0,X}$. ($\mathfrak{g}_{0,X}$ is the eignspace of $ad_X$ with eignvalue $0$.) Define$$
\begin{align}
l_\mathfrak{g}(\mathfrak{g})&=\min_{X\in\mathfrak{g}}\dim\mathfrak{g}_{0,X}\\
R_\mathfrak{g}(\mathfrak{g})&=\{X\in\mathfrak{g}\,|\,\dim\mathfrak{g}_{0,X}=l_\mathfrak{g}(\mathfrak{g})\}
\end{align}
$$Then elements of $R_\mathfrak{g}(\mathfrak{g})$ are called regular elements of $\mathfrak{g}$. Recall that if $X$ is a regular element of the finite-dimensional complex Lie algebra $\mathfrak{g}$, then the Lie algebra $\mathfrak{g}_{0,X}$ is a Cartan subalgebra of $\mathfrak{g}$. (Theorem 2.9', LG-BaI) Notice also that the set of non-regular elements is a lower dimensional subvariety.

So in practice, we choose a diagonal or block diagonal matrix $X\in\mathfrak{g}$, and solve the equation for $Y$:$$
[X,Y]=0.
$$Then if the dimension of the solution space is 