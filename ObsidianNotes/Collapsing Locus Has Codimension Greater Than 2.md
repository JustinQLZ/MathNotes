#Algebraic-Geometry 
>[!tip] Basic Toolkits For (Fiber) Dimensions
>See Hartshorne Ex.II.3.20 for basics.
>Let $f$ be a dominant morphism between irreducible schemes of finite type over $k$.
>1. Fiber dimension $\geq$ relative dimension $=:e$.
>2. Equity holds at generic point. (Corollary of 4.2)
>3. About $E_h:=\{x\in X\,:\,y=f(x),\exists\text{ irreducible component }Z\subset f^{-1}(y)\;\;x\in Z,\dim Z\geq h\}$:
>	1. $E_e=X$ (i.e. 1).
>	2. If $h>e$, then $E_h$ is *not* dense in $X$.
>	3. $E_h$ is closed for all $h$. (Semicontinuity.)
>4. About $C_h:=\{y\in Y\,:\,\dim f^{-1}(y)=h\}$:
>	1. $C_h$ is constructible.
>	2. $C_e$ contains an open dense subset of $Y$.
>
>Next we consider constructible subsets of a scheme $X$ of finite type over $k$.
>1. Basic facts about constructible sets:
>	1. A subset of $X$ is constructible if and only if it can be written as a finite disjoint union of locally closed subsets.
>	2. Image and inverse image of a constructible subset is constructible.
>	3. $S\subset X$ is closed if and only if it's stable under specializations.
>	4. $S\subset X$ is open if and only if it's stable under generalizations.
>	5. $S\subset X$ is dense in $X$ if and only if generic points of all irreducible component of $X$ are contained in $X$. Furthermore, in that case, it contains a nonempty open subset.
>2. Let $S$ be a constructible subset of $X$, then $S$ contains a nonempty open subset of $\bar{S}$. So $\dim S=\dim\bar{S}$.

These are direct consequences of [[Dimension of the Fibers of a Morphism]], and we won't be referring to it every time, but all we use are from that note, and some results of Hartshorne Ex.II.3.18-19, which are about constructible subsets.
**Lemma.** Let $f:X\rightarrow Y$ be a dominant morphism of irreducible schemes of finite type over a field $k$, then $\dim X=\dim Y+\dim X_{\eta}$, where $\eta$ is the generic point of $Y$.
**Proof.** WLOG, assume that $X$ and $Y$ are reduced. Let $\zeta$ be the generic point of $X$. Since $f$ is dominant, $f(\zeta)=\eta$ and $K(X)$ is an extension of $K(Y)$. $\dim X=\mathrm{tr.d.}\,K(X)/k$ and $\dim Y=\mathrm{tr.d.}\,K(Y)/k$. So $\dim X-\dim Y=\mathrm{tr.d.}\,K(X)/K(Y)$. On the other hand, $\dim X_{\eta}=X\times_Y\mathrm{Spec}\,K(Y)\rightarrow\mathrm{Spec}\,K(Y)$ is of finite type, so $\dim X_{\eta}=\mathrm{tr.d.}\,K(X_{\eta})/K(Y)$. Besides, by calculating with affine open subsets, we see that $K(X_{\eta})=K(X)$. Then the conclusion follows.$$\tag*{$\square$}$$**Lemma.** Let $X$ be a noetherian Zariski space with irreducible components $X_1,\dots,X_r$ and let $S$ be a dense subset of $X$. Then $S\cap X_i$ is dense in $X_i$.
**Proof.** Suppose this is not the case, then, WLOG, there's a proper closed subset $W\subsetneq X_1$ such that $S\cap X_1\subset W$. Then $S=\cup_i(S\cap X_i)\subset W\cup \bigcup_{i\geq2}(S\cap X_i)=:F$. $F$ is a proper closed subset of $X$ and this contradicts the hypothesis of $S$ being dense in $X$.$$\tag*{$\square$}$$**Theorem.** Let $f:X\rightarrow Y$ be a dominant morphism of irreducible schemes of finite type over a field $k$. Denote the relative dimension $e:=\dim X-\dim Y$ and $S:=\{y\in Y\,:\,\dim f^{-1}(y)>e\}$. Then $S$ is constructible in $Y$ and $\mathrm{codim}\,(\bar{S},Y)\geq2$. Also, if $f$ is closed, then $S$ is closed in $Y$.
**Proof.** **Claim.** $S=f(E_{e+1}(f))$. If $x\in E_{e+1}(f)$, then trivially $y=f(x)\in S$. Conversely, if $y\in S$, then choose any point $x$ in an irreducible component of $f^{-1}(y)$ with dimension $\geq e+1$, then $x\in E_{e+1}(f)$. The constructability of $S$ and the last statement follows immediately.
Recall that a constructible subset of an irreducible Zariski space is dense if and only if it contains the generic point. By the first lemma, the generic point of $Y$ is not contained in $S$, so $\bar{S}\neq Y$.
If $\mathrm{codim}\,(\bar{S},Y)=1$, then let $S_0$ be an irreducible component of $\bar{S}$ with $\dim S_0=\dim Y-1$. The closure of $S\cap S_0$ is dense in $S_0$ by the second lemma, so again since $S_0$ is constructible, the generic point $\eta$ of $S_0$ is contained in $S$. Since $\eta\in S$, we have $\dim f^{-1}(\eta)\geq e+1$. Let $W$ be an irreducible component of $f^{-1}(\eta)$ such that $\dim W\geq e+1$, and let $\xi$ be the generic point of $W$. Then let $Z$ be the closure of $\xi$ in $X$, which is irreducible. Since $f(\xi)=\eta$, the restriction $f|_{Z}:Z\rightarrow S_0$ is dominant. So by the first lemma, we have $\dim Z=\dim S_0+\dim Z_{\eta}$. Clearly $W\subset Z$. Since $W\subset f^{-1}(\eta)$, we also have $W\subset Z_{\eta}$. Consequently, $$\dim Z=\dim S_0+\dim Z_{\eta}\geq\dim S_0+\dim W\geq\dim S_0+\dim X-\dim Y+1=\dim X.$$Then since $X$ is irreducible, we must have $Z=X$ and $\xi$ is the generic point of $X$. Since $f(\xi)=\eta$, we have $f(X)\subset S_0$, which contradicts the hypothesis of $f$ being dominant.$$\tag*{$\square$}$$**Remark.** It turns out that such a complicated proof is totally unnecessary... Just use two things:
1. Fiber dimension $\geq$ relative dimension.
2. There are fibers such that equity holds. (Actually, there's a dense open subset $U\subset X$ such that equity holds on $f(U)$.)
So we have $\dim f^{-1}(S)=\dim S+\dim f^{-1}(\eta)$, where $\eta\in S$. By the definition of $S$, $\dim f^{-1}(\eta)\geq\dim X-\dim Y+1$, so if $\mathrm{codim}\,(S,Y)=1$, then $$\dim f^{-1}(S)\geq\dim Y-1+\dim X-\dim Y+1=\dim X.$$Therefore $X=f^{-1}(S)$, which is a contradiction.
Also, the fact that **a constructible subset of an irreducible Zariski space is dense if and only if it contains the generic point** is very useful!
