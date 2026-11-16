#Algebraic-Geometry #Category-Theory
## 1. Cartesian Diagrams
Basic definition is omitted, here're some properties.
A. **Towers of cartesian diagrams are Cartesian diagrams** and therefore$$
Z\times_{X}X\times_SY=Z\times_SY.
$$Besides, given $X\rightarrow Y$, we have $X\times_YY=X$.
B. **The diagonal-base-change diagram.** Suppose we're given morphisms $X_1,X_2\rightarrow Y$ and $Y\rightarrow Z$, then
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	X_1\times_YX_2\ar[d]\ar[r]&X_1\times_ZX_2\ar[d]\\
	Y\ar[r,"\Delta"]&Y\times_ZY

\end{tikzcd}
\end{document}
```
is a Cartesian square. In particular, taking $X_1=X$, $X_2=Y$ and $Z=S$ as the base scheme, with morphisms $X\rightarrow Y\rightarrow S$, we have
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	X\ar[d,"f"]\ar[r,"\Gamma_f"]&X\times_SY\ar[d,"f\times 1"]\\
	Y\ar[r,"\Delta"]&Y\times_ZY

\end{tikzcd}
\end{document}
```
as a Cartesian square. See also Hartshorne, Ex. II.4.4.
C. **Preimage and intersection.** Given $X\rightarrow Y$ and $Z$ a locally closed subscheme of $Y$.
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	f^{-1}(Z)=Z\times_YX\ar[d]\ar[r]&Z\ar[d]\\
	X\ar[r]&Y

\end{tikzcd}
\end{document}
```
And as a special case of preimage, let $A$, $B$ be two locally closed subschemes of $X$, we have
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	A\cap B=A\times_XB\ar[d]\ar[r]&A\ar[d]\\
	B\ar[r]&X

\end{tikzcd}
\end{document}
```
Also, by diagonal base change
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	A\times_XB\ar[d]\ar[r]&A\times_SB\ar[d]\\
	X\ar[r,"\Delta"]&X\times_SX

