#Algebraic-Geometry #Commutative-Algebra 
This is an important exercise from Hartshorne, II.3.22. See also Ex. II.3.21. for key properties on dimensions.
Let $f:X\rightarrow Y$ be a dominant morphism of integral schemes of finite type over a field $k$.

(a). Let $Y'$ be a closed irreducible subset of $Y$, whose generic point $\eta'$ is contained in $f(X)$. Let $Z$ be any irreducible component of $f^{-1}(Y')$, such that $\eta'\in f(Z)$, and show that $\text{codim}\,(Z,X)\leq\text{codim}\,(Y',Y)$.
**Important Remark.** When writing a proof, we often first reduce the problem to the affine case or at least show that we can patch affine cases up to the general case. However, when solving the problem, it is always better to solve for the affine case first, since this is always where the original idea of the proposition came from, this helps us to see why it is true and this can surely strengthen our confidence by providing concrete objects to work with. Besides, even if the problem doesn't seem to be local, working in the affine case can help to build intuition on or even give a direct hint on the solution to the general case!
In the affine case, here's a translation table of the properties:
1. Let $X=\text{Spec}\,A$ and $Y=\text{Spec}\,B$, then $f$ corresponds to a ring homomorphism $\varphi:B\rightarrow A$. The basic assumptions translate to: $A$ and $B$ are integral domains which are finitely generated algebras over a field $k$ and $\varphi$ is injective.
2. $Y'$ corresponds to a prime ideal $\mathfrak{q}\subset B$ and there's a prime ideal $\mathfrak{p'}\subset A$ such that $\mathfrak{p'}\cap B=\mathfrak{q}$.
3. $Z$ corresponds to a minimal prime ideal $\mathfrak{p}$ over $\mathfrak{q}A$ such that $\mathfrak{p}\cap B\subset\mathfrak{q}$.
4. $\text{codim}\,(Z,X)=\text{dim}\,B/\mathfrak{p}$ and $\text{codim}\,(Y',Y)=\text{dim}\,A/\mathfrak{q}$.
So $\mathfrak{p}\cap B\subset\mathfrak{q}\subset\mathfrak{q}A\cap B\subset\mathfrak{p}\cap B$ and $\mathfrak{q}=\mathfrak{p}\cap B$. Therefore $B/\mathfrak{p}$ is a subring of $A/\mathfrak{q}$. Now since these are finitely generated algebras over $k$, we have $\text{dim}\,B/\mathfrak{p}=\text{tr.deg}_k\,\text{Frac}\,B/\mathfrak{p}\leq\text{tr.deg}_k\,\text{Frac}\,A/\mathfrak{q}=\text{dim}\,A/\mathfrak{q}$.
Now for the general case, take an affine open nbhd $U=\text{Spec}\,B$ of $\eta'$ then by Ex. II.3.21. we have $\text{codim}\,(Y'\cap U,U)=\text{dim}\,U-\text{dim}\,Y'\cap U=\text{dim}\,Y-\text{dim}\,Y'=\text{codim}\,(Y',Y)$. 
For $Z$ and $X$ we need a topological lemma:
**Lemma.** Let $f:X\rightarrow Y$ be a continuous map between topological spaces, and $A\subset X$, $B\subset Y$. Then $f(\overline{A})\subset\overline{f(A)}$ and $\overline{f^{-1}(B)} ⊆ f^{-1}(\overline{B})$. And the other directions generally don't hold.
**Corollary.** Let $f:X\rightarrow Y$ be a continuous map between Zariski spaces, $Z\subset X$ is a closed irreducible set and $x\in Z$ is the generic point of $Z$. Then $\overline{f(Z)}=\overline{f(x)}$. In particular, if $Y$ is irreducible and $\eta$ is the generic point of $Y$, then for any $x\in X$, $f(x)=\eta$ if and only if ${f\bigr|}_Z$ is dominant (i.e., $\overline{f(Z)}=Y$).
**Proof.** $f(Z)\subset \overline{f(x)}$, so $\overline{f(Z)}\subset\overline{f(x)}$. The other direction is trivial. And $f(x)=\eta\iff\overline{f(Z)}=\overline{f(x)}=Y$$$\tag*{$\square$}$$Here's something about generically finiteness:
**Definition.** A morphism $f:X\rightarrow Y$ with $Y$ irreducible, is generically finite if $f^{-1}(\eta)$ is a finite set, where $\eta$ is the generic point of $Y$.
**Corollay.** Let  be a morphism with  irreducible. Then $f$ is generically finite if and only if  has only finitely many irreducible closed subsets which are mapped dominantly onto . In particular, if  is dominant (i.e., $f^{-1}(\eta)\neq\varnothing$) and generically finite then $X$ has and only finitely many irreducible components which are mapped dominantly onto.
Now get back to the original problem.
With the lemma we can show that $f(\eta_Z)=\eta'$ where $\eta_Z$ is the generic point of $Z$. Let $V=\text{Spec}\,B$ be an affine open nbhd of $\eta_Z$ contained in $f^{-1}(U)$, then we can prove similarly that $\text{codim}\,(Z\cap V,V)=\text{codim}\,(Z,X)$. Now restrict $f$ onto $V$, and show that all conditions hold for ${f\big|}_V:V\rightarrow U$. So we have reduced to the affine case, which has been proved already.
This argument has a useful byproduct:
**Proposition.** Let $f:X\rightarrow Y$ be a dominant morphism between integral schemes which are of finite-type over a field $k$, then $\text{dim}\,Y\leq \text{dim}\,X$.
**Proof.** Just take affine open subsets as above to boil the problem to the affine case then consider the transcendence degree.$$\tag*{$\square$}$$**Remark.** This is another example of [[Trick of Essentially Local So Just The Affine Case]]. Dimensions involving integral schemes of finite-type over a field $k$ are essentially local!

(b). Let $e=\text{dim}\,X-\text{dim}\,Y$ be the relative dimension of $X$ over $Y$. For any point $y\in f(X)$, show that every irreducible component of the fibre $X_y$ has dimension $\geq e$.
By Hartshorne, Ex. II.3.10., $\text{sp}\,X_y\cong f^{-1}(y)$. Let $Z'$ be an irreducible component of $f^{-1}(y)$ and $Y'=\overline{\{y\}}$. Then $Z'\subset f^{-1}(y)\subset f^{-1}(Y')$ and there's an irreducible component $Z$ of $f^{-1}(Y')$ containing $Z'$. Notice that this choice of $Z$ guarantees that $y\in f(Z)$. Then by $\text{dim}\,X-\text{dim}\,Z\leq\text{dim}\,Y-\text{dim}\,Y'$ it suffices to show that $\text{dim}\,Z'\geq\text{dim}\,Z-\text{dim}\,Y'$.
Consider the affine case:
1. $Y'=V(\mathfrak{q})$ where $y=\mathfrak{q}$ as a point. $Z=V(\mathfrak{p})$ where $\mathfrak{p}$ is a minimal prime over $\mathfrak{q}A$ and $\mathfrak{p}\cap B=\mathfrak{q}$. So $B/\mathfrak{q}$ is a subring of $A/\mathfrak{p}$. $X_y=\text{Spec}\,k(\mathfrak{q})\otimes_B A$ and $Z'$ corresponds to a minimal prime $\mathfrak{p}'$ of $k(\mathfrak{q})\otimes_B A$. $By the choice of $Z$, under the homeomorphism $\text{Spec}\,k(\mathfrak{q})\otimes_B A\cong\varphi^{*-1}(\mathfrak{q})$, $\mathfrak{p}'$ corresponds to $\mathfrak{p}$. All rings are finitely generated algebras over $k$.
2. $\text{dim}\,Z'=\text{dim}\,k(\mathfrak{q})\otimes_B A$, $\text{dim}\,Z=\text{dim}\,A/\mathfrak{p}$ and $\text{dim}\,Y'=\text{dim}\,B/\mathfrak{q}$.
Consider the field extension tower: $k\subset\text{Frac}\,B/\mathfrak{q}=k(\mathfrak{q})\subset\text{Frac}\,A/\mathfrak{p}=k(\mathfrak{p})$. We have $\text{dim}\,Z-\text{dim}\,Y'=\text{tr.deg}_{k(\mathfrak{q})}\,k(\mathfrak{p})$. $k(\mathfrak{q})\otimes_B A\cong k(\mathfrak{q})\otimes_{B/\mathfrak{q}}B/\mathfrak{q}\otimes_B A\cong k(\mathfrak{q})\otimes_{B/\mathfrak{q}} A/\mathfrak{q}A\cong S^{-1}(A/\mathfrak{q}A)$, where $S=B/\mathfrak{q}-{0}$. And under this isomorphism $k(\mathfrak{q})\otimes_B A/\mathfrak{p}'\cong S^{-1}(A/\mathfrak{q}A)/S^{-1}(\mathfrak{p}/\mathfrak{q}A)\cong S^{-1}(A/\mathfrak{p})$. Consider $S^{-1}(A/\mathfrak{p})$ as an $k(\mathfrak{q})$-algebra, then $\text{dim}\,Z=\text{tr.deg}_{k(\mathfrak{q})}\text{Frac}\,S^{-1}(A/\mathfrak{p})=\text{tr.deg}_{k(\mathfrak{q})}\,k(\mathfrak{p})=\text{dim}\,Z-\text{dim}\,Y'$.
Now for the general case, choosing affine nbhds as above, we can prove the same.
**Remark.** The key idea here is to view the fibre $X_y$ as a scheme over $k(y)$ rather than over $k$!
These arguments can be concluded as a lemma:
**Lemma.** Let $f:X\rightarrow Y$ be a dominant morphism between integral schemes of finite-type over a field $k$. For any $y\in f(X)$, let $Y'=\overline{\{y\}}$. Let $Z'$ be any irreducible component of $\text{sp}\,X_y=f^{-1}(y)$, and let $Z$ be the irreducible component of $f^{-1}(Y')$ containing $Z'$. Then we have $\text{dim}\,Z'=\text{dim}\,Z-\text{dim}\,Y'$. In particular, if $y$ is the generic point of $Y$, then $\text{dim}\,Z'=e$.

(c). Show that there is a dense open subset $U\subset X$, such that for any $y\in f(U)$, $\text{dim}\,U_y=e$.
This uses Hartshorne, Ex. II.3.7:
**Lemma.** Let $f:X\rightarrow Y$ be a dominant, generically finite morphism of finite type of integral schemes. Then there is an open subset $U\subset Y$ such that the induced morphism $f^{-1}(U)\rightarrow U$ is finite.
**Proof.** First consider the affine case. Conditions translate into:
1. $Y=\text{Spec}\,B$, $X=\text{Spec}\,A$, $B$ is a subring of $A$, these are integral domains, and $A$ is a finitely-generated $B$-algebra. Say $A=B[x_1,\dots,x_n]/I$ where $I$ is a prime ideal.
2. $\text{Spec}\,S^{-1}A$ is a finite set, where $S=B-{0}$.
Firstly, (by the hint) we need to show that $K(A)=\text{Frac}\,A$ is a finite extension field of $K(B)=\text{Frac}\,B$. Observe that $K(A)/K(B)$ is a finitely generated field extension, so it suffices to prove that $\text{tr.deg}_{K(B)}K(A)=\text{dim}\,S^{-1}A=0$. Since $K(B)\subset S^{-1}A=K(B)[x_1,\dots,x_n]/I^e$ is a finitely generated $K(B)$-algebra, applying [Noether's Normalization Lemma](Noether's%20Normalization%20&%20Geometrical%20Interpretation.md), we get $K(B)\subset K(B)[y_1,\dots,y_r]\subset S^{-1}A$, where the second extension is integral. So the induced map $\text{Spec}\,S^{-1}A\rightarrow\text{Spec}\,K(B)[y_1,\dots,y_r]$ is surjective. If $r>0$, then $K(B)[y_1,\dots,y_r]$ must have infinitely many primes (Euclid's proof applies). So $\text{dim}\,S^{-1}A=\text{dim}\,K(B)=0$.
Suppose $A=B[a_1,\dots,a_n]$, then $S^{-1}A=K(B)[a_1,\dots,a_n]=K(B)(a_1,\dots,a_n)=K(A)$, where all $a_i$'s are algebraic over $K(B)$. Therefore, $K(A)=Let $p_i$ be the monic minimal polynomial of $a_i$ over $K(B)$ and let $b$ be the product of all denominators appeared in all $p_i$'s. Consider $B_b\subset A_b$. By the construction, this is an integral extension and hence $A_b$ is a finitely generated $B_b$-module. Hence we can choose $U=D(b)\cong\text{Spec}\,B_b$ and we have $f^{-1}(U)=f^{-1}(D_B(b))=D_A(b)\cong\text{Spec}\,A_b$. Clearly the induced map is finite.
Now we reduce the general case to the affine case. Clearly $K(X)/K(Y)$ is a finite field extension. Replacing $Y$ by an affine open nbhd $U_1=\text{Spec}\,B$ of $\eta_Y$, we reduce to the case where $f:X\rightarrow\text{Spec}\,B$ is a dominant morphism of finite type between integral schemes which induces a finite field extension $K(X)/K(B)$. Then $X$ is covered by finitely $V_i=\text{Spec}\,A_i$ where $A_i$'s are finitely generated $B$-algebras. Since $X$ is irreducible, the restriction of  to each $V_i$ is again dominant. Hence we obtain monomorphisms of rings $B\rightarrow A_i$. Notice that the generic point of $X$ is contained in all $V_i$'s, so $K(A_i)/K(B)$ are all finite field extensions. Let $b_{i}$ be chosen as above for each $B\subset A_i$, then let $b$ be the product of $b_i$'s. Taking and verifying $U=D(b)$ would finish the proof.$$\tag*{$\square$}$$**Remark.** From the proof of the lemma, we see that the algebraic source of "generically finite" corresponds to 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

\end{tikzcd}
\end{document}
```
Now let's get back to the original problem. By taking an affine chart of $Y$ and then taking an affine chart of $X$ mapped into $Y$ we can reduce the problem to the affine case.
Suppose $A=B[a_1,\dots,a_n]$ and denote $S=B-0$. In the first place we see that $f$ is in general not generically finite. So (by the hint) we apply [Noether's Normalization Lemma](Noether's%20Normalization%20&%20Geometrical%20Interpretation.md) to $K(B)\subset S^{-1}A$, we get a set of transcendental elements $x_1,\dots,x_r$ such that $K(B)[x_1,\dots,x_r]\subset S^{-1}A$ is an integral extension. Then $x_1,\dots,x_r$ would be a transcendental base for $K(A)/K(B)$ so $r=e$. Let $X_1=\text{Spec}\,B[x_1,\dots,x_e]$. Notice that via multiplying $x_i$ by elements in $B$ we could assume that $x_1,\dots,x_e\in A$. Therefore $B[x_1,\dots,x_e]$ is a subring of $A$ and this induces a morphism $X\rightarrow X_1$.
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
	B\ar[r]\ar[d]&B[x_1,\dots,x_e]\ar[r]\ar[d]&A\ar[d]\\
    K(B)\arrow[r]&K(B)[x_1,\dots,x_e]\arrow[r]&S^{-1}A\arrow[r]&K(A)
    

\end{tikzcd}
\end{document}
```
Denote $C=B[x_1,\dots,x_e]$. By the choice of $C$, $K(A)/K(C)$ is a finite field extension. For any $a\in A-0$, there're $c_0,\dots,c_{k-1}\in K(C)$ such that $a^k+c_{k-1}a^{k-1}+\cdots+c_0=0$. Or$$\frac{1}{a}=-\frac{a^{k-1}+c_{k-1}a^{k-2}+\cdots+c_1}{c_0}$$Multiplying by the denominator of $c_0$ in $C$, we see that $K(A)=(C-0)^{-1}A=A\otimes_C K(C)$. Therefore $X\rightarrow X_1$ is a generically finite morphism (actually the fibre contains only one elment) and applying the lemma we obtain an open subset $U'$ of $X_1$ which pulls back to $U\subset X$. Furthermore, by the proof of the lemma, we see that these're all affine, say $U'=\text{Spec}\,C_c$, $U=\text{Spec}\,A_c$ and $A_c$ is a finitely generated $C_c$-module. For any $\mathfrak{q}\in f(U)\subset\text{Spec}\,B$, there exists $\mathfrak{p}\in U$, such that $f(\mathfrak{p})=\mathfrak{q}$, i.e. $c\notin\mathfrak{p}\in\text{Spec}\,A$ and $\mathfrak{p}\cap B=\mathfrak{q}$. $U_y=\text{Spec}\,A_c\otimes_B k(\mathfrak{q})$.
```tikz
\usepackage{tikz-cd}
	\usepackage{amssymb}
\begin{document}
\begin{tikzcd}
	B\ar[r]\ar[d]&C\ar[r]\ar[d]&A\ar[d]\\
    B/\mathfrak{q}\ar[r]&C/\mathfrak{q}'\ar[r]\ar[d]&A/\mathfrak{p}\ar[d]\\
					    &(C/\mathfrak{q}')_{\bar{c}}\ar[r]&(A/\mathfrak{p})_{\bar{c}}
\end{tikzcd}
\end{document}
```
Denote $R_1=C_c\otimes_B k(\mathfrak{q})$, $R_2=A_c\otimes_B k(\mathfrak{q})$. We have $R_2=A_c\otimes_{C_c}R_1$. Since $A_c$ is a finitely generated $C_c$ module, $R_2$ must be a finitely generated $R_1$ module, and hence $R_1\rightarrow R_2$ is integral. Since fibres of an integral homomorphism must be of dimension 0, $\text{dim}\,R_2\leq\text{dim}\,R_1$. Besides, let $S=B-\mathfrak{q}$, then $R_1=C_c\otimes_B S^{-1}B\otimes_B B/\mathfrak{q}=(S{c^k})^{-1}C/\mathfrak{q^e}=(k(\mathfrak{q})[x_1,\dots,x_e])_{\bar{c}}$. Since $\bar{c}\neq0$, we have $\text{dim}\,R_1=\text{dim}\,k(\mathfrak{q})[x_1,\dots,x_e]=e$. (Localizing at $\bar{c}$ is equivalent to taking an nonempty open subset of $\text{Spec}\,R_1$.) Besides, applying (b). to $U\rightarrow X\rightarrow Y$ we see that $\text{dim}\,R_2\geq e$. Therefore, we have $\text{dim}\,U_y=\text{dim}\,R_2=e$.

(d). Going back to our original morphism $f:X\rightarrow Y$, for any integer $h$, let $E_h$ be the set of points $x\in X$ such that, letting $y=f(x)$, there is an irreducible component $Z$ of the fibre $X_y$, containing $x$, and having $\text{dim}\,Z\geq h$. Show that
1. $E_e=X$
2. if $h>e$, then $E_h$ is not dense in $X$
3. $E_h$ is closed, for all $h$
**Remark.** (A). Notice that we could write $E_h(f)=\{x\in X\,\bigr|\,\text{dim}_xX_{f(x)}\geq h\}$, where $\text{dim}_x$ denotes the local dimension at $x$, i.e. the supreme of dimensions of the irreducible components containing $x$.
(B). Actually (3). holds as long as $X$ and $Y$ are of finite type over a field $k$. Because the proposition of purely about the underlying topological spaces and we may assume that $X$ and $Y$ are irreducible by considering their irreducible components, which form a closed cover of each space. Then $X$ and $Y$ are already integral. Furthermore, we may assume that $f$ is dominant since we could replace $Y$ by $\overline{f(X)}$. Verify that this doesn't change the fibre.
(1). follows immediately from (b). and (2). follows immediately from (c). As for (3)., we prove by induction on $n=\text{dim}\,X$.
When $n=0$, $\text{sp}\,X$ must be discrete. There's nothing to prove.
Suppose we have proved for $\text{dim}\,X<n$ and now $\text{dim}\,X=n$. Cover $Y$ by affine charts $\{U\}$ and pull this covering back to $X$. $E_h$ is closed if and only it is closed in every $f^{-1}(U)$. So we may assume that $Y=\text{Spec}\,B$. For the same reason, we may assume that $X=\text{Spec}\,A$ and that $B$ is a subring of $A$.
For any $x$ in the open set $U$ of (c)., we have $\text{dim}\,Z=\text{dim}\,Z\cap U\leq\text{dim}\,U_{f(x)}=e$, where $Z$ is any irreducible component of $f^{-1}(Z)$ containing $x$. By (b)., we see that $\text{dim}\,Z=e$ and therefore $\text{dim}_xX_{f(x)}=e$.
For $h\leq e$, by (b)., $E_h=X$. Now suppose $h>e$. By the previous paragraph, we have seen that $E_h\subset X-U=X'$. Endow $X'$ with the reduced induced closed subscheme structure, i.e., $X'=\text{Spec}\,A/I$ with $\sqrt{I}=I$. (The ring sheaf structure over $X'$ is irrelevant since the statement to be prove is purely topological.) We must have $\text{dim}\,X'<\text{dim}\,X$ since $X'$ is a proper closed subscheme of $X$ and $X$ is irreducible.
For any $x\in E_h=E_h(f)$, denote $y=f(x)$. We claim that the fibre $f^{-1}(y)$ is contained in $X'$. Because otherwise, say there exists $z\in U$ such that $f(z)=y$, then by the previous paragraph, $\text{dim}_zX_y=e<h$,, which is a contradiction. Hence $X'_y=X_y$ and $\text{dim}_xX'_y\geq h$. Therefore $E_h(f)\subset E_h({f\bigr|}_{X'})$.
Conversely, for any $x\in E_h({f\bigr|}_{X'})$, denote $y=f(x)$. Let $Z'$ be an irreducible component of $X'_y=X_y\cap X'$ containing $x$ such that $\text{dim}\,Z'\geq h$. Then $Z'$ is also an irreducible closed subset of $X_y$ and is hence contained in an irreducible component $Z$ of $X_y$. Therefore $\text{dim}_xX\geq\text{dim}\,Z\geq\text{dim}\,Z'\geq h$ and $x\in E_h(f)$. So we must have $E_h(f)=E_h({f\bigr|}_{X'})$, which is a closed subset of $X$.

