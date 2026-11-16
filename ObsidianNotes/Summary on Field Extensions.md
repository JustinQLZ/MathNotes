#Algebra #Commutative-Algebra 
Most content are from GTM73.
### 1. Basic Results
#### 1.1 Extension by One Element
Also called simple extensions. Recall basic definitions: transcendental/algebraic element/extension and index.
Basic facts:
1. Multiplication rule of indexes of extension towers. In particular, prime index implies that there's no intermediate extension.
2. If $u$ is algebraic over $K$, then
	1. $K[u]=K(u)$
	2. $\exists!$ minimal polynomial $f$
	3. $K[u]\cong K[x]/(f)$
	4. $[K[u]:K]=\mathrm{deg}\,f$ with a basis $\{1,u,u^2,\dots,u^{\mathrm{deg}\,f-1}\}$
3. If $u$ is transcendental over $K$, then $K(u)\cong K(x)$

Next we extend field isomorphisms:
**Theorem.** Let $\sigma:K\rightarrow L$ be an isomorphism of fields, $u$ in some extension of $K$ and $v$ in some extension of $L$. Assume either
1. $u$ and $v$ are transcendental over $K$ and $L$ resp.; or
2. let $f$ be the minimal polynomial of $u$, then $\sigma\,f(v)=0$.
Then $\sigma$ extends to $K(u)\cong L(v)$, sending $u$ to $v$.
**Corollary.** $E/K$ and $F/K$, $u\in E$ and $v\in F$ are algebraic over $K$. Then the minimal polynomials of $u$ and $v$ are identical if and only if $\exists\,K[u]\cong K[v]$ which sends $u$ to $v$ and fixes $K$.

We can also view an extension by an algebraic element as adding a root of an irreducible polynomial:
**Theorem.** $f\in K[x]$, $\mathrm{deg}\,f=n$. Then there exists a simple extension field $F=K(u)$ such that
1. $u\in F$ is a root of $f$;
2. $[K(u):K]\leq n$, with equality holding if and only if $f$ is irreducible in $K[x]$;
3. if $f$ is irreducible in $K[x]$, then $K(u)$ is unique up to an isomorphism which fixes $K$.
#### 1.2 First Filtrations of Extensions: finitely generated, finite and algebraic.
1. $F/K$, such that $[F:K]<\infty$, then $F$ is finitely generated and algebraic over $K$.
2. $F/K$, $X\subset F$ such that $F=K(X)$ and $X$ is algebraic over $K$, then $F$ is an algebraic extension of $K$. Furthermore, if $\#X<\infty$, then $[F:K]<\infty$.
3. $F/E$ algebraic and $E/K$ algebraic, then $F/K$ algebraic.
4. $F/K$, then $E:=\{u\in F\,:\,u\text{ is algebraic over }K\}$ is a field. In particular, $E$ is closed under operations.
Combining 1&2 we see that $[F:K]<\infty$ if and only if $F$ is finitely generated and algebraic over $K$.

#### 1.3 Some Other Results
1. $u$ is algebraic of odd degree over $K$, then so is $u^2$ and $K(u)=K(u^2)$. (Useful for calculations!)
2. If $u,v$ are algebraic over $K$ of degrees $m$ and $n$ resp., then $[K(u,v):K]\leq mn$. If $(m,n)=1$, then $[K(u,v):K]=mn$.
3. Let $L$ and $M$ be intermediate fields of $F/K$.
	1. $[LM:K]$ is finite if and only if $[L:K]$ and $[M:K]$ are finite.
	2. If $[LM:K]$ is finite, then $[L:K]$ and $[M:K]$ divide $[LM:K]$ and $[LM:K]\leq[L:K][M:K]$.
	3. If $[L:K]$ and $[M:K]$ are finite and relatively prime, then $[LM:K]=[L:K][M:K]$.
	4. If $L$ and $M$ are algebraic over $K$, the so is $LM$.
### 2. Galois Theory
#### 2.1 Basics and the Statement of the Fundamental Theorem
We use the notation $Gal(F/K)$ for the Galois group of $F/K$.
1. $F/K$, $f\in K[x]$ and $u\in F$. If $f(u)=0$, then for all $\sigma\in Gal(F/K)$, $f(\sigma u)=0$, since $\sigma f(u)=f(\sigma u)$.
2. $F/K$, $E$ an intermediate field and $H<Gal(F/K)=G$, then
	1. $H':=\{v\in F\,:\,\forall\sigma\in H\;\;\sigma v=v\}$ is an intermediate field
	2. $E':=\{\sigma\in Gal(F/K)\,:\,\forall u\in E\;\;\sigma u=u\}=Gal(F/E)$ is a subgroup of $Gal(F/K)$.
	3. $F'=1$, $K'=G$ and $1'=F$ are automatic. However it's possible to have $G'\neq K$. *Galois Theory basically says that once this failure is fixed, then two worlds are equivalent under the "prime" operation.* If $Gal(F/K)'=K$, i.e. $K''=K$, then $F/K$ is said to be Galois.
	4. $F$ is Galois over $K$ if and only if $\forall u\in F-K\,\exists\sigma\in Gal(F/K)\;\;\sigma(u)\neq u$. Let $K_0=K''$, then $K_0/K$, $F/K_0$ is Galois and $Gal(F/K_0)=Gal(F/K)$.

**Theorem. (Fundamental Theorem of Galois Theory)** $F/K$ Galois and $[F:K]<\infty$, then there is a one-to-one correspondence between the set of all intermediate fields of the extension and the set of all subgroups of the Galois group $Gal(F/K)$ (given by $E\mapsto E'$) such that:
1. For any two intermediate fields $L\subset M$, $[M:L]=[L':M']$. In particular, $\#Gal(F/K)=[F:K]$.
2. $F$ is Galois over every intermediate field $E$, but $E$ is Galois over $K$ if and only if $E'=Gal(F/E)\lhd Gal(F/K)=G$; in this case $G/E'=Gal(F/K)/Gal(F/E)\cong Gal(E/K)$.

Next we develop the theory for general cases:
**Proposition.** $F/K$, with intermediate fields $L$ and $M$, subgroups $H,J<G=Gal(F/K)$. Then
1. $F'=1$ and $K'=G$
2. $1'=F$
3. $L\subset M\implies M'<L'$
4. $H<J\implies J'\subset H'$
5. $L\subset L''$ and $H<H''$
6. $L'=L'''$ and $H'=H'''$
**Theorem.** $F/K$, then there is a one-to-one correspondence between the closed (i.e. $E''=E$) intermediate fields and the closed subgroups, given by $E\mapsto E'$.

**Lemma.** $F/K$ and $L\subset M$ intermediate fields. If $[M:L]<\infty$, then $[L':M']\leq [M:L]$. In particular, if $[F:K]<\infty$, then $\#Gal(F/K)\leq[F:K]$.
>[!proof]-
>The proof from GTM73 is by induction on $[M:L]$. By introducing a simple intermediate extension, we reduce to the case $M=L(u)$. Then we can construct an injective map from the set of all left cosets of $M'$ in $L'$ to the set of all distinct roots (in $F$) of the minimal polynomial of $u$. The construction is quite natural.

**Lemma.** $F/K$ and $H<J<Gal(F/K)$. If $[J:H]<\infty$, then $[H':J']\leq [J:H]$.

>[!proof]-
>Despite the natural proof of the previous lemma, GTM73's proof for this one is very tricky. The idea is originated from the representation theory. For any $n+1$ elements in $H'$, we want to find scalars in $J'$ annihilating them. **So we start from the larger field $H'$, where solutions trivially exist.** But we need them to lie in $J'$, i.e. fixed by elements in $J$. Suppose the desired solution is $x_j$, then for all $\sigma \in J$, we have $\sigma x_j=x_j$, and we obtain $\sum_j\sigma(u_j)x_j=0$ naturally. So we start from these linear equations instead. We choose $n$ representatives, denoted $\tau_i$, of the left cosets of $H$ in $J$. Since elements are in $H'$, the equations for all $\sigma$ are equivalent to $\sum_j\tau_i(u_j)x_j=0$ for $1\leq i\leq n$. Such a solution always exists by linear algebra!
Now we need to show that we can actually find a solution lying in $J'$. (This tastes like: **we have a system satisfying apparent restrictions, i.e. symmetry, we want to show that we have a realistic solution for the system. Here by "realistic", I mean that the solution lies in $J'$, so the symmetry of the system, here, $J$-invariance, is satisfied in an apparent way.**)
Suppose all nonzero solutions do *not* lie in $H'$, then for any solution, there exists $\sigma\in J$ such that, for some $j_0$, $\sigma x_{j_0}\neq x_{j_0}$. Here we **normalize** the solution so that $x_1=1$, *which utilizes the nonzero condition*. But the system is $J$-invariant, so $\sigma x_j$ is also a solution. Then $\sigma x_j-x_j$ is also a nonzero solution for the system, with slot $j=1$ equal zero, alternatively, it has less nonzero terms! Repeat the process, we can find a solution with $x_1=1$ and $x_j=0$ for all $j\geq 2$. But this would then imply that $u_1=0$, which is a contradiction!
If we insist on a completely constructive and more intuitive proof, we can argue as followings. Start from arbitrary solution $x_j$. Notice that the $J$-invariance of the system results in a whole family of solutions, namely $\sigma(x_j)$. Again, we can choose $n$ representatives, which are all possibly distinct solutions in the family, namely $\tau_i(x_j)$. We need to invent a process to construct another solution out of $x_j$ such that all $\tau_i(x_j)$ with distinct $i$ are identical. Naturally, we induct on the $H'$-rank of these $n$ vectors. A key observation is that there're **two possible operations** we can apply: replace $x_j$ by $J'$-linear combinations of $\tau_i(x_j)$, and multiply $x_j$ by some nonzero $a\in H'$. The second operation results in the family $\tau_i(a)\tau_i(x_j)$. Naturally, since the solution is nonzero, we can assume that the first row are all 1, i.e. normalize the solution so that $x_1=1$. Then by linear combination, if the $H'$-rank is bigger than 1, we can always replace $x_j$ with another vector with less nonzero terms. Since the row rank is identical with the column rank, eventually we obtain the desired solution.

**Lemma.** $F/K$, $L\subset M$ are intermediate fields, $H<J<Gal(F/K)$.
1. If $L$ is closed (i.e. $L''=L$) and $[M:L]<\infty$, then $M$ is closed and $[L':M']=[M:L]$.
2. If $H$ is closed and $[J:H]<\infty$, then $J$ is closed and $[H':J']=[J:H]$. In particular, every finite subgroup of $Gal(F/K)$ is closed, since $1''=1$.
3. If $F$ is a finite Galois extension of $K$, then all intermediate fields and all subgroups of $Gal(F/K)$ are closed and $\#Gal(F/K)=[F:K]$.
Now we have established the first part of the fundamental theorem.
If $E$ is an intermediate field of $F/K$, then $E$ is said to be **stable** (relative to $F/K$), if $\forall \sigma\in Gal(F/K)\;\;\sigma(E)\subset E$. Notice that if $\sigma(E)\subset E$, then $\sigma^{-1}(E)\subset E$ and $\sigma|_E\in Gal(E/K)$. It will turn out that in the finite case $E$ is stable if and only if $E$ is Galois over $K$.

**Lemma.** $F/K$.
1. If $E$ is stable, then $E'\lhd Gal(F/K)$.
2. If $H\lhd Gal(F/K)$, then $H'$ is stable.
**Lemma.** $F/K$ Galois and $E$ is stable, then $E/K$ is Galois.
**Lemma.** $F/K$ and $E$ is an intermediate field. If $E/K$ is algebraic and Galois, then $E$ is stable.
>[!proof]-
>If $u\in E$ with minimal polynomial $f\in K[x]$, let $u_1=u,u_2,\dots,u_r$ be the *distinct* roots of $f$ that lie in $E$. Then $r\leq n=\mathrm{deg}\,f$. If $\tau\in Gal(E/K)$, then $\tau$ permutes the $u_i$. Therefore $g(x)=\prod_i(x-u_i)$ is fixed by every $\tau\in Gal(E/K)$. Since $E/K$ is Galois, we have $g\in K[x]$. **(This implication itself is very useful: for an algebraic Galois extension, the elementary polynomials of the roots lie in the base field!)** Now $u$ is a root of $g$ and hence $f\mid g$. Consequently, we must have $f=g$. Consequently, **for an algebraic and Galois extension, all roots of $f$ are distinct and lie in $E$!** (We will use this result later in section 2.2.) Now if $\sigma\in Gal(F/K)$, then $\sigma(u)$ is a root of $f$, whence $\sigma(u)\in E$. Therefore, $E$ is stable.

Let $E$ be an intermediate field of the extension $F/K$, then $\sigma\in Gal(E/K)$ is said to be **extendible** to $F$ is there exists $\sigma\in Gal(F/K)$ such that $\sigma|_E=\tau$. Recall that if $E$ is stable, then $E'\lhd Gal(F/K)$, and consequently, $Gal(F/K)/Gal(F/E)$ is defined.
**Lemma.** $F/K$ and $E$ is a stable intermediate field. Then $Gal(F/K)/Gal(F/E)\cong \{\sigma\in Gal(E/K)\,:\,\sigma\text{ is extendible to }F\}<Gal(E/K)$.
Now the second part of the fundamental theorem follows.
>[!summary]
>Notice that all except the second lemma are natural till now. First we study the simplest extensions, which are directly named as simple extensions. Then come up with the idea of fixing fields and groups. Next, start to think about what happens ones the failure is fixed, which lead to the key and natural definition of a Galois extension. Prove basic facts about the prime notation. Analyze into indexes, starting from inequities. The first lemma is easy and the second one is tricky. But the statement is completely natural, considering the first one. Then, with the basics developed, the first part of the fundamental theorem follows quite easily. For the second part, we introduce the concepts of stable and extendible. And with them as bridges, we establish the second part of the fundamental theorem. Remaining problems are to establish criterions for Galois extensions.

This section ends with a theorem of Artin. Artin's point of view is that the basic object is a given field $F$ together with a (finite) group $G$ of automorphisms of $F$. One then constructs the subfield $K$ of $F$ as the fixed field of $G$.
**Theorem.** Let $F$ be a field, $G$ a group of automorphisms of $F$ and $K$ the fixed field (which is a field) of $G$ in $F$. Then $F/K$ is Galois. If $G$ is finite, then $F/K$ is a finite Galois extension with $Gal(F/K)=G$.
#### 2.2 Appendix: Symmetric Rational Functions
Recall the definition of symmetric rational functions which form a field $E$ an elementary symmetric functions $f_1,\dots,f_n$.
Also recall that we can view $S_n$ as a subgroup of $Gal(K(x_1,\dots,x_n)/K)$ and clearly the fixed field of $S_n$ consists precisely of the symmetric functions. Therefore, by Artin's theorem above, $K(x_1,\dots,x_n)/E$ is a Galois extension with Galois group $S_n$ and dimension $n!$. Besides, since any finite group is a subgroup of $S_n$, we have:
**Proposition.** If $G$ is a finite group, then there exists a Galois field extension with Galois group isomorphic to $G$.
We have a tower of fields:$$K\subset K(f_1,\dots,f_n)\subset E\subset K(x_1,\dots,x_n).$$We will show that $E=K(f_1,\dots,f_n)$, i.e. every rational symmetric function is in fact a rational function of the elementary symmetric functions over $K$.
**Lemma.** For any integer $1\leq k\leq n-1$, if $h_1,\dots,h_k\in K[x_1,\dots,x_n]$ are the elementary symmetric functions in $x_1,\dots,x_k$, then each $h_j$ can be written as a polynomial over $K$ in $f_1,\dots,f_n$ and $x_{k+1},\dots,x_n$.
>[!proof]-
>The theorem is true when $k=n-1$ since in that case $h_1=f_1-x_n$ and $h_j=f_j-h_{j-1}x_n (2\leq j\leq n)$. Then the proof follows easily by descending induction on $k$ with the same constructions.

