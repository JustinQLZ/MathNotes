#Algebraic-Geometry 
Interesting ones are 7, 10, 19, 20, 24, 28, 29.
$k$ is an algebraically closed field throughout.
#### 1. An affine $k$-scheme $X$ that is reduced and quasi-compact, but not integral.
Consider the $k$-algebra $k\rightarrow k\times k$ decided by $1\mapsto (1,1)$ and let $X=\mathrm{Spec}\,k\times k$.
Clearly $k\times k$ is a reduced ring which is not integral, so $X$ is reduced by not integral. Since $X$ is affine, it must be quasi-compact.
#### 2. An affine $k$-scheme $X$ that is irreducible but not reduced.
Let $X=\mathrm{Spec}\,k[x]/(x^2)$.
A prime ideal of $k[x]/(x^2)$ is of the form $(\bar{f})$ where $f$ is an irreducible polynomial and $f\bigr|x^2$. Therefore $(\bar{f})=(\bar{x})$. So $\mathrm{nil}\,k[x]/(x^2)=(\bar{x})$ which is a prime ideal and hence $X$ is irreducible. But clearly $k[x]/(x^2)$ is not a reduced ring and so $X$ is not reduced.
#### 3. An integral $k$-scheme $X$ that is separated over $k$ but not proper over $k$.
Let $X=\mathrm{Spec}\,k[x]$.
$X$ is integral since $k[x]$ is an integral domain. Also since the $k$-algebra $k\rightarrow k[x]$ is affine we see that $X$ is separated over $k$. Now to show that $X$ is not proper, notice that $X$ is Noetherian so it suffices to show that the valuative criterion fails. Let $K=k(t)$ and $R=k[t]_{(t)}$, then $R$ is a valuation ring of $K$. Consider the $k$-algebra homomorphism $k[x]\rightarrow k(t)$ decided by $x\mapsto t^{-1}$, then there's a commutative diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
\begin{tikzcd}
	\mathrm{Spec}\,K\ar[r]\ar[d]&X\ar[d]\\
	\mathrm{Spec}\,R\ar[r]&\mathrm{Spec}\,k