\end{tikzcd}
\end{document}
```
we see that $A\cap B=\Delta_{X/S}^{-1}(A\times_SB)$.
D. There's an equivalence condition for monomorphisms, see [[About In,Surjectivity In Hartshorne]].
## 2. Limits And Colimits
A. **Limit/Inverse Limit/Projective Limit/$\displaystyle{\lim_{\longleftarrow}}$.** This constructs a "latest earlier" object with consistent arrows toward given objects, any other object with consistent arrows toward these factors through this particular object. A limit finds the commons, constrains, combine things together by looking for their commons, this feels restrictive. And in $\mathcal{Sets}$ limit is of the form$$
\big\{(a_i)_{i\in\mathscr{I}}\in\prod_{i}A_i:F(m)(a_j)=a_k,\,\forall m\in\text{Mor}_{\mathscr{I}}(j,k)\subset\text{Mor}(\mathscr{I})\big\}
$$Notice that in some old contexts, inverse limit refers to limit over a partially ordered index sets.
B. **Colimit/Direct Limit/Injective Limit/Inductive Limit/$\displaystyle{\lim_{\longrightarrow}}$.** This constructs an "earliest later" object, etc. A colimit identifies elements, patch things up according to their commons, it feels constructive. In $\mathcal{Sets}$, if $\mathscr{I}$ is filtered, colimit is of the form$$
\big\{(a_i)_{i\in\mathscr{I}}\in\coprod_{i}A_i\big\}\big/((a_i,i)\sim(a_j,j)\Leftrightarrow\exists f:A_i\rightarrow A_k,g:A_j\rightarrow A_k\,s.t.\,f(a_i)=g(a_j))
$$Notice that in some old contexts, direct limit refers to colimit over a partially ordered index set.
Also, in $\mathcal{Mod}_A$, even if $\mathscr{I}$ is not filtered, we still have the colimit equal to$$
\bigoplus_{i\in\mathscr{I}}M_i\big/(m_i-F(n)(m_i):\forall n:i\rightarrow j)
$$C. **Directed set/filtered set.** A nonempty partially ordered set $(S,\geq)$ is filtered if $\forall x,y\in S\exists z\in S\,s.t.\,x\geq z\text{ and }y\geq z$. More generally, a nonempty category $\mathscr{I}$ is filtered if:
1. $\forall x,y\in\mathscr{I}\,\exists z\in\mathscr{I}\text{ with arrows }x\rightarrow z, y\rightarrow z$, and
2. $\forall u:x\rightarrow y,v:x\rightarrow y\,\exists w:y\rightarrow z\,s.t.\,w\circ u=w\circ v$.
A summary from The Rising Sea: In a category where the objects are "set-like", an element of a limit can be thought of as a family of elements of each object in the diagram, that are "compatible". And an element of a a colimit can be thought of as ("has a representative that is") an element of a single object in the diagram.
D. (Atiyah, Ex. II.14-19) (Notice that there take $\leq$ as arrows.) Let $\mathscr{I}$ be a filtered set and $(M_i)_{i\in\mathscr{I}}$ a family of $A$-modules. Then every element of $\displaystyle{\lim_{\longrightarrow}}M_i$ can be written in the form $\mu_i(x_i)$ for some $i\in\mathscr{I},\,x\in M_i$ and $\forall i\in\mathscr{I},\,x_i\in M_i\,s.t.\,\mu_i(x_i)=0\quad\exists i\leq j\,\mu_{ij}(x_i)=0\in M_j$.
## 3. Adjoints
#### Basic Definitions
Given two category $\mathscr{A,B}$ and two covariant functors $F:\mathscr{A}\rightarrow\mathscr{B}$ and $G:\mathscr{B}\rightarrow\mathscr{A}$. We say that $F$ and $G$ are adjoint (in this order! denote $F\dashv G$) if there is a natural bijection for all $A\in\mathscr{A}$ and $B\in\mathscr{B}$ $$
\tau_{AB}:\text{Hom}_{\mathscr{B}}(F(A),B)\longrightarrow\text{Hom}_{\mathscr{A}}(A,G(B)).
$$For each $A$ there is a unique morphism $\eta_A:A\rightarrow GF(A)$ ($\eta_A=\tau_{AF(A)}(1_{F(A)})$), so that for any $g:F(A)\rightarrow B$, the corresponding $\tau_{AB}(g):A\rightarrow G(B)$ is given by the composition
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	A\ar[r,"\eta_A"]&GF(A)\ar[r,"Gg"]&G(B)

\end{tikzcd}
\end{document}
```
Similarly, for each $B$ there is a unique morphism $\epsilon_B:FG(B)\rightarrow B$ ($\epsilon_B=\tau_{G(B)B}^{-1}(1_{G(B)}))$, so that for each $f:A\rightarrow G(B)$, the corresponding map $\tau_{AB}^{-1}(f):F(A)\rightarrow B$ is given by the composition
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	F(A)\ar[r,"Ff"]&FG(B)\ar[r,"\epsilon_B"]&B