**Theorem.** $E=K(f_1,\dots,f_n)$.
>[!proof]-
>Since $[K(x_1,\dots,x_n):E]=n!$ and $K(f_1,\dots,f_n)\subset E\subset K(x_1,\dots,x_n)$, it suffices to show that $[K(x_1,\dots,x_n):K(f_1,\dots,f_n)]\leq n!$. Let $F=K(f_1,\dots,f_n)$ and consider the tower:$$F\subset F(x_n)\subset F(x_{n-1},x_n)\subset\cdots\subset F(x_1,\dots,x_n)=K(x_1,\dots,x_n).$$It then suffices to show that $x_n$ is algebraic over $F$ of degree $\leq n$ and for each $k<n$, $x_k$ is algebraic of degree $\leq k$ over $F(x_{k+1},\dots,x_n)$.
>To do this, let $g_n(y)\in F[y]$ be the polynomial $g_n(y)=\prod_i(y-x_i)=y^n-f_1y^{n-1}+\cdots+(-1)^nf_n$. Since $g_n\in F[y]$ has degree $n$ and $x_n$ is a root of $g_n$, $x_n$ is algebraic of degree at most $n$ over $F=K(f_1,\dots,f_n)$. Now for each $k\;(1\leq k\leq n)$ define a monic polynomial $g_k(y)=g_n(y)/\prod_{i=k+1}^n=\prod_{i=1}^k(y-x_i)$. Clearly each $g_k(y)$ has degree $k$, $x_k$ is a root of $g_k(y)$ and the coefficients of $g_k(y)$ are precisely the elementary symmetric functions in $x_1,\dots,x_k$. By the previous lemma, $g_k(y)\in F(x_1,\dots,x_n)[y]$, whence $x_k$ is algebraic of degree at most $k$ over $F(x_{k+1},\dots,x_n)$.

Next we prove an analogue for symmetric polynomials, namely: every symmetric polynomial in $x_1,\dots,x_n$ over $K$ is in fact a polynomial in the elementary symmetric functions $f_1,\dots,f_n$ over $K$. In other words, every symmetric polynomial in $K[x_1,\dots,x_n]$ lies in $K[f_1,\dots,f_n]$.
**Lemma.** $X=\{x_1^{i_1}\cdots x_n^{i_n}\,:\,\forall k\;0\leq i_k< k\}$ is a basis of $K(x_1,\dots,x_n)$ over $E$.
>[!proof]-
>Since $\#X=n!$, it suffices to show that $X$ spans $K(x_1,\dots,x_n)$. Consider the tower$$E\subset E(x_n)\subset E(x_{n-1},x_n)\subset\cdots\subset E(x_1,\dots,x_n)=K(x_1,\dots,x_n).$$Since $x_n$ is algebraic of degree $\leq n$ over $E$ by the previous proof, $\{x_n^j,:\,0\leq j<n\}$ spans $E(x_n)$ over $E$. For same reasons, $\{x_{n-1}^i\,:\,0\leq i<n-1\}$ spans $E(x_{n-1},x_n)$ over $E(x_n)$. Therefore $\{x_{n-1}x_n^j\,:\,0\leq i<n-1;0\leq j<n\}$ spans $E(x_{n-1},x_n)$ over $E$. The rest steps are completed by similar arguments.

**Proposition.** Let $f_1,\dots,f_n$ be the elementary symmetric functions in $K(x_1,\dots,x_n)$.
1. Every polynomial in $K[x_1,\dots,x_n]$ can be written uniquely as a linear combination of the $n!$ elements $x_1^{i_1}\cdots x_n^{i_n}\;(\forall k\;0\leq i_k<k)$.
2. Every symmetric polynomial in $K[x_1,\dots,x_n]$ lies in $K[f_1,\dots,f_n]$.
>[!proof]-
>Let $g_k(y)$ be as in the proof of the previous theorem. As noted there, the coefficients of $g_k(y)$ are polynomials over $K$ in $f_1,\dots,f_n$ and $x_{k+1},\dots,x_n$. Since $g_k$ is monic of degree $k$ and $g_k(x_k)=0$, $x_k^k$ can be expressed as a polynomial over $K$ in $f_1,\dots,f_n,x_{k+1},\dots,x_n$ and $x_k^i\;(i\leq k-1)$. If we proceed step by step beginning with $k=1$ and substitute this expression for $x_k^k$ in a polynomial $h\in K[x_1,\dots,x_n]$, the result is a polynomial in $f_1,\dots,f_n,x_1,\dots,x_n$ in which the highest exponent of any $x_k$ is $k-1$. In other words, $h$ is a linear combination of the $n!$ elements $x_1^{i_1}\dots x_n^{i_n}\;(\forall k\;i_k<k)$ with coefficients in $K[f_1,\dots,f_n]$. Furthermore, these coefficient polynomials are uniquely determined since $\{x_1^{i_1}\cdots x_n^{i_n}\,:\,\forall k\;0\leq i_k<k\}$ is linearly independent over $E=K(f_1,\dots,f_n)$. This proves 1 and also implies that if a polynomial $h\in K[x_1,\dots,x_n]$ is a linear combination of $x_1^{i_1}\cdots x_n^{i_n}\;(i_k<k)$ with coefficients in $K(f_1,\dots,f_n)$, then the coefficients are in fact polynomials in $K[f_1,\dots,f_n]$. In particular, if $h$ is a symmetric polynomial (that is, $h\in E)$, then $h$ necessarily lies in $K[f_1,\dots,f_n]$. This proves 2.

#### 2.3 Some Other Results
1. $f/g\in K(x)-K$ and $f,g$ relatively prime in $K[x]$.
	1. $x$ is algebraic over $K(f/g)$ and $[K(x):K(f/g)]=\mathrm{max}\,(\mathrm{deg}\,f,\mathrm{deg}\,g)$, since the minimal polynomial of $x$ over $K(f/g)$ is (up to a $K$ multiple) $(f/g)g(y)-f(y)\in K(f/g)[y]$.
	2. If $E\neq K$ is an intermediate field, then $[K(x):E]$ is finite.
	3. The assignment $x\mapsto f/g$ induces a homomorphism $\sigma:K(x)\rightarrow K(x)$ such that $\varphi(x)/\psi(x)\mapsto \varphi(f/g)/\psi(f/g)$. $\sigma\in Gal(K(x)/K)$ if and only if $\mathrm{max}\,(\mathrm{deg}\,f,\mathrm{deg}\,g)=1$.
	4. $Gal(K(x)/K)$ consists of all automorphisms induced (as in 3.) b the assignment$$x\mapsto \frac{ax+b}{cx+d}$$where $a,b,c,d\in K$ and $ad-bc\neq0$.
	5. $K(x)/K$ is Galois if and only if $K$ is a infinite field. And if $K$ is an infinite field, the only closed subgroups of $Gal(K(x)/K)$ are itself and its finite subgroups.
2. $K\subset E\subset F$. If $E/K$ and $F/E$ are Galois, and every $\sigma\in Gal(E/K)$ is extendible to $F$, then $F/K$ is Galois.
3. Let $F/K$ be a finite Galois extension and let $L$ and $M$ be two intermediate fields.
	1. $Gal(F/LM)=Gal(F/L)\cap Gal(F/M)$
	2. $Gal(F/(L\cap M))=Gal(F/L)\vee Gal(F/M)$
	3. If $Gal(F/L)\cap Gal(F/M)=1$, then $F=LM$.
4. $F/K$ is a finite Galois extension and $E$ is an intermediate field, then there is a unique smallest field $L$ such that $E\subset L\subset F$ and $L/K$ is Galois. Furthermore,$$Gal(F/L)=\bigcap_{\sigma\in Gal(F/K)}\sigma Gal(F/E)\sigma^{-1}.$$
### 3. Criterion for Galois Extensions
#### 3.1 Splitting Fields and Algebraic Closure
Recall the definition of a polynomial being split and the definition of a splitting field of a polynomial (i.e. field extension by adding all roots of a polynomial, or strictly speaking, a field in which the polynomial splits and that the extension is generated by the roots), also the splitting field of a set of polynomials. Notice that although we use the term "the", it's will only become clear later that a splitting field is unique up to isomorphisms fixing the base field.
Notice that for any set of polynomials $S\subset K[x]$, its splitting field $F$ is algebraic over $K$ and finite if $\#S<\infty$, and in the latter case, say $S=\{f_1,\dots,f_n\}$, the splitting field of $S$ coincides with the splitting of $f=f_1\cdots f_n$.
By induction on degrees and adding roots one at a time, we can prove the following theorem easily:
**Theorem.** $f\in K[x]$ has degree $n\geq 1$, then there exists a splitting field $F$ of $f$ with $[F:K]\leq n!$.
**Theorem.** The following conditions on a field $F$ are equivalent, and such a field is said to be **algebraically closed**.
1. Every nonconstant polynomial $f\in F[x]$ has a root in $F$.
2. Ever nonconstant polynomial $f\in F[x]$ splits over $F$.
3. Every irreducible polynomial in $F[x]$ has degree one.
4. There is no algebraic extension field of $F$ (except $F$ itself).
5. There exists a subfield $K$ of $F$ such that $F$ is algebraic over $K$ and very polynomial in $K[x]$ splits in $F[x]$.

**Theorem.** $F/K$. Then TFAE. And such an $F$ is called the algebraic closure of $K$.
1. $F/K$ is algebraic and $F$ is algebraically closed.
2. $F$ is a splitting field over $K$ of the set of all (irreducible) polynomials in $K[x]$.
Clearly the existence of arbitrary splitting fields over a field $K$ is equivalent to the existence of an algebraic closure of $K$. Proving the existence of a splitting field of an infinite set of polynomials uses the axiom of choice and is considerably more difficult. The main difficulty is set-theoretic rather than algebraic (the *class* of all algebraic extension fields of $K$ need *not* be a set) and relevant proofs are omitted here.
**Lemma.** If $F/K$ is algebraic, then $\#F\leq\aleph_0\cdot\#K$.
**Theorem.** Every field $K$ has an algebraic closure and any two algebraic closures of $K$ are $K$-isomorphic.
**Corollary.** $S\subset K[x]$, then a splitting field of $S$ over $K$ exists.

Now that the existence has been established, we turn to uniqueness, which can be established easily by the following results on extendibility.
**Theorem.** Let $\sigma:K\rightarrow L$ be an isomorphism of fields, $S\subset K[x]$ and $S'=\sigma S\subset L[x]$. If $F$ is a splitting field of $S$ over $K$ and $M$ is a splitting field of $S'$ over $L$, then $\sigma$ is extendible to an isomorphism $F\cong M$.
>[!proof]-
>The finite case can be reduced to the previous result on extendibility onto simple extensions by an induction on the index $[F:K]$. The infinite case is a routine argument via Zorn's lemma, where we consider triples $(E,N,\tau)$, with $E$ an intermediate field of $F/K$, $N$ is an intermediate field of $M/L$ and $\tau:E\rightarrow N$ is an isomorphism extending $\sigma$, and the partial ordering is defined in a natural way.

**Corollary.** $S\subset K[x]$, then any two splitting fields of $S$ over $K$ are $K$-isomorphic. In particular, any two algebraic closures of $K$ are $K$-isomorphic.

#### 3.2 Separability
Next we consider a phenomenon that occurs only in nonzero characteristic cases. Recall that the definition of multiple of a root and a simple/multiple root. Also recall the definition of a **separability**:
1. $f\in K[x]$ is *irreducible*, then $f$ is said to be **separable** if in the splitting field of $f$ over $K$, every root of $f$ is a simple root.
2. $F/K$ and $u\in F$ is *algebraic* over $K$, then $u$ is said to be separable over $K$ if its minimal polynomial is separable. And if every element of $F$ is (*algebraic* and) separable over $K$ then we say that $F/K$ is separable.