(e). The main theorem.
**Theorem. (Chevalley)** For each integer $h$, let $C_h$ be the set of points $y\in Y$ such that $\text{dim}\,X_y=h$. Then the subsets $C_h$ are constructible, and $C_e$ contains an open dense subset of $Y$.
**Proof.** The second part of the theorem is proved in the repeatedly used paragraph of (d).
Denote $C_h^+=\{y\in Y\,\bigr|\,\text{dim}\,X_y\geq h\}$, we have $C_h=C_h^+\cap (C_{h+1}^+)^c$. So it suffices to prove that $C_h^+$ is constructible for any $h$. We claim that $C_h^+=f(E_h)$, then the proof follows by the fact that the image of a constructible set is again constructible (see Hartshorne, Ex. II.3.19).
For any $x\in E_h$, let $y=f(x)$. Then $\text{dim}\,X_y\geq\text{dim}_xX_y\geq h$ and therefore $y\in C_h^+$. Conversely for any $y\in C_h^+$. If $y\notin X$, then $X_y$ is empty and $h$ must be non-positive and the proof follows by a previous lemma stating that $e\geq 0$ and an easy discussion for $e=0$. Otherwise, let $x\in X_y$ be contained in the irreducible component of maximum dimension. Then $\text{dim}_xX_y=\text{dim}\,X_y\geq h$ and $y=f(x)\in f(E_h)$.$$\tag*{$\square$}$$