\end{tikzcd}
\end{document}
```
$\eta_A$ and $\epsilon_B$ are called unit and counit of the adjunction. Conversely, given natural transformations $\eta:id_{\mathscr{A}}\rightarrow GF$ and $\epsilon:FG\rightarrow id_{\mathscr{B}}$ with the property that $G\epsilon\circ\eta G=id_G$ and $\epsilon F\circ F\eta=id_F$, then $F$ and $G$ are adjoint.
Note that the right/left adjoint of a functor is unique if exists.
#### Key Properties
A. The idea of an adjunction is basically that we have a correspondence between certain things happening in $\mathscr{A}$ and things happening in $\mathscr{B}$.
B. **Adjunction, (co)limits and (left- and right-)exactness.**
1. Limits commute with limits and right adjoints. Colimits commute with colimits and left adjoints.
2. Kernels are limits, so both limits and right adjoints are left-exact. Cokernels are colimits, so both colimits and left adjoints are right-exact.
3. In $\mathcal{Mod}_A$, colimits over filtered index categories are exact. But limits over cofiltered index category may **NOT** be exact.
4. In $\mathcal{Mod}_A$, limits over surjective systems are exact. More precisely, if $$
0\rightarrow\{A_i\}\rightarrow\{B_i\}\rightarrow\{C_i\}\rightarrow0
$$is an exact sequence of inverse systems, such that $\{A_i\}$ is a surjective system, then the limit sequence is also exact.
**Remark.** Notice that by FHHF Theorem, (functors between (co)chain complex category induced by) exact functors commute with (co)homology functor.
#### Important Adjunctions
A. **Tensor-Hom Adjunction.** Given $N\in\mathcal{Mod}_A$, $\cdot\otimes_AN\dashv\text{Hom}_A(N,\cdot)$.
B. **Extension and Restriction of Scalars.** Given a ring homomorphism $A\rightarrow B$, between $\mathcal{Mod}_A$ and $\mathcal{Mod}_B$, $\cdot\otimes_AB\dashv\cdot_A$.
**Remark.** A forgetful functor, if appears in an adjunction, is often right adjoint to something constructive. This could be the general feeling for adjunctions.
C. **Localization and Its Forgetful Functor.** Given a ring $A$ and a multiplicative subset $S$, between $\mathcal{Mod}_A$ and $\mathcal{Mod}_{S^{-1}A}$, $S^{-1}\cdot\dashv F$.
D. **Sheafification and Its Forgetful Functor.** Given a topological space $X$, between the category of presheaves on $X$ and sheaves on $X$, denote the sheafification functor $\cdot^{sh}$, $\cdot^{sh}\dashv F$.
E. Given a continuous map $f:X\rightarrow Y$, between the category of sheaves over $Y$ and the sheaves over $X$, $f^{-1}\dashv f_*$. In particular, if $X$ is a point $y\in Y$, then $i^{-1}\mathcal{F}(X)=\mathcal{F}_y$. So we see that taking stalks and the constructing the skyscraper sheaf are an adjoint pair.
F. Given an open embedding $j:U\rightarrow X$, between the category of sheaves (of abelian groups or $\mathcal{O}$-modules) over $U$ and sheaves over $X$, $j_!\dashv j^{-1}$.
G. Given a morphism between schemes $f:X\rightarrow Y$, between $\mathcal{QCoh}_Y$ and $\mathcal{QCoh}_X$, $f^*\dashv f_*$.
H. Given a ring homomorphism $A\rightarrow B$, between $\mathcal{Mod}_B$ and $\mathcal{Mod}_A$, $\cdot_A\dashv\text{Hom}_A(B,\cdot)$.
I. Given a morphism between affine schemes $f:X\rightarrow Y$, between $\mathcal{QCoh}_X$ and $\mathcal{QCoh}_Y$, $f_*\dashv f^{!?}$.
## 4. Sheaves
#### Important Constructions
A. **Sheafification.** In categorical language, given a presheaf $\mathcal{F}$ over $X$, its sheafification $\mathcal{F}^{sh}$ is the unique sheaf over $X$ with a morphism $\mathcal{F}\rightarrow\mathcal{F}^{sh}$ such that given any sheaf $\mathcal{G}$ with a morphism $\mathcal{F}\rightarrow\mathcal{G}$, there exists a unique morphism $\mathcal{F}^{sh}\rightarrow\mathcal{G}$ such that the following diagram commutes:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	\mathcal{F}\ar[r]\ar[rd]&\mathcal{F}^{sh}\ar[d]\\
	&\mathcal{G}

\end{tikzcd}
\end{document}
```
Also, any presheaf $\mathcal{F}$ of sets (or groups, rings, etc.) has a sheafification. The idea is to define $\mathcal{F}^{sh}(U)$ as the set of "compatible" germs. (Cut things up and then patch them locally.) Here's an explicit construction:$$
\mathcal{F}^{sh}(U)=\{(f_x\in\mathcal{F}_x)_{x\in U}:\forall x\in U\,\exists\text{ an open nbhd }V\subset U\text{ of }x\text{ and }s\in\mathcal{F}(V)\,s.t.\,\forall y\in V\,s_y=f_y\}
$$Notice that sheafification preserves stalks.
B. **The Skyscraper Sheaf.** Let $P\in X$ and $i_P:P\rightarrow X$ the inclusion, $S$ is a set (or abelian groups or anything else), then $i_{P,*}S$ forms a sheaf. Notice that it is **NOT** the case that the only trivial stalk of a skyscraper sheaf is at $P$, unless $X$ is Hausdorff. But since we work with schemes, this is in general not the case! Actually, let $Z=\overline{P}$. Since open sets are stable under generalization, any point in $Z$ has stalk $S$ and any point not in $Z$ has stalk $0$ or $\varnothing$.
C. **Constant Presheaves and Constant Sheaves.** For any open set $U$, define $\underline{S}_{pre}(U)=S$. The sheafification of this presheaf is the constant sheaf associated to $S$, denote $\underline{S}$. Alternatively, $\underline{S}(U)$ is the set of locally constant maps $U\rightarrow S$. We have $\underline{S}_x=S$.
D. **Pushforward/Direct Image.** Given a continuous map $f:X\rightarrow Y$ and a sheaf $\mathcal{F}$ over $X$. The definition is well-known, no sheafification is needed. Given $x\in X$ and $y=f(x)$, there's a natural morphism of stalks $(f_*\mathcal{F})_y\rightarrow\mathcal{F}_x$, which is in general not an isomorphism. So to deal with stalks and $f_*$, just use the definition: germs are equivalent classes of the form $[s,U]$, where $U$ is an open nbhd of $y$ and $s\in\Gamma(f^{-1}(U),\mathcal{F})$. Also, denote $a_X:X\rightarrow\{\mathrm{pt}\}$, then $(a_X)_*=\Gamma(X,-)$.
**Proposition.** Pushforward of presheaves is commutative with sheafification.
**Proof.** Use the fact that pullback (no sheafification) and pushforward of presheaves are adjoint.$$\tag*{$\square$}$$This can simplify a lot of calculations.
E. **Pullback/Inverse Image.** Given a continuous map $f:X\rightarrow Y$ and a sheaf $\mathcal{F}$ over $Y$. $f^{-1}\mathcal{F}$ is defined to be the sheafification (!) of the presheaf $U\mapsto\underset{f(U)\subset V}{\text{colim}}\mathcal{F}(V)$. Given $y=f(x)$, we have a natural isomorphism $(f^{-1}\mathcal{F})_x=\mathcal{F}_y$, therefore $f^{-1}$ is an **exact** functor. See 3. of [[Simplify a direct system]] for a proof.
F. **Direct Image with Proper Supports** Given a continuous map $f:X\rightarrow Y$ between ==locally compact spaces== and a sheaf  over $X$. For any open $U\subset Y$, $\Gamma(U;f_!\mathcal{F})=\{s\in\Gamma(f^{-1}(U);\mathcal{F})\,:\,f:\mathrm{supp}\,s\rightarrow U\text{ is proper}\}$. If $X$ and $Y$ are locally compact, then we have a canonical isomorphism$$(f_!\mathcal{F})_y\longrightarrow\Gamma_c(f^{-1}(y),\mathcal{F}\bigr|_{f^{-1}(y)})
$$Recall that when $X$ and  $Y$ are locally compact, $f$ is proper if and only if every inverse image of compact subsets of $Y$ are compact and properness is local on $Y$. $f_!$ is always left exact. Also, for locally closed embeddings, $f_!\mathcal{F}$ is the sheafification of $$
U\mapsto\begin{cases}
\mathcal{F}(U\cap\overline{X}),&U\cap\overline{X}\subset X;\\
0,&\text{otherwise.}
\end{cases}
$$In this case, given $y$, we have$$(f_!\mathcal{F})_y=\begin{cases}
\mathcal{F}_x,&y=f(x);\\
0,&y\notin X.
\end{cases}
$$(So, this is also called "extension by 0"). Also in this case, $f_!$ is exact and $f_!\dashv f^{-1}\circ\Gamma_X$.
In particular, when $f$ is proper (e.g. closed embedding), $f_*=f_!$. When $f$ is an open embedding, this is the sheafification of$$
U\mapsto\begin{cases}
\mathcal{F}(U),&U\subset X;\\
0,&\text{otherwise.}
\end{cases}
$$We have $(a_X)_!=\Gamma_c(X,-)$. And finally, given an open subset $U\subset X$ with inclusion $j$, denote $Z=X-U$ with inclusion $i$, we have a short exact sequence$$
0\longrightarrow j_!(\mathcal{F}\bigr|_U)\longrightarrow\mathcal{F}\longrightarrow i_*(\mathcal{F}\bigr|_Z)\longrightarrow0
$$G. **Sheaves with Support on X.** Given a locally closed subset $X$ of $Y$, there's a functor $\Gamma_X:\mathcal{Sh}(Y)\rightarrow\mathcal{Sh}(Y)$. Take $X\subset V\subset Y$, such that $X$ is closed in $V$ and $V$ is open in $Y$, define$$\Gamma_X(V,\mathcal{F}):=\ker(\Gamma(V,\mathcal{F})\longrightarrow\Gamma(V-X,\mathcal{F}))$$and verify that this is independent of $V$. So for any open $U\subset Y$ we define$$\Gamma(U,\Gamma_X\mathcal{F}):=\Gamma_{U\cap X}(U,\mathcal{F}\bigr|_U)
$$(Sections with support contained in $X$.)
In particular, if $X$ is closed, then$$\Gamma(U,\Gamma_X\mathcal{F})=\{s\in\Gamma(U,\mathcal{F}):\mathrm{supp}\,s\subset U\cap X\}$$and setting $Z=X$, $\mathcal{H}_Z^0(\mathcal{F})=\Gamma_Z(\mathcal{F})$, $U=Y-Z$ with inclusion $j$, we have a short exact sequence$$0\longrightarrow\mathcal{H_Z^0(\mathcal{F})}\longrightarrow\mathcal{F}\longrightarrow j_*(\mathcal{F}\bigr|_U)$$where the last map is surjective if $\mathcal{F}$ is flasque. If $X$ is open, then $\Gamma_X=j_*\circ j^{-1}$, where $j$ is the inclusion.
See also [[Summary on QCoh Subsheaves with Support]]
H. **Kernel, Cokernel and Image.** Kernel is the presheaf kernel but cokernel and image needs sheafification! See two propositions below. Notice that (for sheaves taking value in "fine" abelian category) taking kernel, cokernel (inparticular, taking quotient) or image commutes with taking stalks. This is because taking stalks is essentially a colimit over a filtered set, so it's exact. Actually we'll see below that **taking stalks is faithfully exact**.
I. **Sheaf Hom.** Suppose $\mathcal{F}$ and $\mathcal{G}$ are two sheaves over $X$. Define $\mathcal{Hom}\,(\mathcal{F},\mathcal{G})(U)=\text{Hom}\,(\mathcal{F}{\bigr|}_U,\mathcal{G}{\bigr|}_U)$. Notice that $\mathcal{Hom}$ does **NOT** commute with taking stalks! In general we only have a map $\mathcal{Hom}\,(\mathcal{F},\mathcal{G})_x\rightarrow\text{Hom}\,(\mathcal{F}_x,\mathcal{G}_x)$ which may not be bijective. However, if $X$ is a noetherian scheme and $\mathcal{F},\mathcal{G}$ are coherent, then localization does commute with $\mathcal{Hom}$.
Let $\mathcal{F}$ be an $\mathcal{O}_X$-module, we call $\mathcal{Hom}\,(\mathcal{F},\mathcal{O}_X)$ its dual, denote it $\mathcal{F}^{\vee}$.
See [Lemma 17.22.4 on Stacks Project](https://stacks.math.columbia.edu/tag/01CM) for the conditions needed for taking stalks to commute with $\mathcal{Hom}$.
J. **The Extraordinary Inverse Image**. Assume that $f_!$ has finite cohomological dimension, i.e. $\exists d\geq0\,\forall\mathcal{F}\in Sh(X)\,\forall k>d\;R^kf_!\mathcal{F}=0$. (This always holds if $f$ is a algebraic map between varieties.) Then $Rf_!$ admits a right adjoint $f^!:D^+(Y)\rightarrow D^+(X)$.
#### Properties Determined at the Level of Stalks
**Proposition.** Let $\varphi:\mathcal{F}\rightarrow\mathcal{G}$ be a morphism between sheaves over $X$. TFAE
1. $\varphi$ is injective, i.e. $\text{ker}\,\varphi=0$
2. $\varphi$ is a monomorphism in the category of sheaves over $X$
3. $\forall x\in X\,\,\varphi_x$ is injective
4. $\forall\text{open }U\subset X\,\,\varphi(U)$ is injective

**Proposition.** Let $\varphi:\mathcal{F}\rightarrow\mathcal{G}$ be a morphism between sheaves over $X$. TFAE
1. $\varphi$ is surjective, i.e. $\text{im}\,\varphi=\mathcal{G}$, or equivalently, $\text{coker}\,\varphi=0$
2. $\varphi$ is an epimorphism in the category of sheaves over $X$
3. $\forall x\in X\,\,\varphi_x$ is surjective
See item 2. of [[(Counter)examples in Algebraic Geometry]].
So taking sections over $U$ is a left functor, but in general it's not right exact. However here're some exceptional cases. (Another quick proof of this is that taking sections is exact in the category of sheaves of abelian groups, and the forgetful functor is right adjoint to the sheafification functor, so it's left exact.)
#### Sheaves and Morphisms Can Be Constructed on a Base
TBD
#### The Push-Pull Map
Suppose
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	W\ar[r,"\beta'"]\ar[d,"\alpha'"]&X\ar[d,"\alpha"]\\
	Y\ar[r,"\beta"]&Z

\end{tikzcd}
\end{document}
```
is a commutative (not necessarily Cartesian!) diagram, and $\mathcal{F}$ is a sheaf on $X$. Define the push-pull map$$
\beta^{-1}\alpha_*\mathcal{F}\longrightarrow\alpha_*'(\beta')^{-1}\mathcal{F}
$$of sheaves on $Y$ as follows. Start with the identity $(\beta')^{-1}\mathcal{F}\xrightarrow{\sim}(\beta')^{-1}\mathcal{F}$ on $W$. By adjointness of $((\beta')^{-1},\beta'_*)$, this is the same as the data of a morphism $\mathcal{F}\rightarrow(\beta_*')(\beta')^{-1}\mathcal{F}$ on $X$. Apply $\alpha_*$ to get a map $\alpha_*\mathcal{F}\rightarrow\alpha_*(\beta_*')(\beta')^{-1}\mathcal{F}$ on $Z$. By the commutative diagram, this is the map $\alpha_*\mathcal{F}\rightarrow\beta_*(\alpha_*')(\beta')^{-1}\mathcal{F}$ on $Z$. By adjointness of  $(\beta^{-1},\beta_*)$, this yields the desired map.
Observe that this entire construction is functional in $\mathcal{F}$. Besides, we could have defined it in a dual way starting with the identity $\alpha_*\mathcal{F}\rightarrow\alpha_*\mathcal{F}$ on $Z$.
