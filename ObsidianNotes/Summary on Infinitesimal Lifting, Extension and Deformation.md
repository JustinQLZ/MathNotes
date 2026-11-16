#Algebraic-Geometry #Commutative-Algebra 
#### Infinitesimal Lifting
(Hartshorne, Ex.II.8.6) Let $k$ be an algebraically closed field, let $A$ be a finitely generated $k$-domain. Let $0\rightarrow I\rightarrow B'\rightarrow B\rightarrow0$ be an exact sequence, where $B'$ is a $k$-algebra, and $I$ is an ideal with $I^2=0$. Finally suppose given a $k$-algebra homomorphism $f:A\rightarrow B$. Any $k$-algebra homomorphism $g:A\rightarrow B'$ making a commutative diagram
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	&0\arrow[d]\\
	&I\arrow[d]\\
	&B'\arrow[d, "\pi"]\\
	A\arrow[ru, dashed, "g"]\arrow[r, "f"]&B\arrow[d]\\
	&0

\end{tikzcd}
\end{document}
```
is called a infinitesimal lifting of $f$.
**Proposition. (Infinitesimal Lifting Property)** If $\mathrm{Spec}\,A$ is nonsingular, i.e. all local rings of $A$ are regular, then there exists a lifting of $f$.
###### *Step 1.* Classification of liftings.
We will show that liftings of $f$ have a $\mathrm{Hom}_A\,(\Omega_{A/k},I)$-torsor structure. We will see that the hypothesis of $k$ being a field is not used in this step, so we can replace $k$ with arbitrary commutative ring. This observation will be used later in the section of infinitesimal deformations.
First suppose that $g,g':A\rightarrow B'$ are given liftings of $f$.
**Claim.** $\theta=g-g'$ is a $k$-derivation of $A$ into $I$, which we can consider as an element of $\mathrm{Hom}_A\,(\Omega_{A/k},I)$. Note that since $I^2=0$, $I$ has a natural structure of $B$-module and hence also of $A$-module.
>[!note]- proof
>Clearly $\theta$ is $k$-linear and $\mathrm{im}\,\theta\subset I$. For any $a,b\in A$, $$
>\begin{align}
>a\theta(b)+b\theta(a)&=f(a)(g(b)-g'(b))+f(b)(g(a)-g'(a))\\
>&=g(a)(g(b)-g'(b))+g'(b)(g(a)-g'(a))\\
>&=g(ab)-g(a)g'(b)+g'(b)g(a)-g'(ab)\\&
>=\theta(ab).
>\end{align}$$

Conversely, for any $\theta\in\mathrm{Hom}_A\,(\Omega_{A/k},I)$, $g'=g+\theta$ is another lifting of $f$.
>[!note]- proof
>Clearly $g'$ is $k$-linear and $\pi\circ g'=f$. For any $a,b\in A$,$$
>\begin{align}
>g'(a)g'(b)&=(g(a)+\theta(a))(g(b)+\theta(b))\\
>&=g(ab)+g(a)\theta(b)+g(b)\theta(a)+\theta(a)\theta(b)\\
>&=g(ab)+a\theta(b)+b\theta(a)\\
>&=g(ab).
>\end{align}$$

###### *Step 2.* Nonsingularity implies existence of liting.
Let $P=k[x_1,\dots,x_n]$ of which $A$ is a quotient, and let $J$ be the kernel.
**Claim.** There exists a $k$-homomorphism $h:P\rightarrow B'$ making a commutative diagram
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	0\arrow[d]&0\arrow[d]\\
	J\arrow[d]&I\arrow[d]\\
	P\arrow[r, "h"]\arrow[d, "\pi'"]&B'\arrow[d, "\pi"]\\
	A\arrow[r, "f"]\arrow[d]&B\arrow[d]\\
	0&0

\end{tikzcd}
\end{document}
```
and $h$ induces an $A$-linear map $\bar{h}:J/J^2\rightarrow I$.
>[!note]- proof
>For each $i$ choose $y_i\in B'$ such that $\pi(y_i)=f(\pi'(x_i))$, then let $h(x_i)=y_i$.  For each $\bar{a}\in J/J^2$, let $\bar{h}(\bar{a})=h(a)$. By diagram chasing we see that $a\in J$ implies that $h(a)\in I$. For any $rs\in J^2$, $h(rs)\in I^2$, so $\bar{h}$ is well-defined. Finally, for any $r'=\pi'(r)\in A$, $\bar{h}(r'a)=h(ra)=h(r)h(a)=r'\bar{h}(a)$.

Now, the hypothesis $\mathrm{Spec}\,A$ nonsingular and Hartshorne, II.8.17 gives an exact sequence$$0\longrightarrow J/J^2\longrightarrow\Omega_{P/k}\otimes_PA\longrightarrow\Omega_{A/k}\longrightarrow0.$$Since $\Omega_{A/k}$ is locally free by Hartshorne, II.8.15, applying the functor $\mathrm{Hom}_A\,(\cdot,I)$ gives an exact sequence$$0\longrightarrow\mathrm{Hom}_A\,(\Omega_{A/k},I)\longrightarrow\mathrm{Hom}_P\,(\Omega_{P/k},I)\longrightarrow\mathrm{Hom}_A\,(J/J^2,I)\longrightarrow0.$$Let $\theta\in\mathrm{Hom}_P\,(\Omega_{P/k},I)$ be an element whose image gives $\bar{h}\in\mathrm{Hom}_A(J/J^2,I)$. Consider $\theta$ as a derivation of $P$ to $B'$. Then let $h'=h-\theta$.
**Claim.** $h'$ is a homomorphism of $P\rightarrow B'$ such that $h'(J)=0$.
>[!note]- proof
>By the same argument replacing $A$ with $P$, we see that $h'$ is a well-defined $k$-homomorphism making the diagram commute. Then by construction, the induced $A$-linear map $\bar{h}':J/J^2\rightarrow I$ is zero, which implies that $h'(J)=0$.

Thus $h'$ induces the desired homomorphism $g:A\rightarrow B'$.
**Remark.** Once we know that $h$ exists, rest arguments constructing $g$ don't require $P$ to be a polynomial ring.
#### Infinitesimal Extension
(Hartshorne, Ex.II.8.7) As an application of the infinitesimal property, we consider the following general problem. Let $X$ be a scheme of finite type over $k$, and let $\mathcal{F}$ be a coherent sheaf on $X$. We seek to classify schemes $X'$ over $k$, which have a sheaf of ideals $\mathcal{I}$ such that $\mathcal{I}^2=0$ and $(X',\mathcal{O}_{X'}/\mathcal{I})\cong(X,\mathcal{O}_X)$, and such that $\mathcal{I}$ with its resulting structure of $\mathcal{O}_X$-module is isomorphic to the given sheaf $\mathcal{F}$. Such a pair $X', \mathcal{I}$ we call an *infinitesimal extension* of the scheme $X$ by the sheaf $\mathcal{F}$.
###### The trivial extension.
Take $\mathcal{O}_{X'}=\mathcal{O}_X\oplus\mathcal{F}$ as a sheaf of abelian groups, and define multiplication by $(a\oplus f)\cdot(a'\oplus f')=aa'\oplus(af'+a'f)$.
**Claim.** $(\mathrm{sp}\,X,\mathcal{O}_{X'})$ with $\mathcal{I}=0\oplus\mathcal{F}$ is an infinitesimal extension of $X$ by $\mathcal{F}$. (trivial)
###### A special case: $X$ is affine and nonsingular.
**Proposition.** $X$ is affine and nonsingular, then for any coherent sheaf $\mathcal{F}$ on $X$, any extension of $X$ by $\mathcal{F}$ is isomorphic to the trivial one.
**Proof.** Let $X=\mathrm{Spec}\,A$, and $M$ a finitely generated $A$-module. Let $A'=A\oplus M$ and $J=0\oplus M$, corresponding to the trivial extension. Let $X',\mathcal{I}$ be an infinitesimal extension of $X$ by $\mathcal{F}=\tilde{M}$. Take $B'=\Gamma(X',\mathcal{O}_{X'})$ and $I=\Gamma(X',\mathcal{I})\subset B'$.
**Claim.** $X'=\mathrm{Spec}\,B'$. Recall that $X'$ is affine if and only if $X'_{red}$ is affine. $\mathcal{I}^2=0$ implies that $X_{red}=X'_{red}$. Since $X$ is affine, we see that $X'$ is also affine. $B=B'/I=A$. Then a splitting of the exact sequence $$0\longrightarrow I\longrightarrow B'\longrightarrow B \longrightarrow0$$exists by the infinitesimal lifting property. So $B'=B\oplus I$. By definition, $J$ as a $B$-module is isomorphic to $I$ as an $A$-module, so $B'=B\oplus I=A\oplus J=A'$, and the extension $X',\mathcal{I}$ is isomorphic to the trivial one.$$\tag*{$\square$}$$
###### Classification of infinitesimal extension.
(Hartshorne, Ex.III.4.10)
**Proposition.** Let $X$ be a nonsingular variety over an algebraically closed field $k$, and let $\mathcal{F}$ be a coherent sheaf on $X$. Then there is a one-to-one correspondence between the set of infinitesimal extensions of $X$ by $\mathcal{F}$ up to isomorphism, and the group $H^1(X,\mathcal{F}\otimes\mathcal{T})$, where $\mathcal{T}=\Omega_{X/k}^{\vee}$ is the tangent sheaf of $X$.
**Proof.** By the special case above, infinitesimal extensions are locally trivial. So the classical calculations via Čech cohomology apply and we need to show that automorphisms of the trivial extension $A\oplus M$ corresponds to $k$-derivations from $A$ to $M$.
Any automorphism $\varphi$ must fit in the following commutative diagram:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	0\arrow[r]&M\arrow[d, equal]\arrow[r]&A\oplus M\arrow[d, "\varphi"]\arrow[r]&A\arrow[d, equal]\arrow[r]&0\\
	0\arrow[r]&M\arrow[r]&A\oplus M\arrow[r]&A\arrow[r]&0

\end{tikzcd}
\end{document}
```
The right hand side square commutes if and only if for each $(a,m)\in A\oplus M$, $\varphi(a,m)=(a,\varphi^2(a,m))$. If the right hand side square commutes, then the left hand side square commutes if and only if $\varphi(0,m)=(0,\varphi^2(0,m))=(0,m)$, i.e. $\varphi^2(0,m)=m$ and $\varphi(a,m)=(a,D(a)+m)$, where $D(a)=\varphi^2(a,0)$. Now, if the diagram commutes, then $\varphi$ is a $k$-algebra homomorphism implies that for any $a,a'\in A$, $\varphi(aa',0)=(aa',D(aa'))=(a,D(a))(a',D(a'))=(aa',aD(a')+a'D(a))$ and $D$ is $k$-linear, i.e. $D$ is a $k$-derivation from $A$ to $M$. Conversely, one can verify that if $D$ is a $k$-derivation from $A$ to $M$ then $\varphi(a,m)=(a,D(a)+m)$ is an automorphism of the trivial extension.$$\tag*{$\square$}$$
#### Infinitesimal Deformation
###### Classification of infinitesimal deformation for a closed subscheme.
(Hartshorne, Ex.III.9.7) Let $Y\subset X$ be a closed subscheme, where $X$ is a scheme of finite type over a field $k$. Let $D=k[t]/t^2$ be the ring of dual numbers, and define an *infinitesimal deformation of $\,Y$ as a closed subscheme of $X$*, to be a closed subscheme $Y'\subset X\times_kD$, which is flat over $D$, and whose closed fiber is $Y$.
**Lemma.** A $D$-module $M$ is flat if and only if $\forall m\in M\;\;tm=0\implies m\in tM$.
**Proof.** If $M$ is flat, then applying $-\otimes_DM$ to the exact sequence$$0\longrightarrow tD\longrightarrow D\overset{\times t}{\longrightarrow} D$$shows that for any $m\in M$, $tm=0$ if and only if $m\in tM$. Conversely, suppose that $\forall m\in M\;\;tm=0\implies m\in tM$, then $tM$ is the kernel of $M\xrightarrow{\times t}M$ since $t^2=0\in D$. So $tM=tD\otimes_D M\rightarrow M$ is injective. But since $tD$ is the only maximal ideal of $D$, this implies that $M$ is flat.$$\tag*{$\square$}$$**Proposition.** Let $Y\subset X$ be a closed subscheme, where $X$ is a scheme of finite type over a field $k$. Then infinitesimal deformations of $Y$ as a closed subscheme of $X$ are classified by $H^0(Y,\mathcal{N}_{Y/X})$, where $\mathcal{N}_{Y/X}=\mathcal{Hom}_Y\,(\mathcal{I}_Y/\mathcal{I}_Y^2,\mathcal{O}_Y)$ is the normal sheaf of $Y$ in $X$, i.e. they're classified by $\mathrm{Hom}_Y(\mathcal{I}_Y/\mathcal{I}_Y^2,\mathcal{O}_Y)=\mathrm{Hom}_X\,(\mathcal{I}_Y,\mathcal{O}_Y)$.
**Proof.** WLOG, we can assume that $X=\mathrm{Spec}\,A$. Let $I=\Gamma(X,\mathcal{I}_Y)$. Then an infinitesimal deformation $Y'$ of $Y$ as a closed subscheme of $X$ corresponds to an ideal $I'\subset A\otimes_kD=:A'$ such that $I'A=I$ under the homomorphism $A'\rightarrow A$ given by $a\otimes b+ct\mapsto ba$, and $A'/I'$ is flat over $D$. We need to show that such an ideal $I'$ corresponds to an element of $\mathrm{Hom}_{A/I}\,(I/I^2,A/I)=\mathrm{Hom}_A\,(I,A/I)$.
By the lemma, $A'/I'$ is flat over $D$ if and only if $\forall x\in A'\;\;tx\in I'\implies x\in I'+tA'$. We can write $A'=A\oplus tA$, where the $D$-module structure of $A$ is given by the composition $D\rightarrow A'\rightarrow A$. Let $x=a+tb$ with $a,b\in A$, then $tx=ta$ and $x\in I'+tA'$ if and only if $a\in I'$. Since the composition $A\rightarrow A'\rightarrow A$ is identity, we see that $x\in I'+tA'$ if and only if $a\in I'A=I$. So the flat condition becomes $\{a\in A\,:\,ta\in I'\}\subset I$.
Now we construct $\varphi\in\mathrm{Hom}_A\,(I,A/I)$. For each $a\in I$, since $I'A=I$, there exists $b\in A$ such that $a+tb\in I'$. Set $\varphi(a)=\bar{b}$. For any $b'\in A$ such that $a+tb'\in I'$, we have $t(b-b')\in I'$. So $b-b'\in I$ and hence $\varphi$ is well-defined.
Conversely, suppose we're given $\varphi\in\mathrm{Hom}_A(I,A/I)$, we need to construct an ideal $I'\subset A'$ such that $I'A=I$ and $\{a\in A\,:\,ta\in I'\}\subset I$. Set $I'=\{a+tb\,:\,a\in I, \bar{b}=\varphi(a)\}$. For any $a+tb\in I'$ and $f+tg\in A'$, $(a+tb)(f+tg)=af+t(ag+bf)$. Since $af\in I$ and $\varphi(af)=f\varphi(a)=f\bar{b}$ and $fb\equiv ag+bf\pmod{I}$, we see that $I'$ is an ideal of $A'$. Obviously $I'A=I$. Besides, for any $a\in A$, if $ta\in I'$, then $\bar{a}=\varphi(0)=0$, i.e. $a\in I$.
Finally, it's easy to verify that two constructions are mutually inverse.$$\tag*{$\square$}$$
###### Infinitesimal deformation
(Hartshorne, Ex.III.9.8) For any scheme $X_0$ over a field $k$, an infinitesimal deformation of $X_0$ is a flat $D$-scheme $X$ whose closed fiber is $X_0$. We classify infinitesimal deformations of $X_0$ when $X_0=\mathrm{Spec}\,A$ is affine and of finite type over $k$.
Write $A$ as a quotient of a polynomial ring $P$ over $k$, and let $J$ be the kernel of $P\rightarrow A$. Consider the second exact sequence of differentials:$$J/J^2\longrightarrow\Omega_{P/k}\otimes_PA\longrightarrow\Omega_{A/k}\longrightarrow0.$$Apply the functors $\mathrm{Hom}_A\,(\cdot,A)$, and let $T^1(A)$ be the cokernel:$$0\longrightarrow\mathrm{Hom}_A\,(\Omega_{A/k},A)\longrightarrow\mathrm{Hom}_P\,(\Omega_{P/k},A)\longrightarrow\mathrm{Hom}_P\,(J,A)\longrightarrow T^1(A)\longrightarrow0.$$**Claim.** $T^1(A)$ classifies infinitesimal deformations of $\mathrm{Spec}\,A$.
The idea is to show that any infinitesimal deformation can be embedded into $\mathrm{Spec}\,P$ and rule out difference from the embedding. Suppose we're given a deformation $A'$ of $A$, we need to show that there's a surjective $D$-algebra homomorphism $P_D\rightarrow A'$. By definition, there's a surjective homomorphism $\pi:A'\rightarrow A'/tA'=A'\otimes_Dk=A$. Take arbitrary $D$-algebra homomorphism $g:P_D\rightarrow A'$ such that
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	P_D\arrow[r, "g"]\arrow[d]&A'\arrow[d, "\pi"]\\
	P\arrow[r, "\pi'"]&A

\end{tikzcd}
\end{document}
```
is commutative. (This homomorphism exists since $A'\rightarrow A$ is surjective.) Since $\pi'$ is surjective, we see that $g(P_D)+tA'=A'$. Then by Nakayama's lemma we see that $g(P_D)=A'$. So by the previous section, $(A',g)$ corresponds to an element of $\mathrm{Hom}_P\,(J,A)$.
Also, $(A',g)$ can be considered as a lifting problem of $D$-algebras
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	&0\arrow[d]\\
	&tA'\arrow[d]\\
	&A'\arrow[d, "\pi"]\\
	P_D\arrow[ru, dashed, "g"]\arrow[r]&A\arrow[d]\arrow[r]&0\\
	&0

\end{tikzcd}
\end{document}
```
So for a fixed $A'$, all $(A',g)$ have a $\mathrm{Hom}_{P_D}\,(\Omega_{P_D/D},tA')$-torsor structure. The first exact sequence of differentials for $k\rightarrow D\rightarrow P_D$ tells us that $\Omega_{P_D/D}=\mathrm{coker}\,(\Omega_{D/k}\otimes_DP_D\rightarrow\Omega_{P_D/k})$. Since $P_D=P\oplus tP$, we have $\Omega_{P_D/k}=\bigoplus_i P_D\,dx_i\oplus P_D\,dt$ and $\Omega_{D/k}\otimes_D P_D=P_D\,dt$. Therefore $\Omega_{P_D/D}=\bigoplus_iP_D\,dx_i=\Omega_{P/k}\otimes_PP_D$. So $\mathrm{Hom}_{P_D}\,(\Omega_{P_D/D},tA')=\mathrm{Hom}_{P_D}\,(\Omega_{P/k}\otimes_PP_D,tA')=\mathrm{Hom}_P\,(\Omega_{P/k},tA')$. The $P$-module of $tA'$ comes from its $A$-module structure and $\pi':P\rightarrow A$.
**Claim.** As $A$-modules, $tA'\cong A$. Applying the functor $-\otimes_DA'$, which is exact since $A'$ is $D$-flat, to the exact sequence of $D$-modules$$0\longrightarrow D/tD=k\overset{1\mapsto t}{\longrightarrow}D\longrightarrow k=D/tD\longrightarrow0,$$we get an exact sequence $$0\longrightarrow A'/tA'\overset{\varphi}{\longrightarrow} A'\longrightarrow A'/tA'\longrightarrow0.$$For any $x\in A'$, $\pi(x)\in A=A'/tA'=A'\otimes_Dk$ and $\varphi(\pi(x))=\varphi(a'\otimes 1)=ta'$. So $A\cong tA'$ as $D$-modules. For any $a\in A=A'/tA'$, choose arbitrary $a'\in A'$ such that $\pi(a')=a$, then $\varphi(a)=ta'$. So for any $b\in A$, choose arbitrary $b'\in A'$ such that $\pi(b')=b$, then $\varphi(ba)=tb'a'=b\cdot\varphi(a)$, where the multiplication of $\varphi(a)$ by $b$ comes from exactly the $A$-module structure of $tA'$. So we see that $A\cong tA'$ as $A$-modules as well.
Consequently, $\mathrm{Hom}_{P_D}(\Omega_{P_D/D},tA')=\mathrm{Hom}_P(\Omega_{P/k},A)$ and the result follows.
#### Rigidity And Deformations of $\mathbb{P}^1$.
(Hartshorne, Ex.III.9.10) A scheme $X_0$ over $k$ is *rigid* if it has no infinitesimal deformations. (TBD)