\end{tikzcd}
\end{document}
```
but we can't add a morphism $\mathrm{Spec}\,R\rightarrow X$ with the diagram still commutative. Otherwise let this morphism decided by the homomorphism $k[x]\rightarrow R$ which is decided by $x\mapsto f/g$, where $g\notin(t)$. In $K$ we have $f/g=t^{-1}$, i.e. $g=ft\in(t)$, which is a contradiction.
#### 4. A projective $k$-scheme $X$ that is reduced but not integral.
Let $S=k[x,y]/(xy)$ and $X=\mathrm{Proj}\,S$.
$X$ is clearly projective. Being reduced can be checked at the level of stalks. Consider $U=D_+(x)\cong\mathrm{Spec}\,k[y]/(y)$. $U$ is clearly reduced. Symmetrically, let $V=D_+(y)$. Then $U$ and $V$ cover $X$ and are both reduced. So $X$ is reduced. To show that $X$ is not integral, it suffices to show that $U\subsetneq X$ and $U$ is closed hence not dense. The closed point $[0:1]\notin U$ so $U\subsetneq X$. Besides, as classical varieties $U=\{[1:0]\}\subset\{[1:0],[0:1]\}=X$, so clearly it is closed.
#### 5. A projective $k$-scheme $X$ that is not reduced.
Let $S=k[x,y]/(y^2)$ and $X=\mathrm{Proj}\,S$.
$X$ is clearly projective. This time $D_+(x)\cong\mathrm{Spec}\,k[y]/(y^2)$, which is not reduced.
#### 6. A quasi-projective $k$-scheme $X$ that is not projective.
Let $X$ be the affine line $\mathbb{A}_k^1$.
$\mathbb{A}^1_k\rightarrow\mathrm{Spec}\,k$ factors as $\mathbb{A}_k^1\rightarrow\mathbb{P}_k^1\rightarrow\mathrm{Spec}\,k$. The first morphism in the factorization is an open immersion since $\mathbb{P}_k^1=\mathrm{Proj}\,k[x,y]$ and $D_+(x)\cong\mathrm{Spec}\,k[y]=\mathbb{A}_k^1$.
#### 7. A $k$-scheme $X$ that is separated over $k$ but not quasi-compact.
Let $X$ be the disjoint union of $\mathrm{Spec}\,k$ indexed by $\mathbb{N}$.
The underlying topological space of $X$ is countable discrete points, so clearly it's not quasi-compact. $X\times_k X$ is the the disjoint union of $\mathrm{Spec}\,k$ indexed by $\mathbb{N}^2$, which also has discrete topology. So $X$ is separated over $k$.
#### 8. A $k$-scheme $X$ that is quasi-compact but not Noetherian.
Let $X=\mathrm{Spec}\,k[x_1,\dots,x_n,\dots]$.
$X$ is quasi-compact since it's affine. It is not Noetherian since $k[x_1,\dots,x_n,\dots]$ is not a Noetherian ring.
#### 9. A quasi-compact $k$-scheme $X$ that is not separated over $k$.
Let $X$ be the affine line over $k$ with pointe $0$ doubled.
$X$ is not separated by Hartshorne II.4.0.1. Denote the doubled points as $0_+$ and $0_-$ respectively, and take $U=X-\{0_+\}$, $V=X-\{0_-\}$. Then $U$ and $V$ are affine open subsets which cover $X$. So $X$ is quasi-compact.
#### 10. A quasi-compact $k$-scheme $X$ that is not quasi-separated.
Let $S=k[x_1,\dots,x_n,\dots]$ and $U=\mathrm{Spec}\,S-\{(x_1,\dots,x_n,\dots)\}$. Take two copies $S_1$ and $S_2$ of $S$ and let $X_1=\mathrm{Spec}\,S_1$, $X_2=\mathrm{Spec}\,S_2$ along with $U_1$ and $U_2$. Glue $X_1$ and $X_2$ along $U_1\cong U_2$ we obtain $X$.
$X$ is quasi-compact since it's a finite union of its two affine open subsets $X_1$ and $X_2$. Consider $\{D(x_i)\,:\,i=1,2,\dots\}$ which cover $U$. For any finite subcover, WLOG, say $\{D(x_i)\,:\,i=1,2,\dots,n\}$, $\mathfrak{p}=(x_1,\dots,x_n)$ is in $U$ but not covered by it. So $U$ is not quasi-compact. Now the preimage of the open affine subset $X_1\times_kX_2\subset X\times_kX$ under the diagonal morphism, which is precisely $U$, is not quasi-compact. Therefore $X$ is not quasi-separated.
#### 11. A $k$-scheme $X$ that is locally Noetherian but not Noetherian.
The scheme of countable discrete points over $k$ in 7 would be a good example.
#### 12. An integral affine $k$-scheme $X$ such that $X\rightarrow\mathrm{Spec}\,k$ is not locally of finite type.
$X=\mathrm{Spec}\,k[x_1,\dots,x_n,\dots]$. Since $k[x_1,\dots,x_n,\dots]$ is not a finitely generated $k$-algebra.
#### 13. A morphism between $k$-schemes $X\rightarrow Y$ that is of finite type but not finite.
Consider the morphism induced by the $k$-algebra homomorphism $k\rightarrow k[x]$, which is a finitely generated $k$-algebra but $k[x]$ is not a finitely generated $k$-module.
#### 14. A finite morphism $f:X\rightarrow Y$ of $k$-schemes that is not a closed immersion.
Consider the morphism induced by $k\rightarrow k[x]/(x^2)$. Since $k[x]/(x^2)$ is a finite $k$-module, the morphism is finite. However this is not a closed immersion since the both spaces contain only one point and the ring homomorphism over these two points, which is just the ring homomorphism, is not surjective.
#### 15. A closed immersion $i:Z\hookrightarrow X$ of $k$-schemes that is not an open immersion.
Consider the morphism induced by $k[x]\rightarrow k[x]/(x)=k$. The morphism is a closed immersion since the ring homomorphism is surjective. This is not an open immersion since $i(Z)$ is just $\{0\}$, which is not open otherwise we could find a polynomial in $k[x]$ that is zero everywhere other than $0$ but non-zero at $0$, which is impossible.
#### 16. An open immersion $j:U\hookrightarrow X$ of $k$-schemes that is not a closed immersion.
Just take $U$ the complement of $Z$ in 15.
#### 17. An affine morphism $f:X\rightarrow Y$ of $k$-schemes that is not quasi-finite.
Consider the morphism induced by $k[x]\rightarrow k[x]/(x)=k$. The morphism is not quasi-finite since the preimage of the only point of $\mathrm{Spec}\,k$ is the whole affine line $\mathbb{A}_k^1$, which is not a finite set.
(Notice that here quasi-finite means the fiber over each point $y\in f(X)$ is a finite scheme over $\kappa(y)$. But the definition in Hartshorne Ex.II.3.5 just requires that the fiber is a finite set. The first definition clearly implies the second one.)
#### 18. A quasi-finite morphism $f:X\rightarrow Y$ of $k$-schemes that is not finite.
Let $X$ be the affine line over $k$ with 0 doubled as in 9 and $Y=\mathbb{A}_k^1$. Let $f$ be the morphism identifying $0_+$ and $0_-$.
For any $y\in Y$ the fiber has three possibilities. If $y$ is a closed point other than $0$ then the fiber is just $\mathrm{Spec}\,k$ and $\kappa(y)=k$, so the fiber is finite over $\kappa(y)$. If $y$ is 0 then the fiber is a disjoint union of two copies of $\mathrm{Spec}\,k$ which is isomorphic to $\mathrm{Spec}\,k\times k$. Since $k\times k\cong k[t]/(t^2-t)$ is a finite $k$-module, the fiber is also finite. Finally, if $y$ is the generic point, then the fiber contains the generic point of $X$, which as a scheme is isomorphic to $\mathrm{Spec}\,k(t)$, which is a finite $\kappa(y)=\mathrm{Spec}\,k(t)$-module. Therefore $f$ is quasi-finite.
$Y$ is affine but $f^{-1}(Y)=X$ is not affine since $X$ is not separated over $k$. So $f$ is not affine and certainly not finite.
#### 19. A finite proper morphism $f:X\rightarrow Y$ of $k$-schemes that is not an isomorphism.
Consider the morphism induce by $k\rightarrow k\times k$. Geometrically this maps two discrete points to one point, so it's clearly finite. It is clearly separated and of finite type. To see that it's universally closed, consider any base change $Y'\rightarrow Y=\mathrm{Spec}\,k$. $Y'$ is just a scheme over $k$ and $X\times_YY'$ is just the dis joint union of two copies of $Y'$. Then the morphism $X\times _YY'\rightarrow Y'$ is clearly closed since a closed subset of $X\times_Y Y'$ is just a disjoint union of two closed subsets of $Y'$ and its image is just the intersection of them.
For a more non-trivial example, consider the $k$-homomorphism $\varphi:K_1\rightarrow K_2$ between two fields of transcendental degree 1 over $k$. By Hartshorne I.6.12, this corresponds to a dominant morphism $f$ between nonsingular projective curves over $k$. Because the composition of $f$ and $Y\rightarrow\mathrm{Spec}\,k$ is proper and the latter morphism is proper hence separated, so $f$ is proper. Since $f$ is dominant and $X$ is a complete nonsingular curve over $k$, by Hartshorne II.6.8 $f$ is a finite morphism. Finally $f$ is not an isomorphism as long as $K_1\neq K_2$.
#### 20. Assume $\mathrm{char}\,k=p>0$. An integral morphism $f:X\rightarrow Y$ of $k$-schemes that is not finite.
(Here integral morphism means that $f$ is affine and for any $V=\mathrm{Spec}\,B\subset Y$, $f^{-1}(V)=U=\mathrm{Spec}\,A$, then $B\rightarrow A$ is an integral extension.)
Ignoring the assumption, $k[t]\rightarrow k[t,t^{1/2},t^{1/3},\dots]$ would do. But with the assumption we could construct an example with better properties. Consider $B=k[t]\rightarrow k[t,t^{1/p},t^{1/p^2},\dots]=A$. This is clearly integral but not finite.
Fibers are of two types. For any closed point $(t-a)$, the fiber is the spectrum of $A\otimes_{k[t]}k[t]/(t-a)=k[a^{1/p},a^{1/p^2},\dots]=k$ since $k$ is algebraically closed. Notice that we use the fact for any $a\in k$ and $n\in\mathbb{N}$, $x^{p^n}-a=0$ has only one solution in $k$ when $\mathrm{char}\,k=p$ to establish the isomorphisms. For the generic point $(0)$, the fiber is the spectrum of $A\otimes_{k[t]}k(t)=k(t)[t^{1/p},\dots]=k(t,t^{1/p},\dots)$. The last isomorphism holds since $k(t)[t^{1/p},\dots,t^{1/p^n},\dots]$ is the direct limit of the infinite extension tower$$k(t)\subset k(t)[t^{1/p}]\subset k(t)[t^{1/p^2}]\subset\cdots$$where all intermediate rings are actually fields. So the direct limit must also be a field.
Since $B\rightarrow A$ is integral, the corresponding morphism must be surjective. By the discussion of fibers above we see that it is also injective. Now to show that the underlying topological spaces are homeomorphic, it remains to show that the morphism is closed. But this is just another corollary of $B\rightarrow A$ being integral. Therefore the morphism is a homeomorphism between underlying topological spaces.
#### 21. A morphism $f:X\rightarrow\mathrm{Spec}\,k$ that is of finite type but not separated.
Let $X$ be the affine line over $k$ with 0 doubled. Then the morphism is clearly quasi-compact and locally of finite type, hence of finite type. It is not separated by Hartshorne II.4.0.1.
#### 22. A morphism $f:X\rightarrow\mathrm{Spec}\,k$ that is locally of finite type but not of finite type.
Let $X$ be countable discrete points as in 7.
#### 23. A proper morphism $f:X\rightarrow\mathrm{Spec}\,k$ that is not affine.
Just let $X=\mathbb{P}^1_k$ then by Hartshorne Ex.I.3.1.(e) this is not affine.
#### 24. A projective birational morphism $f:X\rightarrow Y$ of varieties over $k$ that is not an isomorphism.
Let $Y$ be any closed subvariety of $\mathbb{A}^n_k$ passing through the original point $O$ and let $X$ be the blowing-up of $Y$ at $O$. Then we have a commutative diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
\begin{tikzcd}
	X\ar[hookrightarrow]{r}\ar[rd,"f"]&Y\times_k\mathbb{P}^{n-1}_k\ar[d]\\
	&Y

\end{tikzcd}
\end{document}
```
The vertical morphism is a closed immersion, hence $f$ is projective. Since $f$ is an isomorphism from $X-f^{-1}(O)$ to $Y-\{O\}$, we see that $f$ is birational. Clearly this is not an isomorphism.
#### 25. In a fixed ambient $k$-scheme $X$, find two closed immersions $i_1:Z_1\hookrightarrow X$ and $i_2:Z_2\hookrightarrow X$ having the same underlying closed subset in $|X|$, with $Z_1$ reduced and $Z_2$ nonreduced.
Take $X=\mathrm{Spec}\,k[x]$, $Z_1=\mathrm{Spec}\,k[x]/(x)=\mathrm{Spec}\,k$ and $Z_2=\mathrm{Spec}\,k[x]/(x^2)$.
#### 26. Find an affine morphism $f:X\rightarrow\mathrm{Spec}\,k$ that is not locally of finite type.
Just take $X=\mathrm{Spec}\,k[x_1,\dots,x_n,\dots]$.
#### 27. For $\mathbb{A}_k^1$ associated with Zariski topology, find a presheaf of abelian groups that is not a sheaf.
$$
\mathcal{F}(U)=
\begin{cases}
\mathbb{Z},&U=\mathbb{A}_k^1;\\
0,&\text{otherwise.}
\end{cases}
$$ and take all restriction homomorphisms zero.
#### 28. A finite birational morphism $f:X\rightarrow Y$ of $k$-schemes that is not an isomorphism.
Let $Y$ be the curve $y^2=x^3$ in $\mathbb{A}^2_k$, i.e. $Y=\mathrm{Spec}\,k[x,y]/(y^2-x^3)\cong\mathrm{Spec}\,k[t^2,t^3]$ and let $X$ be the integral closure of $k[t^2,t^3]$ in its fractional field, i.e. $X=\mathrm{Spec}\,k[t]$. Then let $f$ be the morphism induced by the ring homomorphism $k[t^2,t^3]\subset k[t]$. This is the parameterization of the curve or the normalization of the curve.
Since $k[t]$ is a finitely generated $k[t^2,t^3]$-algebra and integral over $k[t^2,t^3]$, we see that it's a finite $k[t^2,t^3]$-module and hence $f$ is finite. To see that $f$ is birational consider $U=X-\{0\}=D_X(t)\cong\mathrm{Spec}\,k[t,t^{-1}]$. $f(U)=D_Y(t)=\mathrm{Spec}\,k[t^2,t^3]_t=\mathrm{Spec}\,k[t,t^{-1}]$. Hence $f$ is birational. It's clearly not an isomorphism.
#### 29. An open immersion $j:U\hookrightarrow\mathbb{A}_k^2$ that is not an affine morphism.
Let $U=\mathbb{A}_k^2-\{(0,0)\}$. Suppose $U$ is affine, then $U=\mathrm{Spec}\,A$, where $A=\Gamma(U,\mathcal{O}_{\mathbb{A}_k^2})$. Consider the restriction homomorphism $\varphi:k[x,y]\rightarrow A$.
**Claim.** $\varphi$ is an isomorphism.
For any $f\in\ker\varphi$, $f$ could be nonzero only at the point $(0,0)$, but then $f$ must be zero. So $\varphi$ is injective. For any $f\in A$, take any $g\in k[x,y]$ such that $g(0,0)=0$, then $D(g)\subset U$. Since $D(g)\cong\mathrm{Spec}\,k[x,y]_g$, $f\bigr|_{D(g)}$ is of the form $h/g^n$. Now take $g=x$ or $g=y$, we see that on $D(xy)$ $f$ is of the form $h_1/x^n=h_2/y^m$, where $h_1\notin(x)$ and $h_2\notin(y)$. But then $y^mh_1=x^nh_2$ and we must have $n=m=0$. Therefore $f\in k[x,y]$ and $\varphi$ is surjective.
By Hartshorne Ex.II.2.4 or I.3.5, we see that $j$ must be an isomorphism, which is a contradiction.
#### 30. A morphism of ringed spaces $f:(X,\mathcal{O}_X)\rightarrow(Y,\mathcal{O}_Y)$ which is a homeomorphism on the underlying topological spaces but is not an isomorphism of ringed spaces.
Consider the morphism of schemes induced by the ring homomorphism $k[x]/(x^2)\rightarrow k[x]/(x)$.