**Remarks.**
1. Recall the following lemma: let $D\subset E$ be integral domains and let $f\in D[x]$ and $c\in E$, then
	1. $c$ is a multiple root of $f$ if and only if it's the common root of $f$ and $f'$;
	2. if $D$ is a field and $(f,f')=1$, then $f$ has no multiple roots in $E$;
	3. if $D$ is a field, $f\in D[x]$ is irreducible and $E$ contains a root of $f$, then $f$ has no multiple roots in $E$ if and only if $f'\neq 0$. ($f$ is irreducible and $f'\neq0$ implies that $(f,f')=1$. Conversely, suppose $f$ has no multiple roots in $E$ and $b$ is a root of $f$ in $E$, then $f'=0$ implies that $b$ is a multiple root, which is a contradiction.)
2. By the lemma, an irreducible polynomial $f\in K[x]$ is separable if and only if $f'\neq0$, whence every irreducible polynomial is separable if $\mathrm{char}\,K=0$. Hence **every algebraic extension of fields of characteristic zero is separable**.
3. Separability is defined here only for irreducible polynomials, but we could say any polynomial is separable if all of its irreducible factor are separable.
4. We only define separable extensions for algebraic extensions here, but later we will define separability for possibly non-algebraic extensions. But we temporarily deals *only with algebraic extensions*.

**Theorem.** $F/K$, then TFAE.
1. $F/K$ is algebraic and Galois.
2. $F/K$ is algebraic, separable and $F$ is a splitting field over $K$ of a set $S$ of polynomials in $K[x]$.
3. $F$ is a splitting field over $K$ of a set of $T$ of *separable* polynomials in $K[x]$.
**Remark.** For finite case, we can take $T$ and $S$ to have only one element. Also, the theorem can be stated as: $F/K$ algebraic, then $F/K$ is separable and $F$ a splitting field over $K$ if and only if $F$ is a splitting field over $K$ of a set of separable polynomials, and these are equivalent to $F/K$ being algebraic and Galois.
>[!proof]-
>(1 $\Rightarrow$ 2&3) If $u\in F$ has minimal polynomial $f$, then it was proved in the lemma in 2.1 about stability that $f$ splits in $F[x]$ into product of distinct linear factors. Hence $u$ is separable over $K$. Let $\{v_i\,:\,i\in I\}$ be a basis of $F/K$ and for each $i\in I$ let $f_i\in K[x]$ be the minimal polynomial of $v_i$. Then each $f_i$ is separable and splits in $F[x]$. Therefore $F$ is a splitting field over $K$ of $S=\{f_i\,:\,i\in I\}.$
>
>(2 $\Rightarrow$ 3) Let $f\in S$ and let $g\in K[x]$ be a monic irreducible factor of $f$. Since $f$ splits in $F[x]$, $g$ must be the irreducible polynomial of some $u\in F$. Since $F/K$ is algebraic and separable, $g$ is necessarily separable. It follows that $F$ is a splitting field over $K$ of the set $T$ of of separable polynomials consisting of all monic irreducible factors of polynomials in $S$. Actually, if we just define separability for arbitrary polynomials, then we can just take $T=S$. Then we could restate this as: **$F/K$ is algebraic, separable and $F$ is a splitting field over $K$ of $S\subset K[x]$, then any $f\in S$ is separable**.
>(3 $\implies$ 1) $F/K$ is algebraic over $K$ since any splitting field over $K$ is an algebraic extension. If $u\in F-K$, then $u\in K(v_1,\dots,v_n)$ with each $v_i$ a root of some $f_i\in T$. Thus $u\in E=K(u_1,\dots,u_r)$ where $u_i$ are all the roots of $f_1,\dots,f_n$ in $F$. Hence $[E:K]$ is finite. Since each $f_i$ splits in $F$, $E$ is a splitting field over $K$ of $f=f_1\cdots f_n$. Assume for now that the theorem is true in the finite case. Then $E$ is Galois over $K$ and hence there exists $\tau Gal(E/K)$ such that $\tau(u)\neq u$. Since $F$ is a splitting field of $T$ over $E$, $\tau$ extends to an automorphism $\sigma\in Gal(F/K)$ such that $\sigma(u)=\tau(u)\neq u$. Therefore, $u\notin Gal(F/K)'$; that is, $F/K$ is Galois.
>Now we are reduced to the case when $[F:K]$ is finite. In this case there exist a finite number of polynomials $g_1,\dots,g_t\in T$ such that $F$ is a splitting field of $\{g_1,\dots,g_t\}$ over $K$. Furthermore, $Gal(F/K)=K'$ is a finite group since $\#Gal(F/K)=[Gal(F/K):1]=[K':F']\leq [F:K]<\infty$. Let $K_0=K''$, then $F/K_0$ is Galois with $[F:K_0]=\#Gal(F/K)$. Thus in order to show that $F/K$ is Galois (that is, $K=K_0$), it suffices to show that $[F:K]=\#Gal(F/K)$.
>We proceed by induction on $n=[F:K]$, with the case $n=1$ being trivial. If $n>1$, then one of the $g_i$, say $g_1$, has degree $s>1$. Let $u\in F$ be a root of $g_1$; then $[K(u):K]=\mathrm{deg}\,g_i=s$ since $g_i$ is irreducible and the number of distinct roots of $g_1$ is $s$ since it's separable. Recall that we have showed that there is an injective map from the set of all left cosets of $H=Gal(F/K(u))$ in $Gal(F/K)$ to the set of all roots of $g_1\in F$, given by $\sigma H\mapsto \sigma(u)$. Therefore, $[Gal(F/K):H]\leq s$. Now if $v\in F$ is any other root of $g_1$, there is an isomorphism $\tau:K(u)\cong K(v)$ with $\tau(u)=v$ and fixing $K$. Since $F$ is a splitting field over $K(u)$ and over $K(v)$ of the same set $\{g_1,\dots,g_t\}\subset K[x]$, $\tau$ extends to an automorphism $\sigma\in Gal(F/K)$ with $\sigma(u)=v$. Therefore, the map is also surjective. Since $[F:K(u)]=n/s<n$, the induction hypothesis implies that $[F:K(u)]=\#Gal(F/K(u))=\#H$. Therefore, $$[F:K]=[F:K(u)][K(u):K]=\#H\cdot s=\#H\cdot[Gal(F/K):H]=\#Gal(F/K).$$

>[!info] Very General Techniques
>The third part of the proof shows a standard process dealing with problem of field extensions. First we reduce the problem to finite case by considering an intermediate field that only added finitely many appropriate elements. We probably want to add all roots, i.e. take the intermediate field as a splitting field, because then we would have beautiful extendibility properties and Galois correspondences. Now once the problem is reduced to the finite case, we use induction on index by introducing a simple extension as an intermediate field.
>The reason why we can reduce to the finite case is that all wonderful concepts are defined elementwise. Local-global principal is literally everywhere in mathematics! This fancy way of defining concepts, a global property (about an extension) is defined as a local property (about one single element) satisfied everywhere, is the way we mathematicians use to deal with infinity and complicated global structures.
>Notice also how properties are naturally satisfied with a larger base field or a smaller extension field since they are defined via polynomials or elements.

**Theorem.** (Generalized Fundamental Theorem) $F/K$ an algebraic Galois extension, then there is a one-to-one correspondence between the set of all intermediate fields and the set of all *closed* subgroups of $Gal(F/K)$ (given by $E\mapsto E'=Gal(F/E)$) such that: $F$ is Galois over any intermediate field $E$, but $E$ is Galois over $K$ if and only if the corresponding subgroup $E'$ is normal in $G=Gal(F/K)$; in this case $G/E'=Gal(F/K)/Gal(F/E)$ is (isomorphic to) $Gal(E/K)$.
**Remark.** If $[F:K]$ is infinite, then there are always subgroups of $Gal(F/K)$ that are *not* closed, and the proof uses topological group theory, which shows that considering the closed subgroups as topologically closed subsets makes $Gal(F/K)$ into a compact topological group. See the original remark after Theorem 3.12 of GTM73 for more information.
>[!important]- Grand Structure: Algebra-Geometry Duality
>It seems that infinite algebra structures tend to have natural topological structures. For example, compare this with Zariski topology in algebraic geometry. Theory of Galois connection describes this phenomenon. See [this](https://ncatlab.org/nlab/show/duality+between+algebra+and+geometry) page on nlab.

>[!proof]-
>In view of theorems in section 2.1, we only need to show that every intermediate field is closed in order to establish the one-to-one correspondence. They are closed because by the previous theorem, $F$ is a splitting field of a set of separable polynomials $T$ over $K$, and therefore $F$ is also a splitting field of $T$ over any intermediate field $E$. Hence by the theorem again, $F/E$ is Galois; that is, $E$ is closed.
>For the second part of the theorem, there's no difference between the finite and infinite cases to prove that for any intermediate field $E$, $E/K$ is Galois if and only if $E'\lhd Gal(F/K)$. If $E=E''$ is Galois over $K$, so that $E'$ is normal in $G=Gal(F/K)$, then $E$ is a stable intermediate field. Therefore $G/E'\cong \{\sigma\in Gal(E/K)\,:\,\sigma\text{ is extendible to }F\}$. But $F$ is a splitting field over $K$ and hence over $E$ also. Therefore, every $K$-automorphisms in $Gal(E/K)$ extends to $F$.

#### 3.3 Normality and Normal Closure
The concept of splitting fields is not very natural, so now we fix that by the appropriate concept, normality, by dropping of specific set of polynomials. Also notice how we establish this via a categorical flavor intermediate step.
Recall that $F/K$ is **normal** if every irreducible polynomial in $K[x]$ that has a root in $F$ actually splits in $F[x]$.

**Lemma.** $F/K$ algebraic, then $F/K$ is normal if and only if for every $K$-monomorphism $\sigma:F\rightarrow N$, where $N$ is any normal extension of $K$ containing $F$, $\sigma(F)=F$ so that $\sigma\in Gal(F/K)$.
**Theorem.** $F/K$ is algebraic, then TFAE.
1. $F/K$ is normal.
2. $F$ is a splitting field over $K$.
3. If $\bar{K}$ is an algebraic closure of $K$ containing $F$, then for any $K$-monomorphism of fields $\sigma:F\rightarrow \bar{K}$, $\mathrm{im}\,\sigma=F$ and hence $\sigma\in Gal(F/K)$.
4. Item 3 is still true if we replace $\bar{K}$ with any normal extension $E$ of $K$ containing $F$.
**Remark.** The fancy part of this theorem is that by splitting certain polynomials, we actually guarantees that every element has its "companion", i.e. other roots of its minimal polynomial, added.
>[!proof]-
>(1 $\implies$ 2) Just take the set of minimal polynomials of a basis of $F/K$.
>(2 $\implies$ 4) Just observe that $\sigma$ permutes roots of any polynomial.
>(4 $\implies$ 3) Trivial.
>(3 $\implies$ 1) Let $f\in K[x]$ be an irreducible polynomial with a root $u\in F$, then $E$ contains all roots of $f$. If $v\in E$ is an root of $f$ then there is a $K$-isomorphism $\sigma:K(u)\cong K(v)$ with $\sigma(u)=v$, which extends to a $K$-automorphism of $E$ by the lemma. Then by hypothesis, $v\in F$, which implies that $f$ splits in $F$. Hence $F/K$ is normal. The logic on gtm73 is not like this, there we prove the equivalence of 1, 2&3, then the next theorem and we come back to prove the lemma and establish this full theorem.

**Corollary.** $F/K$ is algebraic, then $F/K$ is Galois if and only if $F/K$ is normal and separable. If $\mathrm{char}\,K=0$, then $F/K$ is Galois if and only if $F/K$ is normal.
**Theorem.** $E/K$ algebraic, then there exists $F/E$ such that
1. $F/K$ is normal;
2. no proper subfield of $F$ containing $E$ is normal over $K$;
3. if $E/K$ is separable, then $F/K$ is Galois;
4. $[F:K]$ is finite if and only if $[E:K]$ is finite.
The field $F$ is uniquely determined up to an $E$-isomorphism by 1&2, and is called the **normal closure** of $E/K$.
>[!proof]-
>Just let $F$ be the splitting field of the set of minimal polynomials of a basis of $E/K$, then $F/K$ is normal by the previous theorem. 2 and 3 and the uniqueness are trivial by the construction. If $E/K$ is separable, then each $f_i$ is separable and hence $F/K$ is separable.

#### 3.4 Appendix: The Fundamental Theorem of Algebra
In this section, we prove the well-known theorem assuming the followings:
1. every positive real number has a real positive square root;
2. every polynomial in $\mathbb{R}[x]$ of odd degree has a root in $\mathbb{R}$.
Also, a few lemmas in this section are useful in their own interests.

**Lemma.** $F/K$ is finite and either
1. $K$ is a finite field, or
2. $F/K$ is separable,
then $F/K$ is simple.
>[!proof]-
>If $K$ is a finite field, then $F$ is also a finite field and by the fact that the multiplicative group of a finite field is cyclic, which we will prove later, we can choose a generator $\theta$ of its multiplicative group and clearly $F=K(\theta)$.
>Now suppose $F$ is infinite. Choose any finite set of generator of $F/K$, say $a_1,\dots,a_r$ and we induct on $r$. When $r=2$, say $F=K(a,b)$ and the minimal polynomials of $a,b$ are $f,g$. Let $E$ be the splitting field of $fg$ over $K$ and suppose that $a_1=a,a_2,\dots,a_s$ and $b_1=b,b_2,dots,b_t$ are all roots of $f$ and $g$ respectively. Consider the following system of equations:$$a_i+yb_j=a+yb\;\;(1\leq i\leq,2\leq j\leq t).$$
>There are $s(t-1)$ equations and each of them has at most one solution in $K$, so there exists $c\in K$ *not* satisfying any of them. Now let $\theta=a+cb$.
>*Claim.* $F=K(\theta)$. Clearly $K(\theta)\subset K(a,b)=F\subset E$. On the other hand, since $b$ is a root of $f(\theta-cx)$ whereas $b_2,\dots,b_t$ are not, $f(\theta-cx)$ and $g(x)$ have at most one common root $b$. So $(f(\theta-cx),g(x))=x-b$ in $E[x]$. Notice that $f(\theta-cx),g(x)\in K(\theta)[x]$, so $(f(\theta-cx),g(x))=x-b$ in $F(\theta)[x]$. Therefore $b,a=\theta-cb\in K(\theta)$ and $K(a,b)=K(\theta)$. *(Key observation! Factors split as the field extends and gcd is independent of the coefficient field.)*
>Finally for $r>2$, repeat the process for pairs.
>Also, gtm73 gives a neat proof. If $[F:K]$ is finite, then we can choose $u\in F$ such that $[K(u):K]$ is maximal. If $K(u)\neq F$, there exists $v\in F-K(u)$. Consider all intermediate fields of the form $K(u+av)$ with $a\in K$. Since $K$ is infinite and there are only finitely many intermediate fields, there exist $a,b\in K$ such that $a\neq b$ and $K(u+av)=K(u+bv)$. Therefore $(a-b)v=(u+av)-(u+bv)\in K(u+av)$. Since $a\neq b$, we have $v\in K(u+av)$, whence $u=(u+av)-av\in K(u+av)$. Consequently $K\subset K(u)\subsetneq K(u+av)$, whence $[K(u+av):K]>[K(u):K]$. This contradicts the choice of $u$ and hence $K(u)=F$.

**Remark.** For a simple algebraic extension $F=K(u)$, $u$ is also called a primitive element of $F/K$. Before Artin's reconstruction of Galois theory, proofs relied heavily on primitive elements and algebra on polynomials.
**Lemma.** There are no extension fields of dimension 2 over $\mathbb{C}$.
**Theorem.** $\mathbb{C}$ is algebraically closed.
(See gtm73 for proofs.)

#### 3.5 Some Other Results
1. $F/K$ is generated by a (possibly infinite) set of separable elements over $K$, then $F/K$ is separable.
2. $F/K$ finite, then TFAE.
	1. $F/K$ is Galois.
	2. $F/K$ is separable and $F$ is the splitting field of some $f\in K[x]$.
	3. $F$ is the splitting field of a separable $f\in K[x]$.
3. $F/K$, $L$ and $M$ are intermediate fields. If $L/K$ is finite and Galois, then $LM/M$ is also finite and Galois and $Gal(LM/M)\cong Gal(L/(L\cap M))$.
4. $K\subset E\subset F$.
	1. If $F/K$ is algebraic and Galois, then $F/E$ is algebraic and Galois. (The "algebraic" hypothesis is necessary!)
	2. If $F/E$ is Galois, then $E/K$ is Galois and $F$ is a splitting field over $E$ of a family polynomials in $K[x]$, then $F/K$ is Galois.
5. $K\subset E\subset F$. If $E/K$ is normal, then $E$ is stable relative to $F/K$.
6. $K\subset E\subset F$. If $F/K$ is normal, then $E/K$ is normal if and only if $E$ is stable relative to $F/K$. Furthermore $Gal(F/K)/Gal(F/E)\cong Gal(E/K)$.
7. Part two of the Fundamental Theorem (also the generalized version) is equivalent to: an intermediate field $E$ is normal over $K$ if and only if $E'\lhd G=Gal(F/K)$, and in this case $G/E'\cong Gal(E/K)$.
8. $F/K$ algebraic and $\forall u\in F\,\exists\text{ intermediate field }E\;\;E/K\text{ is normal and }u\in E$, then $F/K$ is normal.
9. $[F:K]=2$, then $F/K$ is normal.
10. $F/K$ algebraic. $F/K$ is normal if and only if $\forall\text{ irreducible }f\in K[x]\;\;f\text{ factors in }F[x]\text{ into irreducible factors of the same degree}$.
### 4. The Galois Group of a Polynomial
Recall that the Galois group of $f\in K[x]$ is the group $Gal(F/K)$ where $F$ is the splitting field of $f$ over $K$.
**Theorem.** $f\in K[x]$ with Galois group $G$.
1. $G<S_n$, where $n$ is the number of distinct roots of $f$ and hence $1\leq n\leq\mathrm{deg}\,f$.
2. If $f$ is irreducible and separable of degree $n$, then $n\mid\#G$ and $G$ is transitive (under the natural action of $S_n$ on $n$ elements.)
>[!proof]-
>A $K$-automorphism of $F$ permutes roots of $f$ and is completely determined by their action on them, so 1 follows. If $f$ is irreducible and separable of degree $n$, then $F/K$ is Galois and $G$ is transitive by considering simple intermediate extensions of roots of $f$ over $K$. Let $u$ be a root of $f$, then $n=[K(u):K]\mid [F:K]=\#G$.

**Corollary.** $f\in K[x]$ irreducible of degree 2 with Galois group $G$. If $f$ is separable (as is always the case when $\mathrm{char}\,K\neq2$), then $G\cong\mathbb{Z}/2$; otherwise $G=1$.

**Definition.** Let $K$ be a field with $\mathrm{char}\,K\neq2$ (!) and $f\in K[x]$ a polynomial of degree $n$ with $n$ distinct roots $u_1,\dots,u_n$ in some splitting field $F$ of $f$ over $K$. Let$$\Delta=\prod_{i<j}(u_i-u_j)\in F.$$Then the **discriminant** of $f$ is the element $D=\Delta^2$.
**Remark.** Notice that $\Delta$ can be written as a Vandermonde determinant in $u_1,\dots,u_n$, so $D$ is the determinant of $(s_{i+j-2})$, where $s_k=\sum_iu_i^k$ can be expressed by coefficients of $f$ via Newton's identity.)
**Proposition.** Let $K,f,F$ and $\Delta$ be as in the definition.
1. $D$ actually lies in $K$.
2. For each $\sigma\in Gal(F/K)<S_n$, $\sigma$ is an even (resp. odd) premutation if and only if $\sigma(\Delta)=\Delta$ (resp. $\sigma(\Delta)=-\Delta$).
**Corollary.** Let $K,f,F,\Delta$ be as in the definition (so that $F/K$ is Galois) and consider $G=Gal(F/K)<S_n$. In the Galois correspondence, the subfield $K(\Delta)$ corresponds to the subgroup $G\cap A_n$. In particular, $G$ consists of even permutations if and only if $\Delta\in K$.

TBD
### 5. Finite Fields
#### 5.1 Structure of Finite Fields
**Theorem.** Let $F$ be a field and $P$ the intersection of all subfields of $F$, then $P$ is a field with no proper subfields. If $\mathrm{char}\,F=p$, then $P\cong \mathbb{F}_p$. If $\mathrm{char}\,F=0$, then $P\cong \mathbb{Q}$.
$P$ is called the **prime subfield** of $F$.
**Corollary.** If $F$ is a finite field, then $\mathrm{char}\,F=p\neq0$ and $\#F=p^n$ for some integer $n\geq1$.
**Theorem.** If $F$ is a field and $G$ is a finite subgroup of the multiplicative group $F^*=F-\{0\}$, then $G$ is cyclic. In particular, the multiplicative group of all nonzero elements of a finite field is cyclic.
**Corollary.** If $F$ is a finite field, then $F$ is a simple extension of its prime subfield $\mathbb{F}_p$.
(These are easy consequences of the structure theorem for finitely generated abelian groups.)

**Lemma.** $\mathrm{char}\,F=p>0$ and $r\geq1$ is an integer, then $\varphi_r:F\rightarrow F$ given by $u\mapsto u^{p^r}$ is a $\mathbb{F}_p$-monomorphism. If $F$ is finite, then $\varphi_r\in Gal(F/(\mathbb{F}_p))$, and is called the $r$-th Frobenius automorphism. For $r=1$, we just call it the Frobenius automorphism.
**Proposition.** Let $p$ be a prime and $n\geq1$ an integer, then $F$ is a field with $p^n$ elements if and only if $F$ is a splitting field of $x^{p^n}-x$ over $\mathbb{F}_p$.
>[!proof]-
>If $\#F=p^n$, then $\#F^*=p^n-1$ and hence every nonzero $u\in F$ satisfies $u^{p^n-1}-1=0$ and therefore every element in $F$ is a root of $f=x^{p^n}-x\in\mathbb{F}_p[x]$. So $f$ has $p^n$ distinct roots in $F$ and $F$ must be the splitting field of $f$.
>Conversely, since $f'=-1$ and $f$ is relatively prime to $f'$, $f$ has $p^n$ distinct roots in $F$. Clearly $\varphi_n(u)=u$ if and only if $f(u)=0$ for an $u\in F$. So the roots of $f$ form an intermediate field $E=<\varphi_n>'$. Therefore $F=E$.

**Corollary.** If $p$ is a prime and $n\geq1$ is an integer, then there exists a field with $p^n$ elements. Any two finite fields with the same number of elements are isomorhpic.
**Corollary.** If $K$ is a finite field and $n\geq1$ is an integer, then there exists a simple extension $F=K(u)$ such that $[F:K]=n$.  Any two $n$-dimensional extension fields of $K$ are $K$-isomorphic. Actually, if $\#E=p^r$, then $F$ is the splitting field of $x^{p^{rn}}-x$ over $K$ (or over $\mathbb{F}_p$) and $\#F=p^{rn}$.
**Corollary.** If $K$ is a finite field and $n\geq1$ is an integer, then there exists an irreducible polynomial of degree $n$ in $K[x]$.
**Proposition.** $K$ finite and $F/K$ finite, then $F$ is finite and is Galois over $K$. If $[F:K]=n$, then $Gal(F/K)\cong\mathbb{Z}/p$ and is generated by the Frobenius automorphism $u\mapsto u^p$, where $p=\mathrm{char}\,K$.
#### 5.2 Infinite Galois Theory
**Proposition.** The algebraic closure of $\mathbb{F}_p$ is the splitting field of $\{P_n=x^{p^n}-x\,:\,n\in\mathbb{N}\}\subset\mathbb{F}_p[x]$, i.e. the union of all finite fields of characteristic $p$ is $\bar{\mathbb{F}}_p$.
>[!proof]-
>Let $F$ be the splitting field, we need to show that $F$ is algebraically closed. For any polynomial $f\in F[x]$, there exists $n$ such that $f\in\mathbb{F}_{p^n}[x]$. (Every coefficient lies in some $\mathbb{F}_{p^{n_i}}$, so we can let $n$ be the lcm of these $n_i$'s.) So all roots of $f$ lie in the splitting field of $f$ over $\mathbb{F}_{p^n}$, which is also a finite field. Therefore all roots of $f$ lie in $F$ and $F$ is algebraically closed.

We can consider the set $\mathfrak{L}_p$ of all finite intermediate fields of $\bar{\mathbb{F}}_p/\mathbb{F}_p$ and the set $\bar{\mathfrak{L}}_p$ of all intermediate fields. Now $\mathfrak{L}_p$ is closed under operations $\cap$ and $\cdot$ of intermediate fields, i.e. it is a sub-lattice of $\bar{\mathfrak{L}}_p$. Recall that $(\mathbb{N},\mathrm{gcd},\mathrm{lcm})$ is a distributive lattice. (Actually for any commutative ring, all its ideals form a modular lattice. If the ring is a PID, then this is a distributive lattice.) We can show that the map $\mathbb{N}\rightarrow\mathfrak{L}_p$ given by $n\mapsto\mathbb{F}_{p^n}$ is in fact a lattice isomorphism. The key is to prove that the set of polynomials $\mathcal{S}_p=\{P_n\}\subset\mathbb{F}_p[x]$ inherits a lattice structure and the map $\mathbb{N}\rightarrow\mathcal{S}_p$ given by $n\mapsto P_n$ is an isomorphism of lattices. Besides, the full lattice $\bar{\mathfrak{L}}_p$ corresponds to the lattice of *supernatural numbers*. These structures also carry over to the Galois groups. Most importantly, with the lattice structure of supernatural numbers, it's natural to guess that the direct limit of all absolute Galois groups $Gal(L/\mathbb{F}_p)$ is actually isomorphic to $Gal(\bar{\mathbb{F}}_p/\mathbb{F}_p)$! And these observations give rise to a much general theory, called the Infinite Galois Theory. See [[Infinite Galois Theory.pdf]].
### 6. Separability
#### 6.1 Purely Inseparable Extension
First recall the definition of purely inseparability. $F/K$.
1. An *algebraic* element $u\in F$ is **purely inseparable** over $K$ if its minimal polynomial $f\in K[x]$ factors in $F[x]$ as $f=(x-u)^m$.
2. $F/K$ is purely inseparable if every element of $F$ is inseparable over $K$.
>[!tip] Useful Trick
>We will use frequently the fact that if $F/K$ is separable/purely inseparable, then the property is kept as $K$ gets larger or $F$ gets smaller.

**Theorem.** $F/K$. Then $u\in F$ is both separable and purely inseparable over $K$ if and only if $u\in K$.
If $\mathrm{char}\,K=0$, then every algebraic element over $K$ is separable over $K$, therefore the only elements that are purely in separable over $K$ are the elements in $K$. Thus purely inseparable extensions of $K$ are trivial if $\mathrm{char}\,K=0$.
**Lemma.** $F/K$, $\mathrm{char}\,K=p>0$. If $u\in F$ is algebraic over $K$, then $u^{p^n}$ is separable over $K$ for some $n\geq0$.
>[!proof]-
>Induct on the degree $d$ of $u$ over $K$. Case $d=1$ or $u$ being separable is trivial. Let $f$ be the minimal polynomial of $u$. If $u$ is not separable and $d>1$, then $f'=0$, whence $f$ is a polynomial in $x^p$. Therefore $u^p$ is algebraic of degree less than $d$ over $K$, and the lemma follows by induction.

**Lemma.** $F/K$, $\mathrm{char}\,K=p>0$. If $u\in F$ is algebraic, then TFAE.
1. $u$ is purely inseparable over $K$.
2. The minimal polynomial of $u$ is of the form $x^{p^n}-a\in K[x]$. 
3. $u^{p^n}\in K$ for some $n\geq0$.
>[!proof]-
>(1 $\Rightarrow$ 2) Suppose $u$ is purely inseparable over $K$, then let $(x-u)^m$ be the minimal polynomial of $u\in F$, and let $m=np^r$ with $(n,p)=1$. Then $(x-u)^m=(x^{p^r}-u^{p^r})^n$. Since $(x-u)^m\in K[x]$, the coefficient of $x^{p^r(n-1)}$, namely $\pm nu^{p^r}$, must lie in $K$. Now $(p,n)=1$ implies that $u^{p^r}\in K$. Since $(x-u)^m$ is irreducible in $K[x]$, we must have $n=1$ and $(x-u)^m=x^{p^r}-a$, where $a=u^{p^r}\in K$.
>(2 $\Rightarrow$ 3) is trivial.
>(3 $\Rightarrow$ 1) Let $a=u^{p^n}\in K$, then the minimal polynomial of $u$ over $K$ divides $x^{p^n}-a\in K[x]$. Since $x^{p^n}-a=(x-u)^{p^n}\in F[x]$, we see that the minimal polynomial of $u$ splits as $(x-u)^m$ in $F[x]$.

**Theorem.** $F/K$ algebraic, $\mathrm{char}\,K=p>0$, then TFAE.
1. $F/K$ is purely inseparable.
2. $\forall u\in F$, the minimal polynomial of $u$ is of the form $x^{p^n}-a\in K[x]$.
3. $\forall u\in F\,\exists n\geq0\;\;u^{p^n}\in K$.
4. The only elements of $F$ which are separable over $K$ are the elements of $K$.
5. $F$ is generated over $K$ by a set of purely inseparable elements.
>[!proof]-
>(1 $\Rightarrow$ 2) is the previous lemma. (2 $\Rightarrow$ 3), (3 $\Rightarrow$ 1) and $(1 $\Rightarrow$ 5)$ are easy. (1 $\implies$ 4) follows from the theorem above and (4 $\implies$ 3) by the lemma above. (5 $\implies$ 3) If $u$ is purely inseparable over $K$, then $u^{p^n}\in K$ for some $n\geq0$ b the previous lemma. If $u$ is arbitrary, then $u$ is a polynomial with coefficients in $K$ of some purely inseparable elements. There exists $n$ such that the $p^n$ power of these purely inseparable elements lie in $K$, so the $p^n$ power of $u$ lie in $K$.

**Corollary.** $F/K$ is finite and purely inseparable and $\mathrm{char}\,K=p>0$. Then $[F:K]=p^n$ for some $n\geq0$.
>[!proof]-
>Suppose $F=K(u_1,\dots,u_r)$, then $u_r$ is purely inseparable over $K$ and hence over $K(u_1,\dots,u_{r-1})$. So the minimal polynomial of $u_r$ over $K(u_1,\dots,u_{r-1})$ is of the form $x^{p^{n_r}}-a$ and $[F:K(u_1,\dots,u_{r-1})]=p^{n_r}$. The corollary then follows by induction on $r$.
#### 6.2 Separable Closure
**Lemma.** $F/K$, $X\subset F$ and $F=K(X)$. If every element of $X$ is separable over $K$, then $F/K$ is separable.
>[!proof]-
>For any $v\in F$, there exist $u_1,\dots,u_n\in X$ such that $u\in K(u_1,\dots,u_n)$. Let $f_i$ be the minimal polynomial of $u_i$ over $K$, which is separable over $K$, and let $E$ be the splitting field of $f_1,\dots,f_n$ over $K$, then $E/K$ is Galois and hence separable. Therefore $v\in E$ is separable over $K$.

**Theorem.** $F/K$ algebraic. Let $S:=\{u\in F\,:\,u\text{ is separable over }K\}$ and $P=\{u\in F\,:\,u\text{ is purely inseparable over }K\}$.
1. $S/K$ is a separable extension.
2. $F/S$ is purely inseparable.
3. $P/K$ is a purely inseparable extension.
4. $P\cap S=K$.
5. $F/P$ is separable if and only if $F=SP$.
6. If $F/K$ is normal, then $S/K$ is Galois, $F/P$ is Galois and $Gal(S/K)\cong Gal(F/P)=Gal(F/K)$.
**Remark.** It is clear that $S$ is the unique largest subfield of $F$ separable over $K$ and that $S$ contains every intermediate field that is separable over $K$; similarly for $P$ and purely inseparable intermediate fields. If $\mathrm{char}\,K=0$, then $S=F$ and $P=K$. Also, by the theorem we see that in general we add separable elements first, i.e. we use $S$, the **separable closure**, as an intermediate field, and an algebraic extension is split into a separable extension followed by a purely inseparable extension.
>[!proof]-
>If $\mathrm{char}\,K=0$, then all are trivial. So we assume $\mathrm{char}\,K=p>0$.
>1. $S$ is a subfield by the lemma and 1 follows easily.
>2. For any $u\in F$, there exists $n\geq0$ such that $u^{p^n}\in S$, so $F/S$ is purely inseparable by results from the previous section.
>3. Since $u\in P$ if and only if $u^{p^n}\in K$ for some $n$, we see that $P$ is a field.
>4. Easy.
>5. If $F/P$ is separable then $F/SP$ is separable. But $F/SP$ is also purely inseparable since $F/S$ is purely inseparable, so $F=SP$. Conversely, if $F=SP$, then $F/P$ is separable by the previous lemma.
>6. *Claim.* $K''=:K_0=P$. Let $u\in F$ have minimal polynomial $f\in K[x]$ and let $\sigma\in Gal(F/K)$, then $\sigma(u)$ is a root of $f$. If $u\in P$, then $f=(x-u)^m$ and hence $\sigma(u)=u$. Therefore $P\subset K_0$. Conversely, if $u\in K_0$ and $v\in F$ is any other root of $f$, then there is a $K$-isomorphism $\tau:K(u)\rightarrow K(v)$ such that $\tau(u)=v$. Since $F/K$ is normal, $\tau$ extends to an element of $Gal(F/K)$. Since $u\in K_0$, we have $u=\tau(u)=v$. Since $f$ splits in $F[x]$ by normality, this argument shows that $f=(x-u)^m$ for some $m$. Therefore, $u\in P$ and $K_0\subset P$. Hence $P=K_0$. The claim immediately implies that $Gal(F/K)=Gal(F/P)$ and $F/P$ is Galois. Now, every element $\sigma\in Gal(F/P)=Gal(F/K)$ *must send separable elements to separable elements since they fix minimal polynomials over $K$*. So $\sigma\mapsto\sigma|_S$ defines a homomorphism $Gal(F/P)\rightarrow Gal(S/K)$. Since $F/S$ is normal, $\theta$ is an epimorphism. Since $F/P$ is Galois, $F/P$ is separable and hence $F=SP$, which implies that $\theta$ is a monomorphism. So $Gal(F/P)\cong Gal(S/K)$. Finally, suppose $u\in S$ is fixed by every $\sigma\in Gal(S/K)$, then since it is fixed by every element in $Gal(F/P)$. Since $F/P$ is Galois, we have $u\in P\cap S=K$. Therefore $S/K$ is Galois.

**Corollary.** If $F/E$ and $E/K$ are algebraic and separable extensions, then so is $F/K$.
Let $F$ be a field of characteristic $p>0$, then $F^{p^n}:=\{u^{p^n}\,:\,u\in F\}$ is a subfield of $F$. Then by the theorem in 6.1, $F/F^{p^n}$ is purely inseparable and hence over any intermediate field as well.
**Corollary.** $F/K$ algebraic, $\mathrm{char}\,K=p>0$. If $F/K$ is separable, then $F=KF^{p^n}$ for each $n\geq1$. If $[F:K]<\infty$ and $F=KF^p$, then $F/K$ is separable. In particular, $u\in F$ is separable over $K$ if and only if $K(u^p)=K(u)$.
>[!proof]-
>If $F/K$ is separable, then $F/KF^{p^n}$ is separable. But since $F/F^{p^n}$ is purely inseparable, $F/KF^{p^n}$ is also purely inseparable, so we must have $F=KF^{p^n}$.
>Let $S$ be the separable closure of $F/K$. If $[F:K]<\infty$, then we can write $F=K(u_1,\dots,u_r)$. Since $F/S$ is purely inseparable, there is an $n\geq$ such that $u_i^{p^n}\in S$ for every $i$. So $F^{p^n}\subset S$. $S/F^{p^n}$ is purely inseparable since $F/F^{p^n}$ is, and hence $S/KF^{p^n}$ is purely inseparable. But $S/KF^{p^n}$ is also separable since $S/K$ is, so $S=KF^{p^n}$. For any $t\geq1$, $F^{p^t}=K^{p^t}(u_1^{p^t},\dots,u_r^{p^t})$ and hence $KF^{p^t}=K(u_1^{p^t},\dots,u_r^{p^t})$. Now if $F=KF^p$, then $K(u_1,\dots,u_r)=F=KF^p=K(u_1^p,\dots,u_r^p)$. An iterated argument with the generators $u_i^{p^t}$ in place of $u_i$ shows that $F=K(u_1,\dots,u_r)=K(u_1^{p^n},\dots,u_r^{p^n})=KF^{p^n}=S$, whence $F/K$ is separable over $K$.
#### 6.3 Separable and Inseparable Degrees
$F/K$ is algebraic and $S$ its separable closure.
1. $[F:K]_s:=[S:K]$ is called the **separable degree** of $F/K$.
2. $[F:K]_i:=[F:S]$ is called the **inseparable degree** of $F/K$.
3. Clearly $[F:K]=[F:K]_s[F:K]_i$.
4. If $[F:K]<\infty$ and $\mathrm{char}\,K=p>0$, then $[F:K]_i$ is a power of $p$.
5. Consequently, if $\mathrm{char}\,K=p>0$ and $[F:K]<\infty$ and is not divisible by $p$, then $F/K$ is separable.
**Lemma.** $N/F/E/K$ and $N/K$ normal. Let $r:=\#\text{distinct }E\text{-monomorphisms }F\rightarrow N$ and $t:=\#\text{distinct }K\text{-monomorphisms }E\rightarrow N$, then $rt=s:=\#\text{distinct }K\text{-monomorphisms }F\rightarrow N$.
>[!proof]-
>Each $K$-monomorphism $\sigma:E\rightarrow N$ extends to a $K$-automorphism of $N$ and its composition with any $E$-monomorphism $\tau:F\rightarrow N$ is a $K$-monomorphism $\sigma\tau:F\rightarrow N$. Now for any such $\sigma,\sigma',\tau,\tau'$, if $\sigma\tau=\sigma'\tau'$, then $\sigma'^{-1}\sigma\tau=\tau'$, which implies that $\sigma'|_E=\sigma|_E$. Since $\sigma$ is injective, we also have $\tau=\tau'$. Therefore by making a choice of extensions of all $\sigma$, we have proved that $rt\leq s$. Let $\sigma:F\rightarrow N$ be any $K$-monomorphism. Then $\sigma|_E$ is a $K$-monomorphism $\sigma':E\rightarrow N$. Continuing with the choices made above, $\tau=\sigma'^{-1}\sigma:F\rightarrow N$ is a $E$-monomorphism. Therefore $s\leq rt$.

**Proposition.** $N/F/K$, $F/K$ finite and $N/K$ normal. Then $$\#\text{distinct }K\text{-monomorphisms }F\rightarrow N=[F:K]_s$$
>[!proof]-
>Let $S$ be the separable closure of $F/K$. Every $K$-monomorphism $S\rightarrow N$ extends to a $K$-automorphism of $N$, and hence to a $K$-monomorphism $F\rightarrow N$. We claim that the number of distinct $K$-monomorphisms $F\rightarrow N$ is the same as the number of distinct $K$-monomorphisms $S\rightarrow N$. This is trivially true if $\mathrm{char}\,K=0$. So let $\mathrm{char}\,K=p>0$ and suppose $\sigma,\tau$ are $K$-monomorphisms $F\rightarrow N$ such that $\sigma|_T=\tau|_S$. If $u\in F$, then $u^{p^n}\in S$ for some $n\geq0$. Therefore $\sigma(u)^{p^n}=\tau(u)^{p^n}$, whence $\sigma(u)=\tau(u)$. Thus $\sigma|_S=\tau|_S$ implies that $\sigma=\tau$, which proves our claim. Consequently, it suffices to assume that $F/K$ is separable.
>Proceed now by induction on $n=[F:K]=[F:K]_s$ with the case $n=1$ being trivial. If $n>1$, choose $u\in F-K$; then $[K(u):K]=r>1$. If $r<n$, use the induction hypothesis and the previous lemma. If $r=n$, then $F=K(u)$ and $[F:K]=\mathrm{deg}\,f$, where $f\in K[x]$ is the minimal polynomial of $u$ over $K$. Every $K$-monomorphism $\sigma:F\rightarrow N$ is completely determined by $\sigma(u)=v$. Since $v$ is a root of $f$, there are at most $[F:K]$ such $K$-monomorphisms. Since $f$ splits in $N$ by normality and is separable, there are exactly so many.

>[!tip] Useful Viewpoint
>From the proof, we can see that the key is that we can break down $F/K$ into simples extensions and for the simple case, a $K$-monomorphism $K(u)\rightarrow K$ is a choice of root of the minimal polynomial of $u$. So in general, we can memorize this result by thinking that **a $K$-monomorphism $F\rightarrow N$ is a choice of roots, and the separable index is just the number of choices**.
>Also, this viewpoint explains why separable index is multiplicative.

**Corollary.** $F/K$ is inseparable if and only if $F/K$ is algebraic and for any extension $E/F$, the only $K$-monomorphism $F\rightarrow E$ is the inclusion map.
**Corollary.** $F/E/K$, then $[F:E]_s[E:K]_s=[F:K]_s$ and $[F:E]_i[E:K]_i=[F:K]_i$.
**Corollary.** $F/E/K$.
1. If $F/E$ and $E/K$ are separable/purely inseparable, then so is $F/K$.
2. If $F/K$ is separable/purely inseparable, then so is $F/E$ and $E/K$.

**Corollary.** Let $f\in K[x]$ be irreducible and monic, $F$ the splitting field of $f$ over $K$ and $u_1$ a root of $f$ in $F$.
1. Ever root of $f$ has multiplicity $[K(u_1):K]_i$, so that in $F[x]$,$$f=\prod_i(x-u_i)^{[K(u_1):K]_i}.$$
2. $u_1^{[K(u_1):K]_i}$ is separable over $K$.
>[!proof]-
>Case $\mathrm{char}\,K=0$ is trivial, so assume $\mathrm{char}\,K=p>0$. For any $i>1$, there is a $K$-isomorphism $\sigma:K(u_1)\cong K(u_i)$ with $\sigma(u_1)=u_i$ that extends to a $K$-isomorphism $\sigma$ of $F$. Since $f\in K[x]$ we have$$\prod_i(x-u_i)^{r_i}=f=\sigma f=\prod_i(x-\sigma(u_i))^{r_i}.$$So $r:=r_1=r_i$ and $[K(u_1):K]=\mathrm{deg}\,f=nr$.Now there are $n$ distinct $K$-monomorphisms $K(u_1)\rightarrow F$, whence $[K(u_1):K]_s=n$ and $[K(u_1):K]_i=r$.
>Since $r$ is a power of $p$, we have $f=\prod_i(x^r-u_i^r)$. Thus $f$ is a polynomial in $x^r$ with coefficients in $K$, say $f=g(x^r)$. Consequently, $u_1^r$ is a root of $g\in K[x]$, which has no multiple roots. Therefore $u_1^r$ is separable over $K$.

**Corollary.** Let $\mathrm{char}\,K=p\neq0$ and let $f\in K[x]$ be irreducible of degree $n$. Let $m$ be the largest nonnegative integer such that $f$ is a polynomial in $x^{p^m}$ but is not a polynomial in $x^{p^{m+1}}$. Then $n=n_0p^m$. If $u$ is a root of $f$, then $[K(u):K]_s=n_0$ and $[K(u):K]_i=p^m$.
**Corollary.** If $f\in K[x]$ is irreducible of degree $m>0$, and $\mathrm{char}\,K>0$ does *not* divide $m$, then $f$ is separable.

**Proposition.** (Primitive Element Theorem) $F/K$ finite.
1. If $F/K$ is separable, then $F/K$ is simple.
2. (Artin) More generally, $F/K$ is simple if and only if there are only finitely many intermediate fields.
>[!proof]-
>Recall that GTM73's proof of the fact that if $K$ is infinite and $F/K$ is separable and finite then $F/K$ is simple was to show that if $F/K$ is separable and finite then $F/K$ only has finitely many intermediate fields, which doesn't use the hypothesis $K$ infinite, and then to show that if $F/K$ only has finitely many intermediate fields and $K$ is infinite, then $F/K$ is simple. Thus it suffices to prove Artin's generalization. Since 2 is trivial when $K$ is finite, we may assume that $K$ is infinite.
>Now it remains to show that if $F/K$ is simple, then $F/K$ only has finitely many intermediate fields. Suppose $F=K(u)$ with $u$ algebraic over $K$. Let $E$ be an intermediate field and $g\in E[x]$ the minimal polynomial of $u$ over $E$. If $g=sum_{i=0}^{n-1}a_ix^i+x^n$, then $[F:E]=n$.
>*Claim.* $E=K(a_0,\dots,a_{n-1})=:L$. Clearly $F=L(u)$. Suppose the minimal polynomial of $u$ over $L$ is $f$, then $g\mid f$. Since $g\in L[x]$ and $f$ is irreducible in $L[x]$, we must have $g=f$. So $[F:L]=[F:E]$ and hence $L=E$.
>Thus we have proved that *every intermediate field of $K(u)$ is the extension of $K$ by the coefficient of the minimal polynomial of $u$ over $K$*. But these polynomials divide the minimal polynomial over $u$ over $K$ and hence are finite.

#### 6.4 Some Other Results
1. $F/K$. If $u\in F$ is separable over $K$ and $v\in F$ is purely inseparable over $K$, then $K(u,v)=K(u+v)$. If $u\neq0$, $v\neq0$, then $K(u,v)=K(uv)$.
2. If $\mathrm{char}\,K=p>0$ and $a\in K-K^p$, then $x^{p^n}-a\in K[x]$ is irreducible for every $n>1$.
3. If $f\in K[x]$ is monic irreducible, $\mathrm{deg}\,f\geq2$ and $f$ has all its roots equal, then $\mathrm{char}\,K=p\neq0$ and $f=x^{p^n}-a$ for some $n\geq1$ and $a\in K$.
4. Let $F/K$ algebraic, $S$ and $P$ separable and purely inseparable closures, and $E$ an intermediate field.
	1. $F/E$ is purely inseparable if and only if $S\subset E$.
	2. If $F/E$ is separable, then $P\subset E$.
	3. If $E\cap S=K$, then $E\subset P$.
5. TFAE. And such a field is said to be **perfect.** Every finite field is perfect.
	1. Every irreducible polynomial in $K[x]$ is separable.
	2. The algebraic closure $\bar{K}$ of $K$ is Galois over $K$.
	3. Every algebraic extension field of $K$ is separable over $K$.
	4. Either $\mathrm{char}\,K=0$ or $\mathrm{char}\,K=p$ and $K=K^p$.
### 7. Special Extensions
#### 7.1 Norm and Trace
$F/K$ finite and $\bar{K}$ an algebraic closure of $K$ containing $F$. Let $\sigma_1,\dots,\sigma_r$ be all the distinct $K$-monomorphisms $F\rightarrow \bar{K}$. (By previous sections, $r=[F:K]_s$.) If $u\in F$, the **norm** of $u$, denoted $N_{F/K}(u)$ is the element$$N_{F/K}(u):=\prod_{i=1}^r\sigma_i(u)^{[F:K]_i}.$$The **trace** of $u$, denoted $T_{F/K}(u)$, is the element$$T_{F/K}(u):=[F:K]_i\sum_{i=1}^r\sigma_i(u).$$**Remark.** Next we show that these are independent of $\bar{K}$ and one can replace $\bar{K}$ with the normal closure of $F/K$. Also notice that the definition of $T_{F/K}$ is somewhat confusing and **$T_{F/K}=0$ if $F/K$ is not separable**. But we will see later that the coefficient $[F:K]_i$ is introduced for a good reason, because proofs then would be very smooth and equations would work regardless of characteristic (for example, for any $u\in K$, $T_{F/K}(u)=[F:K]u$ and $N_{F/K}(u)=u^{[F:K]}$), although this somewhat *blurs what is really happening* and I personally don't like it very much. Now let's introduce them in a natural way.
Recall the thought of the proof of $r=[F:K]_s$, that a $K$-monomorphism $F\rightarrow \bar{K}$ is a choice of root and $[F:K]_s$ is the number of choices. Also recall that in the separable case, elementary symmetric polynomials of roots in fact lie in $K$. To be precise, let's assume that $F=K(u)$ with $f\in K[x]$ the minimal polynomial of $u$ over $K$ and suppose $\mathrm{char}\,K=p>0$. Then in the splitting field of $f$ over $K$, as we have shown above, $f$ splits as$$f=\prod_{i=1}^r(x^{p^m}-u_i^{p^m}),$$where $u_i$ are distinct roots of $f$, $r=[K(u):K]_r$, $p^m=[K(u):K]_i$ and $\mathrm{deg}\,f=rp^m$. So the coefficients of $x^k$ if $f$ is 0 if $p^m\nmid k$; and otherwise the $k/p^m$-th elementary symmetric polynomial of $u_i^{p^m}$. So we should be putting $p^m$ power on $u$. Equivalently, we should replace $F$ by the separable closure of $F/K$. Actually, the latter method is more reasonable, because then the trace does not vanish. One might want to remove $[F:K]_i$ from the definition of the trace, but then the problem would be that for $u\notin F-F^{p^m}$, its trace may not lie in $K$.
By Newton's identities, all other elementary symmetric polynomials of $u_i^{p^m}$ can be expressed as polynomials of $\sum_iu_i^{kp^m}$. So it's possible to study only the trace with $F$ replaced by the separable closure $S$, which is more reasonable because $T_{S/K}$ is $K$-linear, and lie in the dual space of $S$ as a $K$-linear space, i.e. $\mathrm{Hom}_K\,(S,K)$. But we also want to include the norm, because it is multiplicative and can be useful even when $F/K$ is not separable.
Above we have introduced trace and norm by focusing the element $u$, but they're defined in more general cases and we can consider trace and norm of any element in $F$. From the view point that they characterize the extension $F/K$, we continue our discussions.
**Theorem.** $F/K$ finite and Galois and $Gal(F/K)=\{\sigma_1,\dots,\sigma_n\}$. Then for any $u\in F$,$$
\begin{align}
N_{F/K}(u)&=\prod_{i=1}^n\sigma_i(u),\\
T_{F/K}(u)&=\sum_{i=1}^n\sigma_i(u).
\end{align}
$$
>[!proof]-
>Just notice that $[F:K]_i=$, $F/K$ is normal and the $K$-monomorphisms $F\rightarrow\bar{K}$ are precisely the elements of $Gal(F/K)$.

From the theorem, we see clearly that trace and norm are fixed by $Gal(F/K)$ and hence they lie in $K$. Next we show that this is true even if $F/K$ is not Galois.
**Theorem.** $F/K$ finite, $u\in F$.
1. $N_{F/K}$ is multiplicative and $T_{F/K}$ is additive.
2. If $u\in K$, then $N_{F/K}(u)=u^{[F:K]}$ and $T_{F/K}(u)=[F:K]u$.
3. $N_{F/K}(u), T_{F/K}(u)\in K$. More precisely,$$
\begin{align}
N_{F/K}(u)&=((-1)^na_0)^{[F:K(u)]}\in K,\\
T_{F/K}(u)&=-[F:K(u)]a_{n-1}\in K,
\end{align}
$$where $f=\sum_ia_ix^i+x^n$ is the minimal polynomial of $u$.
4. If $E$ is an intermediate field, then$$
\begin{align}
N_{E/K}(N_{F/E}(u))&=N_{F/K}(u),\\
T_{E/K}(T_{F/E}(u))&=T_{F/K}(u).
\end{align}
$$
>[!proof]-
>1&2 are trivial.
>For 3, let $E=K(u)$. Then the distinct $K$-monomorphisms $F\rightarrow\bar{K}$ are precisely the maps $\sigma_k\tau_j\;(1\leq k\leq t;1\leq j\leq s)$, where the $\sigma$'s are elements in $Gal(\bar{K}/K)$ whose restrictions to $E$ are distinct and the $\tau$'s are all distinct $E$-monomorphisms $F\rightarrow \bar{K}$. (Think of this as breaking down the process of choosing roots for $F/K$ into two iterated choices $E/K$ and $F/E$.) Thus $t=[E:K]_s$ and $n=[E:K]=t[E:K]_i$. Also $s=[F:E]_s$, $r=[F:K]_s=st$ and $[F:K]_is=[F:E]_i[E:K]_i[F:E]_s=[F:E][E:K]_i$
>Then $N_{F/K}(u)=\prod_{k=1}^t\sigma_k(u)^{[F:E][E:K]_i}$ and $T_{F/K}(u)=[F:E][E:K]_i\sum_{k=1}^t\sigma_k(u)$. Also, $\sigma_k(u)\;(1\leq k\leq t)$ are all distinct roots of $f$. So$$f=\prod_{k=1}^t(x-\sigma_k(u))^{[E:K]_i}=\Big[x^t-\big(\sum_{k=1}^t\sigma_k(u)\big)x^{t-1}+\cdots+\big((-1)^t\prod_{k=1}^t\sigma_k(u)\big)\Big].$$If $[E:K]_i=1$, then $n=t$ and the conclusion is immediate. If $[E:K]_i>1$, then it's easy to calculate $a_0$ and to see that $a_{n-1}=0=T_{F/K}(u)$.
>Finally, using the same notion above, with $E$ any intermediate field, we can prove 4.

Now consider $F/K$, with $u\in F$ algebraic over $K$ and let $f$ be its minimal polynomial. $u$ induces a $K$-linear homomorphism $T_u:F\rightarrow F$ given by $T_u(v)=uv$. Clearly $g(u)=0$ if and only if $g(T_u)=0$, so the minimal polynomial $T_u$ is also $f$. This is unusual, since the minimal polynomial of a linear map is not necessarily irreducible in general. Let $v_1,\dots,v_m$ be a basis of $F/K(u)$, then $F=\oplus_iK(u)v_i$ and each subspace is $T_u$-acyclic with minimal polynomial (of $T_u|_{K(u)v_i}$) being $f$. So the invariant factors of $T_u$ are $f\mid f\mid\cdots\mid f$ ($m$ of them) and the characteristic polynomial of $T_u$ is $f^m$, with $m=[F:K(u)]$. So by the theorem above, we have$$
\begin{align}
N_{F/K}(u)&=\mathrm{det}\,T_u,\\
T_{F/K}(u)&=\mathrm{tr}\,T_u.
\end{align}
$$
#### 7.2 Cyclic Extension
Let $S$ be a nonempty set of automorphisms of $F$. Then $S$ is **linearly independent** provided that for any $a_1,\dots,a_n\in F$ and $\sigma_1,\dots,\sigma_n\in S\;(n\geq1)$:$$\forall u\in F\;\;\sum_{i=1}^na_i\sigma_i(u)=0\implies\forall i\;\;a_i=0.$$**Lemma.** Every set of distinct automorphisms of $F$ is linearly independent.
>[!proof]-
>Choose one dependence relation with $n$ minimal, all $a_i\neq0$; clearly $n>1$.$$\sum_{i=1}^na_i\sigma_i(u)=0,\;\;\forall u\in F.$$Since $\sigma_1$ and $\sigma_2$ are distinct, there exists $v\in F$ with $\sigma_1(v)\neq\sigma_2(v)$. Then$$\sum_{i=1}^na_i\sigma_i(u)\sigma_i(v)=0,$$and$$\sum_{i=1}^na_i\sigma_i(u)\sigma_1(v)=0.$$The difference$$\sum_{i=2}^na_i[\sigma_i(v)-\sigma_1(v)]\sigma_i(u)=0,\;\;\forall u\in F$$is a relation with smaller length but since $a_2\neq0$ and $\sigma_2(v)\neq\sigma_1(v)$ this new relation is nontrivial. This contradicts the choice of $n$.

$F/K$ is **cyclic** (resp. **abelian**) if $F/K$ is algebraic and Galois and $Gal(F/K)$ is a cyclic (resp. abelian) group. If in this situation $Gal(F/K)$ is a finite cyclic group of order $n$, then $F/K$ is said to be a **cyclic extension of degree $n$**. For example, we have shown that every finite extension of a finite field is cyclic.
**Theorem.** $F/K$ cyclic of degree $n$, $Gal(F/K)=\langle\sigma\rangle$ and $u\in $F$$.
1. $T_{F/K}(u)=0$ if and only if $u=v-\sigma(v)$ for some $v\in F$.
2. (*Hilbert's Theorem 90*) $N_{F/K}(u)=1_K$ if and only if $u=v\sigma(v)^{-1}$ for some nonzero $v\in F$.
>[!proof]-
>$T(u)=\sum_{i=0}^{n-1}\sigma^iu$ and $N(u)=\prod_{i=0}^{n-1}\sigma^iu$.
>1. If $u=v-\sigma(v)$, then since $T(\sigma v)=T(v)$, we have $T(u)=0$. Conversely, suppose $T(u)=0$. Choose $w\in F$ such that $T(w)=1_K$ as follows. By the lemma, there exists $z\in F$ such that $0\neq\sum_{i=1}^{n-1}\sigma^iz=T(z)$. Since $T(z)\in K$, if $w=T(z)^{-1}z$, then $T(w)=T(z)^{-1}T(z)=1_K$. Now let $$v=\sum_{i=0}^{n-2}\sigma^iw\sum_{j=0}^{i}\sigma^ju.$$ Since $T(u)=0$, we have $u=-\sum_{i=1}^{n-1}\sigma^iu$ and hence $$
>\begin{align}
>v-\sigma v&=\sum_{i=1}^{n-1}u\sigma^iw\\
>&=uT(w)\\&=u.
>\end{align}
>$$
>2. If $u=v\sigma(v)^{-1}$, then clearly $N(u)=1$. Conversely, suppose $N(u)=1$, which implies $u\neq0$. There exists $y\in F$ such that $$v=\sum_{i=0}^{n-1}\sigma^iy\prod_{j=0}^i\sigma^jy\neq0.$$Since the last summand of $v$ is $N(u)\sigma^{n-1}y=\sigma^{n-1}y$, it is easy to verify that $u^{-1}v=\sigma v$, whence $u=v\sigma(v)^{-1}$ ($\sigma(v)\neq0$ since $v\neq0$ and $\sigma$ is injective).

**Proposition.** $F/K$ is cyclic of degree $n=mp^t$ where $0\neq p=\mathrm{char}\,K$ and $(m,p)=1$. Then there exists a chain of intermediate fields $K\subset E_t\subset \cdots\subset E_0\subset F$ such that $F/E_0$ is cyclic of degree $m$ and for each $0\leq i\leq t$, $E_{i-1}/E_i$ is cyclic of degree $p$.
>[!proof]-
>By the Fundamental Theorem, for every intermediate field $E$, $F/E$ and $E/K$ are cyclic. It follows that for any intermediate fields $L\subset M$, $M/L$ is cyclic.
>Let $H$ be the unique subgroup of order $m$ and let $E_0=H'$. Then $F/E_0$ is cyclic of degree $m$ and $E_0/K$ is cyclic of degree $p^t$. Since $Gal(E_0/K)$ is cyclic of order $p^t$ it has a chain of subgroups$$1=G_0<G_1<G_2<\cdots<G_t=Gal(E_0/K)$$with $\#G_i=p^i$, $[G_i:G_{i-1}]=p$ and $G_i/G_{i-1}$ cyclic of order $p$. For each $i$ let $E_i$ be the fixed field of $G_i$ relative to $E_0$ and $Gal(E_0/K)$. The Fundamental Theorem then implies that
>1. $E_0\supset E_1\supset\cdots\supset E_t=K$,
>2. $[E_{i-1}:E_i]=[G_i:G_{i-1}]=p$, and
>3. $Gal(E_{i-1}/E_i)\cong G_i/G_{i-1}$.
>
>Therefore $E_{i-1}/E_i$ is cyclic of degree $p$ for $0\leq i\leq t-1$.

Let $F/K$ be a cyclic extension of degree $n$. Then by the proposition, we may restrict our attention to just **two cases**:
1. $n=\mathrm{char}\,K=p>0$, and
2. $\mathrm{char}\,K=0$ or $\mathrm{char}\,K=0>0$ and $(p,n)=1$.

For the fist case, we have:
**Proposition.** $\mathrm{char}\,K=p>0$, then $F/K$ is cyclic of degree $p$ if and only if there exists an *irreducible* polynomial $x^p-x-a\in K[x]$ such that $F$ is its splitting field. In this case $F=K(u)$ where $u$ is any root of $x^p-x-a$. (Key: $$u^p-u-a=0\implies \forall i\in\mathbb{F}_p\;\;(u+i)^p-(u+i)-a=0,$$so $x^p-x-a$ either splits or is irreducible both in $F$ and in $K$.)
>[!proof]-
>($\Rightarrow$) Let $\sigma$ be the generator of $Gal(F/K)$, then $T_{F/K}(1)=[F:K]=0$, whence $1=v-\sigma(v)$ for some $v\in F$. If $u=-v$, then $\sigma(u)=u+1\neq u$, whence $u\notin K$. Since $[F:K]=p$, there are no intermediate fields, and we must have $F=K(u)$. Note that $\sigma(u)^p=u^p+1$, and hence $\sigma(u^p-u)=u^p-u=a\in K$. Therefore, $u$ is a root of $x^p-x-a\in K[x]$, which is necessarily the irreducible polynomial of $u$ over $K$ since the degree of $u$ over $K$ is $p$.
>Since $u$ is a root of $x^p-x-a$, we have for each $i\in \mathbb{F}_p$: $(u+i)^p-(u+i)-a=u^p-u-a=0$ since $i^p=i$. Thus $u+i\in K(u)=F$ is a root of $x^p-x-a$ for each $i\in \mathbb{F}_p$, whence $F$ contains $p$ distinct roots of $x^p-x-a$ and must be its splitting field. Finally if $u+i$ is any root of $x^p-x-a$, then clearly $K(u+i)=K(u)=F$.
>($\Leftrightarrow$) Suppose $F/K$ is the splitting field of $x^p-x-a\in K[x]$ over $K$. We shall not assume that $x^p-x-a$ is irreducible and shall prove somewhat more than is stated in the theorem. If $u$ is a root of $x^p-x-a$, then the preceding paragraph shows that $K(u)$ contains $p$ distinct roots of $x^p-x-a$: $u, u+1, \dots,u+(p-1)\in K(u)$. So $F=K(u)$, the irreducible factors of $x^p-x-a$ are separable and $F/K$ is Galois. Every $\ta\in Gal(F/K)$ is completely determined by $\tau(u)$ and $\tau(u)=u+i$ for some $i\in \mathbb{F}_p$. Verify that the assignment $\tau\mapsto i$ defines a monomorphism of groups $\theta:Gal(F/K)\rightarrow \mathbb{Z}/p$. Consequently, $Gal(F/K)\cong\mathrm{im}\,\theta$ is either $1$ or $\mathbb{Z}/p$. If $Gal(F/K)=1$, then $F=K$, whence $u\in K$ and $x^p-x-a$ splits in $K[x]$. Thus if $x^p-x-a$ is irreducible over $K$, we must have $Gal(F/K)\cong \mathbb{Z}/p$. In this case, therefore, $F/K$ is cyclic of degree $p$.

In order to determine the structure of the second case, it will be necessary to introduce an additional assumption on the base field $K$.
Let $K$ be a field and $n\in\mathbb{N}$, an element $\zeta\in K$ is said to be an **$n$-th root of unity** provided $\zeta^n=1_K$. It is easy to see that the set of all $n$-th roots of unity in $K$ form a multiplicative subgroup of $K^*$. This subgroup is cyclic by one of the first lemmas in 5.1 and has order at most $n$. $\zeta\in K$ is said to be a **primitive $n$-th root of unity** provided $\zeta$ is an $n$-th root of unity and $\zeta$ has order $n$. In particular, a primitive $n$-th root of unity generates the cyclic group of all $n$-th roots of unity.
**Remark.** If $\mathrm{char}\,K=p$ and $p\mid n$, then $n=p^km$ with $(p,m)=1$ and $m<n$. Thus $x^n-1=(x^m-1)^{p^k}$. Consequently the $n$-th roots of unity in $K$ coincides with the $m$-th roots of unity in $K$. Since $m<n$, there can be no primitive $n$-th root of unity in $K$. But since $(x^m-1)'=mx^{m-1}\neq0$, $x^m-1$ has no multiple roots. So **there exists an $n$-th root of unity in some extension field of $K$ if and only if $p\nmid n$ or $\mathrm{char}\,K=0$**.
The following lemma is easy.
**Lemma.** $n\in\mathbb{N}$ and $K$ contains a primitive $n$-th root of unity $\zeta$.
1. If $d\mid n$, then $\zeta^{n/d}=:\eta$ is a primitive $d$-th root of unity in $K$.
2. If $d\mid n$ and $u\neq0$ (not necessarily in $K$) is a root of $x^d-a\in K[x]$, then $x^d-a$ has $d$ distinct roots, namely $u,u\eta,\dots,u\eta^{d-1}$, where $\eta\in K$ is a primitive $d$-th root of unity. Furthermore, $K(u)$ is a splitting field of $x^d-a$ over $K$ and $K(u)/K$ is Galois.

**Theorem.** $n\in\mathbb{N}$, $F/K$ and $K$ is a field containing a primitive $n$-th root of unity $\zeta$. Then TFAE.
1. $F/K$ is cyclic of degree $d$, where $d\mid n$.
2. $F$ is the splitting field over $K$ of a polynomial (which is *not* necessarily irreducible) of the form $x^n-a\in K[x]$ (in which case $F=K(u)$, for any root $u$ of $x^n-a$).
3. $F$ is the splitting field over $K$ of an irreducible polynomial of the form $x^d-b\in K[x]$, where $d\mid n$ (in which case $F=K(v)$, for any root $v$ of $x^d-b$).
>[!proof]-
>(1 $\Rightarrow$ 2) Key: for any $\sigma\in Gal(F/K)$, $\sigma(u)=\zeta^iu$ for some $i\;(0\leq i\leq n-1)$, and the assignment $\sigma\mapsto\zeta^i$ defines a monomorphism $Gal(F/K)\rightarrow\langle\zeta\rangle\cong\mathbb{Z}/n$.
>(1 $\Rightarrow$ 3) Let $\eta=\zeta^{n/d}$. Since $N_{F/K}(\eta)=\eta^{[F:K]}=\eta^d=1$, $\eta=w\sigma(w)^{-1}$ for some $w\in F$. If $v=w^{-1}$, then $\sigma(v)=\eta v$ and $\sigma(v^d)=v^d=b\in K$. Then $K(v)\subset F$ and $K(v)$ is a splitting field of $x^d-b$ over $K$ by the lemma above. Furthermore, for each $i\;(0\leq i\leq d-1)$, $\sigma^i(v)=\eta^iv$ so that $\sigma^i:K(v)\cong K(\eta^iv)$. Consequently, $x^d-b$ is irreducible since $v$ and $\eta^iv$ have the same minimal polynomial. Therefore $[K(v):K]=d=[F:K]$, whence $F=K(v)$.
>(3 $\Rightarrow$ 2) $v^d-b=0\in K$ implies that $F=K(v)$. Now $(\eta v)^n=b^{n/d}=a\in K$ and $\zeta v$ is a root of $x^n-a\in K[x]$. Then $K(\zeta v)$ is a splitting field of $x^n-a$ over $K$. But $\zeta\in K$ implies that $F=K(v)=K(\zeta v)$.

**Remark.** What is really happening here is that if $K$ contains a primitive $n$-th root of unity, then for any $a\in K[x]$, by introducing any $n$-th root $u$ of $a$ we splits $x^n-a$, and the resulting extension is a cyclic of degree $d$, where $d$ is the smallest positive integer such that $u^d\in K$ and $x^d-u^d\in K[x]$ is the minimal polynomial of $u$ over $K$. And for the other direction, just memorize (1 $\Rightarrow$ 3).

However, it's considerably more difficult to characterize the splitting field of $x^n-a\in K[x]$ when $K$ does not contain a primitive $n$-th root of unity. The case when $a=1$ is considered in the next section.
#### 7.3 Cyclotomic Extension
In this section, we examine splitting fields of $x^n-1$, in particular with base field $\mathbb{Q}$. A splitting field $F$ of $x^n-1\in K[x]$ over $K$ is called a **cyclotomic extension of order $n$**. If $\mathrm{char}\,K=p>0$ and $n=mp^t$ with $(m,p)=1$, then $x^n-1=(x^m-)^{p^t}$, and hence we shall assume that $\mathrm{char}\,K=0$ or relatively prime to $n$.
Recall the Euler function $\varphi(n):=\#\{k\,:\,1\leq k\leq n,(k,n)=1\}$.
1. $1\leq m\leq n$, then $m$ is a unit mod $n$ if and only if $(m,n)=1$, so the multiplicative group of $\mathbb{Z}/n$ has order $\varphi(n)$.
2. If $p$ is prime and $n>0$, then $\varphi(p^n)=p^{n-1}(p-1)$.
3. If $(m,n)=1$, then $\varphi(mn)=\varphi(m)\varphi(n)$.
4. If $n=p_1^{k_1}\cdots p_r^{k_r}$ is the factorization of $n$, then $\varphi(n)=n\prod_{i=1}^r(1-1/p_i)$.
5. $\sum_{d\mid n}\varphi(d)=n$.
6. $\varphi(n)=\sum_{d\mid n}d\mu(n/d)$, where $\mu$ is the Moebius function.
TBD
#### 7.4 Radical Extension
TBD
#### 7.5 Appendix: The General Equation of Degree $n$
#### 7.6 Some Other Results
1. Let $v\in\bar{\mathbb{Q}}-\mathbb{Q}$, and let $E$ be a subfield of $\bar{\mathbb{Q}}$ maximal with respect to the condition $v\notin E$, then $E$ and every finite extension of $E$ is cyclic.
2. Let $\sigma$ be in the absolute Galois group $Gal(\bar{K}/K)$ and $F$ its fixed field, then $F$ and every finite extension of $F$ is cyclic.
3. If $\mathrm{char}\,K=p>0$, let $K_p:=\{u^p-u\,:\,u\in K\}$. Using trace, we can show that:
	1. A cyclic extension field $F$ of $K$ of degree $p$ exists if and only if $K\neq K_p$.
	2. If there exists a cyclic extension of degree $p$ of $K$, then there exists a cyclic extension of degree $p^n$ for every $n\geq1$.
4. If $F/\mathbb{Q}$ is finite, then $F$ contains only a finite number of roots of unity.
5. Let $p$ be a prime and assume either $\mathrm{char}\,K=p$ or $\mathrm{char}\,K\neq p$ and $K$ contains a primitive $p$-th root of unity. Then $x^p-a\in K[x]$ is either irreducible or splits in $K[x]$.
6. If $\mathrm{char}\,K=p>0$, then for any root $u$ of $x^p-a\in K[x]$, $K(u)\neq K(u^p)$ if and only if $[K(u):K]=p$.
### 8. Transcendental Extensions
#### 8.1 Basics
$F/K$ and $S\subset F$. $S$ is **algebraically dependent** over $K$ if for some $n\in\mathbb{N}$, there exists a nonzero polynomial $f\in K[x_1,\dots,x_n]$ such that $f(s_1,\dots,s_n)=0$ for some distinct $s_1,\dots,s_n\in S$. $S$ is **algebraically independent** over $K$ if $S$ is *not* algebraically dependent over $K$. The following tip will be used later.
>[!tip] Algebraic Independence Criterion
>$S$ is algebraic independent over $K$ if and only if the set $M(S)$ of monomials in elements of $S$ is linearly independent over $K$.

**Theorem.** $F/K$ and $\{s_1,\dots,s_n\}\subset F$ algebraically independent over $K$, then there's a $K$-isomorphism $K(s_1,\dots,s_n)\cong K(x_1,\dots,x_n)$.
**Corollary.** For $i=1,2$, $F_i/K_i$ and $S_i\subset F_i$ with $S_i$ algebraically independent over $K_i$. If $\varphi:S_1\rightarrow S_2$ is injective and $\sigma:K_1\rightarrow K_2$ is a monomorphism, then $\sigma$ extends to a monomorphism $\bar{\sigma}:K_1(S_1)\rightarrow K_2(S_2)$ such that $\bar{\sigma}(s)=\varphi(s)$ for every $s\in S_1$. Furthermore if $\varphi$ is bijective and $\sigma$ is an isomorphism, then $\bar{\sigma}$ is an isomorphism. In particular, every permutation of an algebraically independent set $S$ over a field $K$ extends to a $K$-automorphism of $K(S)$.

A **transcendence base** of $F/K$ is a subset $S$ of $F$ which is algebraically independent over $K$ and is maximal in the set of all algebraically independent subsets of $F$.
The existence of a transcendence base follows by a standard Zorn's lemma argument. It's easy to show that $\{x\}$ is a transcendence base of $K(x)/K$.
**Theorem.** $F/K$, $S\subset F$ algebraically independent over $K$, and $u\in F-K(S)$. Then $S\cup\{u\}$ is algebraically independent over $K$ if and only if $u$ is transcendental over $K(S)$.
**Corollary.** $F/K$, $S\subset F$ algebraically independent over $K$. Then $S$ is a transcendence base of $F$ over $K$ if and only if $F/K(S)$ is algebraic.
$F/K$ is called **purely transcendental** if $F=K(S)$, where $S\subset F$ and $S$ is algebraically independent over $K$. In this case $S$ is necessarily a transcendence base of $F$ over $K$ by the corollary. If $F$ is an arbitrary extension field of $K$, et $S$ be a transcendence base of $F/K$ and let $E=K(S)$. Then the corollary shows that $F/E$ is algebraic and $E/K$ is purely transcendental. Finally, $F/K$ is algebraic if and only if the null set is a transcendence base of $F/K$. In this case the null set is clearly the unique transcendence base of $F/K$.
**Corollary.** $F/K$ and $F/K(X)$ is algebraic for some $X\subset F$ (in particular, if $F=K(X)$), then $X$ contains a transcendence base of $F/K$.
(Show that a maximal algebraically independent subset $S$ of $X$ exists, then show that $K(X)/K(S)$ is algebraic and hence $F/K(S)$ is algebraic, and the conclusion follows.)

Analogous to linear independence, we prove that the cardinality of any two transcendental bases are identical in two steps.
**Theorem.** $F/K$. If $S$ is a finite transcendence base of $F/K$, then every transcendence base of $F/K$ has the same number of elements as $S.
>[!proof]-
>Let $S=\{s_1,\dots,s_n\}$ and let $T$ be any transcendence base. We claim that some $t_1\in T$ is transcendental over $K(s_2,\dots,s_n)$. Otherwise every element of $T$ is algebraic over $K(s_2,\dots,s_n)$, whence $K(s_2,\dots,s_n)(T)/K(s_2,\dots,s_n)$ is algebraic. Since $F/K(T)$ is algebraic, $F$ is necessarily algebraic over $K(T)(s_2,\dots,s_n)=K(s_2,\dots,s_n)(T)$. Therefore $F/K(s_2,\dots,s_n)$ is algebraic. In particular $s_1$ is algebraic over $K(s_2,\dots,s_n)$, which is a contradiction. Hence some $t_1\in T$ is transcendental over $K(s_2,\dots,s_n)$ and $\{t_1,s_2,\dots,s_n\}$ is algebraically independent.
>Now if $s_1$ were transcendental over $K(t_1,s_2,\dots,s_n)$, then $\{t_1,s_1,s_2,\dots,s_n\}$ would be algebraically independent, which contradicts the hypothesis on $S$. Therefore, $s_1$ is algebraic over $K(t,s_2,\dots,s_n)$ and $F/K(t_1,s_2,\dots,s_n)$ is algebraic. Hence $\{t_1,s_2,\dots,s_n\}$ is a transcendence base of $F/K$.
>Repeatedly using the argument above, we eventually obtain $t_1,t_2,\dots,t_n\in T$ such that $\{t_1,\dots,t_n\}$ is a transcendence base of $F/K$. Clearly we must have $T=\{t_1,\dots,t_n\}$ and hence $\#S=\#T$.

**Theorem.** $F/K$. If $S$ is an infinite transcendence base of $F/K$, then every transcendence base of $F/K$ has the same cardinality as $S$.
(See GTM73, VI.1.10 for a proof.)
So for any $F/K$, the **transcendence degree** of it is the cardinal number of any transcendence base of it, and is denoted $\mathrm{tr.d.}\,F/K$.
We have shown that $\mathrm{tr.d.}\,F/K$ is independent of the choice of $S$. Obviously, $\mathrm{tr.d.}\,F/K\leq[F:K]$ and $\mathrm{tr.d.}F/K=0$ if and only if $F/K$ is algebraic.

**Theorem.** $F/E/K$.$$\mathrm{tr.d.}\,F/K=\mathrm{tr.d.}\,F/E+\mathrm{tr.d.}\,E/K.$$(Just show that if $S$ is a transcendence base of $F/E$ and $T$ is a transcendence base of $E/K$, then $S\cup T$ is a transcendence base of $F/K$.)

**Theorem.** Let $F_1$ (resp. $F_2$) be an algebraically closed field extension of $K_1$ (resp. $K_2$). If $\mathrm{tr.d.}\,F_1/K_1=\mathrm{tr.d.}\,F_2/K_2$, then every isomorphism $K_1\cong K_2$ extends to an isomorphism $F_1\cong F_2$.
(Reduce to the purely transcendental and algebraic case, which have been proved.)
#### 8.2 Some Other Results
1. (Exchange property.) $S\subset F$. If $u\in F$ is algebraic over $K(S)$ and $u$ is not algebraic over $K(S-\{v\})$, where $v\in S$, then $v$ is algebraic over $K((S-\{v\})\cup\{u\})$.
2. $\{x_1,\dots,x_n\}$ is a transcendence base of $K(x_1,\dots,x_n)$.
3. Let $E_1,E_2$ be intermediate fields of $F/K$, then$$\mathrm{max}\,\big(\mathrm{tr.d.}\,E_1/K,\mathrm{tr.d.}\,E_2/K\big)\leq\mathrm{tr.d.}\,E_1E_2/K\leq\mathrm{tr.d.}\,E_1/K+\mathrm{tr.d.}\,E_2/K.$$
4. If $F/K$ is finitely generated, then for any intermediate field $E$, $E/K$ is finitely generated.
5. Here're some results about $\mathbb{C}/\mathbb{Q}$.
	1. $\mathrm{tr.d.}\,\mathbb{C}/\mathbb{Q}=\#\mathbb{C}$.
	2. The absolute Galois group $Gal(\mathbb{C}/\mathbb{Q})$, i.e. all automorphisms of $\mathbb{C}$, is infinite.
6. $F/E/K$, $F$ is algebraically closed. If $\mathrm{tr.d.}\,E/K<\infty$, then any $K$-monomorphism $E\rightarrow F$ extends to a $K$-automorphism of $F$.
7. $F/K$, $F$ is algebraically closed. If $\mathrm{tr.d.}\,F/K<\infty$, then every $K$-monomorphism $F\rightarrow F$ is in fact an automorphism.
### 9. Generalized Characterization of Separability
Through out this section, let $C$ be an algebraically closed field with subfield $K,E,F$ such that $K\subset E\cap F$.
#### 9.1 Linear Disjointness
Consider the subring $E[F]=F[E]$ generated by $E$ and $F$ as a vector space over $K$. We say that $E$ and $F$ are **linearly disjoint** over $K$ if and only if the $K$-linear transformation $E\otimes_KF\rightarrow E[F]$ given by $a\otimes b\rightarrow ab$ is an isomorphism. This is clearly surjective.
**Lemma.** $E$ and $F$ are linearly disjoint over $K$ if and only if every subset of $E$ which is linearly independent over $K$ is also linearly independent over $F$.
>[!proof]-
>Suppose $E$ and $F$ are linearly disjoint over $K$, and $e_1,\dots,e_n\in E$ are linearly independent over $K$. For any $f_1,\dots,f_n\in F$ such that $\sum_if_ie_i=0$, by linearly disjointness, $\sum_ie_i\otimes f_i=0\in E\otimes_KF$. Recall that there are finitely generated $K$-subspaces $E_0\subset E$ and $F_0\subset F$ such that $\sum_ie_i\otimes f_i=0\in E_0\otimes_KF_0$. Let $f'_j$ be a set of basis of $F_0$ over $K$ and write $f_i=\sum_ja_{ij}f'_j$ with $a_{ij}\in K$. Then $\sum_i\sum_ja_{ij}e_i\otimes f'_j=0$ implies that for all $j$, $\sum_ia_{ij}e_i=0$. But $e_i$ are linearly independent over $K$, so for all $i,j$, we have $a_{ij}=0$. Therefore $f_i=0$ for all $i$ and $e_1,\dots,e_n$ are linearly independent over $F$.
>Conversely, suppose we have $\sum_ie_if_i=0$ with $e_i\in E$ and $f_i\in F$. WLOG, suppose $e_1,\dots,e_r$ are linearly independent over $K$ and $e_i=\sum_{j=1}^ra_{ij}e_j$ for $r+1\leq i\leq n$. Then $\sum_{j=1}^r(f_j+\sum_{i=r+1}^na_{ij}f_i)e_j=0$. By hypothesis, $e_1,\dots,e_r$ are also linearly independent over $F$, so for all $1\leq j\leq r)$, we have $f_j+\sum_{i=r+1}^na_{ij}f_i=0$. Consequently, $\sum_{j=1}^ne_j\otimes f_j=\sum_{j=1}^re_j\otimes(f_j+\sum_{i=r+1}^na_{ij}f_i)=0$.

Observe that if $K\subset E$, then $E$ and $K$ are trivially linearly disjoint over $K$. This fact will be repeatedly used.
**Lemma.** Let $R$ be a subring of $E$ such that $K(R)=E$ and $K\subset R$ (which implies that $R$ is a vector space over $K$). Then TFAE.
1. $E$ and $F$ are linearly disjoint over $K$.
2. Every subset of $R$ that is linearly independent over $K$ is also linearly independent over $F$.
3. There exists a basis of $R$ over $K$ which is linearly independent over $F$.
>[!proof]-
>(1 $\Rightarrow$ 2) and (2 $\Rightarrow$ 3) are trivial.
>(3 $\Rightarrow$ 2) Let $r_1,\dots,r_n\in R$ be linearly independent over $K$, then there are $s_1,\dots,s_m$ with $m\geq n$ from the basis such that $r_i=\sum_ja_{ij}s_j$ with $a_{ij}\in K$. For any $f_1,\dots,f_n\in F$ such that $\sum_ir_if_i=0$, we have $\sum_i\sum_ja_{ij}s_jf_i=0$. Then since the basis is linearly independent over $F$, we have $\sum_ia_{ij}f_i=0$ for all $1\leq j\leq m$. Since $s_j$ are linearly independent over $K$, the $n\times m$ matrix $(a_ij)$ with coefficients in $K$ has rank $n$ and admits a right inverse. So $f_i=0$ for $1\leq i\leq n$ and $r_1,\dots,r_n$ are linearly independent over $F$.
>(2 $\Rightarrow$ 1) Now we use the hypothesis that every element in $E$ can be written as rational functions of elements in $R$ with coefficients in $K$. Suppose $e_1,\dots,e_n\in E$ are linearly independent over $K$. Since $R$ is the subring of a field and hence must be an integral domain, we can multiply by a common denominator $r\in R$, such that $re_1,\dots,re_n\in R$, and have $e_1,\dots,e_n\in E$ are linearly independent over $K$ (resp. $F$) if and only if $re_1,\dots,re_n\in R$ are linearly independent over $K$ (resp. $F$). Then it's trivial.

**Remark.** 2 is equivalent to $R\otimes_KF\rightarrow R[F]$ being injective. Item 3 is very useful, in particular with $R=E$, which says:
>[!tip] Linearly Disjointness Criterion
>$E$ and $F$ are linearly disjoint over $K$ if and only if there exists a basis $X$ of $E/K$ such that $X$ is also linearly independent over $F$. And in that case, this is true for any basis $X$ of $E/K$.

Besides, we can slightly strengthen the lemma:
**Lemma'.** Assume $E$ and $F$ are the quotient fields of integral domains $R$ and $S$ respectively. Then $C$ is an $R$-module and an $S$-module in the natural way.
1. $E$ and $F$ are linearly disjoint over $K$ if and only if every subset of $R$ that is linearly independent over $K$ is also linearly independent over $S$.
2. Assume further that $R$ is a vector space over $K$. Then $E$ and $F$ are linearly disjoint over $K$ if and only if every basis of $R$ over $K$ is linearly independent over $F$.
3. Assume that both $R$ and $S$ are vector spaces over $K$. Then $E$ and $F$ are linearly disjoint over $K$ if and only if every basis $X$ of $R$ over $K$ and basis $Y$ of $S$ over $K$, the set $XY:=\{uv\,:\,u\in X,v\in Y\}$ is linearly independent over $K$.

**Theorem.** Let $C$ be an algebraically closed field with subfields $K,E,L,F$ such that $K\subset L\cap E$ and $L\subset F$. Then $E$ and $F$ are linearly disjoint over $K$ if and only if
1. $E$ and $L$ are linearly disjoint over $K$, and
2. $EL$ and $F$ are linearly disjoint over $L$.
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}

	&&C\arrow[ld,-]\arrow[rd,-]&\\
	&EL\arrow[ld,-]\arrow[rd,-]&&F\arrow[ld,-]\\
	E\arrow[rd,-]&&L\arrow[ld,-]\\
	&K&&

\end{tikzcd}
\end{document}
```
>[!proof]-
>$E$ and $F$ are linearly disjoint over $K$ if and only if $E\otimes_KF\rightarrow E[F]$ is injective. This clearly implies that $E\otimes_KL\rightarrow E[L]$ is injective, i.e. $E$ and $E$ and $L$ are linearly disjoint over $K$. Also, we have a commutative diagram
>```tikz
>\usepackage{tikz-cd}
>\begin{document}
>\begin{tikzcd}
>	E\otimes_KL\otimes_LF\arrow[r,equal]\arrow[d,->>]&E\otimes_KF\arrow[rdd]&\\
>	E[L]\otimes_LF\arrow[d]&&\\
>	EL\otimes_LF\arrow[r]&EL[F]\arrow[r,equal]&E[F]
>\end{tikzcd}
>\end{document}
>```
>We see that $E\otimes_KF\rightarrow E[F]$ being injective implies that $E[L]\otimes_LF\rightarrow EL\otimes_LF\rightarrow EL[F]$ is injective. By the lemma, we see that this is equivalent to $EL\otimes_LF\rightarrow EL[F]$ being injective, i.e. $EL$ and $F$ are linearly disjoint over $L$. The other direction follows directly from the diagram. Notice that $-\otimes_LF$ is exact since $L$ is a field.

#### 9.2 Separability for Any Extension
Let $K$ be a field with $\mathrm{char}\,K=p>0$ and let $C$ be an algebraically closed field containing $K$. For each integer $n\geq0$, set$$
\begin{align}
K^{1/p^n}&:=\{u\in C\,:\,u^{p^n}\in K\},\\
K^{1/p^{\infty}}&:=\bigcup_{n\geq0}K^{1/p^n}.
\end{align}
$$Verify that these are extensions of $K$, and since $C$ is algebraically closed, $K^{1/p^n}$ is the splitting field of $\{x^{p^n}-a\,:\,a\in K\}$, so these are essentially independent of $C$. In particular, $K=(K^{1/p^n})^{p^n}$. Besides, if $\mathrm{char}\,K=0$, we can define these to be $K$ itself for convenience.
**Lemma.** $\mathrm{char}\,K=p>0$, $C/F/K$, $C$ is algebraically closed. Then for any $n\geq0$, a subset $X$ of $F$ is linearly independent over $K^{1/p^n}$ if and only if $X^{p^n}=\{u^{P^n}\,:\,u\in X\}$ is linearly independent over $K$. Furthermore $X$ is linearly independent over $K^{1/p^{\infty}}$ if and only if $X$ is linearly independent over $K^{1/p^n}$ for all $n\geq0$.
>[!proof]-
>Every $a_i\in K$ is of the form $v_i^{p^n}$. So $\sum_ia_iu_i^{p^n}=0$ if and only if $\sum_iv_iu_i=0$. For the second statement, observe that if $\sum_iw_iu_i=0$ with $w_i\in K^{1/p^{\infty}}$, then for a large enough $n$, all $w_i$'s belong to $K^{1/p^n}$.

Using the tip from the previous section, we can show that:
**Corollary.** $F$ and $K^{1/p^{\infty}}$ are linearly disjoint over $K$ if and only if $F$ and $K^{1/p^n}$ are linearly disjoint over $K$ for every $n\geq0$.

**Theorem.** Let $F$ be a field contained in an algebraically closed field $C$. If $F/K$ is a purely transcendental extension and $\mathrm{char}\,K=p>0$, then $F$ and $K^{1/p^n}$ are linearly disjoint over $K$ for all $n\geq0$ and $F$ and $K^{1p^{\infty}}$ are linearly disjoint over $K$.
>[!proof]-
>By the corollary, we only need to prove the first statement. Let $F=K(S)$ with $S$ a transcendental base of $F/K$. If $S=\varnothing$, then the statement is trivially true. If $S\neq\varnothing$, then let $M$ be the set of monomials of elements in $S$. $S$ is algebraically independent over $K$ if and only if $M$ is linearly independent over $K$. So $M$ is a basis of $K[S]/K$. Also, $M^{p^n}$ is linearly independent over $K$ for any $n\geq0$. The theorem follows by the lemma and the tip from the previous section.

**Theorem.** $F/K$ algebraic of characteristic $p>0$, and $C$ an algebraically closed field containing $F$. Then $F/K$ is separable if and only if $F$ and $K^{1/p}$ are linearly disjoint over $K$.
>[!proof]-
>We prove here only that separability implies that $F$ and $K^{1/p}$ are linearly disjoint over $K$. The other half will be an easy consequence of results below.
>Let $X=\{u_1,\dots,u_n\}$ be a finite subset of $F$ which is linearly independent over $K$. We must show that $CX$ is linearly independent over $K^{1/p}$. The subfield $E=K(u_1,\dots,u_n)$ is finite dimensional over $K$ and has a basis $\{u_1,\dots,u_n,u_{n+1},\dots,u_r\}$. If $v\in E$ and $k\in\mathbb{N}$, then $v^k=\sum_{i=1}^ra_iu_i$ with $a_i\in K$ and hence $v^{kp}=\sum_i^pu_i^p$. Since $v$ is separable over $K$, $K(v)=K(v^p)$ and $E$ is spanned by $\{u_1^p,\dots,u_r^p\}$. Since $[E:K]=r$, $\{u_1^p,\dots,u_r^p\}$ must be a basis. Then $X^p$ is linearly independent over $K$. So $F$ and $K^{1/p}$ are linearly disjoint over $K$.

**Definition.** $F/K$. A transcendence base $S$ of $F/K$ is called a **separating transcendence base** of $F/K$ if $F/K(S)$ is separable. If $F/K$ has a separating transcendence base, then $F/K$ is said to be **separably generated.**
**Remarks.**
1. An algebraic extension is separably generated if and only if it is separable.
2. It is *not* true that every transcendence base of a separately generated extension is a separating transcendence base.
3. Every purely transcendental extension is trivially separably generated.

**Lemma.** $C/K$, $C$ is algebraically closed, then $K_0:=Gal(C/K)'=K^{1/p^{\infty}}$, where $p=\mathrm{char}\,K\geq0$.
>[!proof]-
>The case $p=0$ follows directly from Galois theory, so we assume that $\mathrm{char}\,p>0$. For any $u\in C$ such that there exists $n\in\mathbb{N}$ that $u^{p^n}\in K$, for any $\sigma\in Gal(C/K)$, $\sigma(u)$ is another root of $x^{p^n}-u^{p^n}\in K[x]$. But $x^{p^n}-u^{p^n}=(x-u)^{p^n}$ and hence only has one root $u$ of multiplicity $p^n$. So $u\in K_0$
>Conversely, let $u\in K_0$. If $u$ is transcendental over $K$, then $u\mapsto u^2$ gives an $K$-isomorphism $K(u)\cong K(u^2)$. And this further extends to a $K$-automorphism of $C$ by the last theorem of 8.2, so we see that $u\notin K_0$, which is a contradiction. So $u$ must be algebraic over $K$. Let $f\in K[x]$ be its minimal polynomial over $K$. Since $f$ is algebraically closed, $f$ splits in $C$. If $u\in K$, then trivially $u\in K^{1/p^{\infty}}$. So we assume that $u\notin K$ and hence $\mathrm{deg}\,f\geq1$. If $\mathrm{char}\,K=0$, then $f$ has distinct roots. Let $v$ be another root of $f$, then there's a $K$-isomorphism $K(u)\cong K(v)$ and it further extends to a $K$-automorphism of $C$ by the last theorem of 8.2. Consequently, $u\notin K_0$, which is a contradiction, so we must have $\mathrm{char}\,K=p>0$. The above argument also shows that $f$ only has one distinct root, namely $u$. So $K(u)/K$ is purely inseparable and hence $f=x^{p^n}-u^{p^n}$ for some $n\geq0$. Then $u^{p^n}\in K$.

**Theorem.** $F/K$ with characteristic $p\geq0$ and $C$ is an algebraically closed field containing $F$, then TFAE.
1. $F$ and $K^{1/p}$ are linearly disjoint over $K$.
2. $F$ and $K^{1/p^n}$ are linearly disjoint over $K$ for some $n\geq1$.
3. $F$ and $K^{1/p^{\infty}}$ are linearly disjoint over $K$, i.e. $F$ and $K^{1/p^n}$ are linearly disjoint over $K$ for any $n\geq0$.
4. Every finitely generated intermediate field $E$ is separably generated over $K$.
5. $K_0$ and $F$ are linearly disjoint over $K$, where $K_0$ is the fixed field of $Gal(C/K)$ relative to $C/K$.
**Remark.** (1 $\Rightarrow$ 4) provides a proof for the other direction of the previous theorem. If $K$ and $K^{1/p}$ are linearly disjoint over $K$, then for every $u\in F$, $K(u)$ is separably generated over $K$ and hence separable over $K$.
>[!proof]-
>Except in proving (3 $\Leftrightarrow$ 5) we shall assume that $\mathrm{char}\,K=p>0$ since the case when $\mathrm{char}\,K=0$ is trivial otherwise. (3 $\Rightarrow$ 2 $\Rightarrow$ 1) is immediate.
>(1 $\Rightarrow$ 4) This is the most difficult one, for details see GTM73's proof of VI.2.10. We start from a transcendence basis $\{s_1,\dots,s_r\}$ chosen from a set of generators $\{s_1,\dots,s_n\}$ of $E/K$, then choose another element $s_{r+1}$ and let $g\in K[x_1,\dots,x_{r+1}]$ such that $g(s_1,\dots,s_r,x)$ is an irreducible polynomial of $s_{r+1}$ over $K(s_1,\dots,s_r)$ (which can be chosen to be having coefficients in $K[s_1,\dots,s_n]$ by multiplying a common denominator). First we show that some $x_i$ occurs in $g$ with an exponent that is *not* divisible by $p$ using the hypothesis, say $x_1$. (From here on, we forget that $s_{r+1}$ is special.) Then we show that $\{s_2,\dots,s_{r+1}\}$ is algebraic independent and hence a transcendence base of $E/K$. Then it's easy to see that $g(x,s_2,\dots,s_{r+1})$ is irreducible in $K[s_2,\dots,s_{r+1}][x]$ and hence in $K(s_2,\dots,s_{r+1})[x]$. So $g(x,s_2,\dots,s_{r+1})$ is an irreducible polynomial for $s_1$ over $K(s_2,\dots,s_{r+1})=:L$. The derivative of $g(x,s_2,\dots,s_{r+1})$ is nonzero by the construction above and hence $s_1$ is separable and algebraic over $L$. In particular, $E=L(s_{r+2},\dots,s_n)(s_1)$ is separable and algebraic over $L(s_{r+2},\dots,s_n)=K(s_2,\dots,s_n)$. The conclusion follows by repetition of the process.
>(4 $\Rightarrow$ 3) Let $W$ be a finite subset of $F$ that is linearly independent over $K$. We must show that $W$ is linearly independent over $K^{1/p^{\infty}}$. Let $E=K(W)$. We need only show that $E$ and $K^{1/p^{\infty}}$ are linearly disjoint over $K$, since this fact immediately implies that $W$ is linearly independent over $K^{1/p^{\infty}}$. Since $W$ is finite, $E$ has a separating transcendence base $S$ over $K$. We shall prove the linear disjointness of $E$ and $K^{1/p^{\infty}}$ over $K$ by applying the last theorem of 9.2 to extensions $K\subset K^{1/p^{\infty}}$ and $K\subset K(S)\subset E$. $K(S)$ and $K^{1/p^{\infty}}$ are linearly disjoint over $K$ by since $K(S)/K$ is purely transcendental. Let $X$ be a subset of $E$ that is linearly independent over $K(S)$. Since $E$ is separable algebraic over $K(S)$, $X$ is linearly independent over $K(S)^{1/p}$. Therefore $X^p$ is linearly independent over $K(S)$. Then repeat the last three sentences. We see that $K(S)^{1/p^{\infty}}$ and $E$ are linearly disjoint over $K$. But then this implies that $E$ and the subfield $K^{1/p^{\infty}}K(S)$ are linearly disjoint over $K$. The conclusion then follows.
>(3 $\Rightarrow$ 5) Immediate consequence of the previous lemma.

**Definition.** $F/K$ is said to be separable if $F$ satisfies the equivalent conditions of the theorem.
**Remark.** We have seen that this definition is compatible with our previous one. Also, since the first condition of the theorem is trivially satisfied, we see that any extension of characteristic 0 is separable.

**Corollary.** (Mac Lane's Criterion) $F/K$, $F/K$ is separably generated, then $F/K$ is separable. Conversely, if $F/K$ is separably and finitely generated, then $F/K$ is separable, and in fact some subset of any set of generators is a separating transcendence base of $F$.
>[!proof]-
>The proof of (4 $\Rightarrow$ 3 above) is valid here with $F=E$ since it uses only the fact that $E$ is separably generated. The last two statements are consequences of the proof of (1 $\Rightarrow$ 4) above.

**Corollary.** $F/E/K$.
1. If $F/K$ is separable, then $E/K$ is separable.
2. If $F/E$ and $E/K$ are separable, then $F/K$ is separable.
3. If $F/K$ is separable and $E/K$ is algebraic, then $F/E$ is separable.
**Remark.** 3 may be false if $E$ is not algebraic over $K$!
>[!proof]-
>1 follows directly from the last theorem of 9.1. 
>For 2, $F/E$ is separable implies that $F$ and $EK^{1/p}$ are separable over $E$ since $EK^{1/p}\subset E^{1/p}$. Then the conclusion follows by applying the last theorem of 9.1 to extensions $K\subset K^{1/p}$ and $K\subset E\subset F$.
>3. If $\mathrm{char}\,K=p>0$, let $U$ be a basis of $F/E$ and let $V$ be a basis of $E/K$. Then $UV$ is a basis of $F/K$, whence $UV$ is linearly independent over $K^{1/p}$ by separability. So $(UV)^p=U^pV^p$ is linearly independent over $K$. We claim furthermore that $V^p$ is a basis of $E/K$. Because $E/K$ is separable by 1, $E$ and $K^{1/p}$ are linearly disjoint, and hence $V^p$ is linearly independent over $E$. Since $E=KE^p$ by a corollary of 6.2 (which uses the hypothesis that $E/K$ is algebraic), $V^p$ necessarily spans $E$ over $K$. Therefore, $V^p$ is a basis of $E/K$. If $\sum_ia_iu_i=0$ with $a_i\in E^{1/p}$ and $u_i\in U$, then $\sum_ia_i^pu_i^p=0$. Since $a_i\in E^{1/p}$, we have $a_i^p=\sum_jc_{ij}v_j^p$ with $c_{ij}\in K$ and $v_j\in V$. Therefore $0=\sum_{i,j}c_{ij}u_i^pv_j^p$. The linearly independence of $U^pV^p$ then implies that $c_{ij}=0$ for all $i,j$ and hence that $a_i=0$ for all $i$. Therefore, $X$ is linearly independent over $E^{1/p}$.
#### 9.3 Some Other Results
1. If $\{u_1,\dots,u_n\}$ is algebraically independent over $F$, then $F$ and $K(u_1,\dots,u_n)$ are linearly disjoint voer $K$.
2. Let $K=\mathbb{F}_p$, $F=\mathbb{F}_p(x)$ and $E=\mathbb{F}_p(x^p)$.
	1. $F/K$ is separably generated and separable.
	2. $E\neq F$.
	3. $F/E$ is algebraic and purely inseparable.
	4. $\{x^p\}$ is a transcendence base of $F/K$ which is *not* a separating transcendence base.
3. Let $\mathrm{char}\,K=p>0$ and let $u$ be transcendental over $K$. Suppose $F/K$ is generated by $\{u,v_1,\dots,v_2,\dots\}$, where $v_i$ is a root of $x^{p^i}-u\in K(u)[x]$ for $i=1,2,\dots$. Then $F/K$ is separable but not separably generated.
4. $K$ is a perfect field if and only if every field extension of $K$ is separable.
5. (Mac Lane) Assume $K$ is a perfect field, $F$ is not perfect and $\mathrm{tr.d.}\,F/K=1$. Then $F/K$ is separably generated.
6. $F/K$ is purely inseparable if and only if the only $K$-monomorphism $F\rightarrow C$ is the inclusion.
7. $E$ and $F$ are free over $K$ if every subset $X$ of $E$ that is algebraically independent over $K$ is also algebraically independent over $RF$.
	1. The definition is symmetric.
	2. If $E$ and $F$ are linearly disjoint over $K$, then $E$ and $F$ are free over $K$. But the converse is false.
	3. If $E/K$ is separable and $F$ and $E$ are free over $K$, then $EF$ is separable over $F$.
	4. If $E$ and $F$ are free over $K$ and both separable over $K$, then $EF$ is separable over $K$.
### 10
