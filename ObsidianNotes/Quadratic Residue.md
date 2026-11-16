#Algebra #Number-Theory 
### 1. Basics
**Definition.** Let $p$ be an odd prime, $d\in\mathbb{Z}$, $p\nmid d$. If there exists $a\in\mathbb{Z}$ such that
$$\tag{1.1} x^2\equiv d\mod p, $$
then we say that $d$ is a quadratic residue modulo $p$. Note that $a^2\equiv a\mod 2$, so we leave $p=2$ as a trivial case.

**Theorem 1.** In a reduced residue system modulo $p$, there exist exactly $(p-1)/2$ quadratic residues modulo $p$ and exactly $(p-1)/2$ quadratic non-residue modulo $p$. Besides, if $\ref{eq:1.1}$ has a solution $a$, then $a,-a$ are all its solutions.
**Proof.** It suffices to take
$$ -\frac{p-1}{2},-\frac{p-1}{2}+1,\cdots,-1,1,\cdots,\frac{p-1}{2}-1,\frac{p-1}{2} $$
as a reduced residue system modulo $p$. Take the square and note that $(-j)^2\equiv j^2\mod p$. We see that $d$ is a quadratic residue modulo $p$ if and only if
$$\tag{1.2} d\equiv 1^2,\cdots,(\frac{p-1}{2})^2\mod p. $$
When $1\leq i<j\leq (p-1)/2$, we have
$$ i^2\not\equiv j^2\mod p. $$
So $\ref{eq:1.2}$ gives all quadratic residues modulo $p$. The rest is trivial.
$$
\tag*{$\square$}
$$
**Theorem 2.** (Euler's Criterion) Let $p$ be an odd prime, $p\nmid d$. Then $d$ is a quadratic residue modulo $p$ if and only if
$$ d^{\frac{p-1}{2}}\equiv1\mod p\tag{1.3}. $$
Besides, $d$ is a quadratic non-residue modulo $p$ if and only if
$$ d^{\frac{p-1}{2}}\equiv-1\mod p\tag{1.4}. $$
**Proof.** First note that $d^{p-1}\equiv 1\mod p$. Therefore one of the two equations holds. If $d$ is a quadratic residue modulo $p$, say $a^2\equiv d\mod p$, then $d^{\frac{p-1}{2}}\equiv a^{p-1}\equiv 1\mod p$. Now suppose $d$ is not a quadratic residue. Consider the equation
$$ xy\equiv d\mod p. $$
Fix a reduced residue system modulo $p$. For any $y$ in this system, there exists a unique $x$ in this system satisfying this equation. However, since $d$ is a quadratic non-residue, $x\neq y$. Therefore the reduced system can be split into $(p-1)/2$ pairs. (Note that if $d$ is a quadratic residue, then the system splits into $(p-1)/2-1$ pairs and two square-roots $a$ and $-a$ of $d$ modulo $p$.) Then
$$ d^{\frac{p-1}{2}}\equiv\prod_{i=1}^{\frac{p-1}{2}}x_iy_i\equiv(p-1)!\equiv-1\mod p. $$
Note that if $d$ is a quadratic residue, then
$$	d^{\frac{p-1}{2}}\equiv a(-a)\prod_{i=1}^{\frac{p-1}{2}-1}x_iy_i\equiv-(p-1)!\equiv1\mod p.$$
$$\tag*{$\square$}$$
**Corollary 3.** $-1$ is a quadratic residue modulo $p$ if and only if $p\equiv1\mod 4$. When $p\equiv1\mod 4$,
$$ \left(\pm\left(\frac{p-1}{2}\right)!\right)^2\equiv-1\mod p.\tag{1.5}$$
**Proof.** By **Theorem 2**, $-1$ is a quadratic residue modulo $p$ if and only if
$$ (-1)^{\frac{p-1}{2}}\equiv1\mod p.$$
Since $p>2$, this is equivalent to $p\equiv1\mod 4$. The last part follows from the choice of reduced residue system in **Theorem 1** and
$$-1\equiv(p-1)!\equiv(-1)^{\frac{p-1}{2}}\left(\left(\frac{p-1}{2}\right)!\right)^2\mod p.$$
$$\tag*{$\square$}$$
**Corollary 4.** Let $p$ be an odd prime, $p\nmid d_1$ and $p\nmid d_2$. Then
1. If $d_1,d_2$ are quadratic residues modulo $p$, then so is $d_1d_2$.
2. If $d_1,d_2$ are quadratic non-residues modulo $p$, then so is $d_1d_2$.
3. If $d_1$ is a quadratic residue modulo $p$ and $d_2$ is not, then $d_1d_2$ is not.
**Proof.** This follows immediately from **Theorem 2**.
$$\tag*{$\square$}$$
### 2. Gaussian Reciprocity
**Definition.** We introduce the Legendre symbol
$$\genfrac{(}{)}{}{}{d}{p}=\begin{cases}
1,&d\text{ is a quadratic residue modulo }p;\\
-1,&d\text{ is a quadratic non-residue modulo }p;\\
0,&p\mid d.
\end{cases}\tag{2.1}$$
**Theorem 1.** Let $p$ be a prime and $d,c$ be integers.
1. $\genfrac{(}{)}{}{}{d}{p}=\genfrac{(}{)}{}{}{d+p}{p}$.
2. $\genfrac{(}{)}{}{}{d}{p}\equiv d^{\frac{p-1}{2}}\mod p$.
3. $\genfrac{(}{)}{}{}{dc}{p}=\genfrac{(}{)}{}{}{d}{p}\genfrac{(}{)}{}{}{c}{p}$.
4. If $p\nmid d$, then $\genfrac{(}{)}{}{}{d^2}{p}=1$.
5. $\genfrac{(}{)}{}{}{1}{p}=1,\genfrac{(}{)}{}{}{-1}{p}=(-1)^{\frac{p-1}{2}}$.
**Proof.** All are trivial.
$$\tag*{$\square$}$$
So if we can compute
$$\genfrac{(}{)}{}{}{-1}{p},\quad\genfrac{(}{)}{}{}{2}{p}
,\quad\genfrac{(}{)}{}{}{q}{p},$$
then we can compute arbitrary $\genfrac{(}{)}{}{}{d}{p}$, where $q$ is any odd prime less than $p$.
**Lemma 2.** (Gaussian Lemma) Let $p$ be an odd prime, $p\nmid d$. Suppose $1\leq j<p/2$, and
$$ t_j\equiv jd\mod p $$
with $0<t_j<p$. Let $n$ be the number of $t_j$ bigger than $p/2$. Then
$$\genfrac{(}{)}{}{}{d}{p}=(-1)^n.\tag{2.2} $$
**Proof.** For any $1\leq j<i<p/2$,
$$ t_j\pm t_i\equiv (j\pm i)d\not\equiv0\mod p, $$
i.e., $t_i\not\equiv\pm t_j\mod p$. Let $r_1,\dots,r_n$ be those $t_j$ greater than $p/2$. Let $s_1,\dots,s_k$ be those less than $p/2$. Then $1\leq p-r_i<p/2$. Therefore
$$ s_j\not\equiv p-r_i\mod p,\quad\forall i,j.$$
Therefore $s_1,\dots,s_k,p-r_1,\dots,p-r_n$ is a permutation of $1,\dots,(p-1)/2$. So
$$
\begin{align*}
\left(\frac{p-1}{2}\right)!\cdot d^{\frac{p-2}{2}}
&\equiv t_1\cdots t_{\frac{p-1}{2}}\\
&\equiv s_1\cdots s_k\cdot r_1\cdots r_n\\
&\equiv(-1)^ns_1\cdots s_k\cdot(p-r_1)\cdots(p-r_n)\\
&\equiv(-1)^n\left(\frac{p-1}{2}\right)!\mod p.
\end{align*}
$$
And therefore
$$ d^{\frac{p-1}{2}}\equiv(-1)^n\mod p. $$
The conclusion then follows from Euler's criterion above.
$$\tag*{$\square$}$$
**Theorem 3.** We have
$$ \genfrac{(}{)}{}{}{2}{p}=(-1)^{\frac{p^2-1}{2}}.\tag{2.3} $$
**Proof.** Take $d=2$ in **Lemma 2**, we see that
$$
\begin{align*}
1\leq t_j=2j<p/2,\quad&1\leq j<p/4;\\
p/2<t_j=2j<p,\quad &p/4<j<p/2.
\end{align*}
$$
So
$$ n=\frac{p-1}{2}-\left[\frac{p}{4}\right]. $$
Therefore
$$
n=
\begin{cases}
l,&p=4l+1;\\
l+1,&p=4l+3.
\end{cases}
$$
Then by $\ref{eq:2.2}$ we have
$$
\genfrac{(}{)}{}{}{2}{p}=(-1)^n=
\begin{cases}
1,&p\equiv \pm1\mod 8;\\
-1,&p\equiv\pm3\mod 8.
\end{cases}
$$
And the conclusion follows.
$$\tag*{$\square$}$$
Now we analyze **Lemma 2** further.
$$ jd=p\genfrac{[}{]}{}{}{jd}{p}+t_j, \quad1\leq j<p/2.$$
Take summation over $j$ we get
$$ d\sum_{j=1}^{\frac{p-1}{2}}j=pT+\sum_{j=1}^{\frac{p-1}{2}}t_j, $$
where
$$ T=\sum_{j=1}^{\frac{p-1}{2}}\genfrac{[}{]}{}{}{jd}{p}.\tag{2.4} $$
The proof of **Lemma 2** shows that
$$ \sum_{j=1}^{\frac{p-1}{2}}t_j=\sum_{j=1}^{\frac{p-1}{2}}j-np+2(r_1+\cdots r_n). $$
Therefore
$$ \frac{p^2-1}{8}(d-1)=p(T-n)+2(r_1+\cdots+r_n).\tag{2.5} $$
When $d=2$, clearly $T=0$ and hence $n\equiv(p^2-1)/8\mod 2$ and **Theorem 3** follows. When $(d,2p)=1$, we get $T\equiv n\mod 2$. So we have proved
**Theorem 4.** Let $p$ be an odd prime, $(d,2p)=1$. Then
$$ \genfrac{(}{)}{}{}{d}{p}=(-1)^T, $$
where $T$ is defined by equation $\ref{eq:2.4}$.

When $d$ is positive,
$$ T=\#\left\{(x,y)\in\mathbb{Z}^2\,|\,x<p/2,0<y<dx/p\right\}, $$ ![[Excalidraw/Quadratic Residue-fig1.excalidraw.md#^clippedframe=XQqG30eo]]i.e., the number of integer points in $\Delta OAB$. Now, suppose $d=q\neq p$ is another odd prime. (Check that their isn't any integer point on $\overline{AB},\overline{OB}$ other than $O$.) Then
$$ \genfrac{(}{)}{}{}{q}{p}=(-1)^S, $$where
$$
S=\sum_{i=1}^{\frac{q-1}{2}}\genfrac{[}{]}{}{}{lp}{q},
$$
i.e., $S$ is the number of integer points in $\Delta OBC$. Consequently, $S+T$ is the number of integer points in the rectangle $OABC$. Therefore
$$ S+T=\frac{p-1}{2}\cdot\frac{q-1}{2}. $$
We have proved the following main theorem:
**Theorem 5.** (Gaussian Reciprocity) Let $p,q$ be distinct odd primes, then
$$ \genfrac{(}{)}{}{}{q}{p}\genfrac{(}{)}{}{}{p}{q}=(-1)^{\frac{(p-1)(q-1)}{4}}.\tag{2.6} $$
In particular, if $p\text{ or }q\equiv 1\mod 4$, then
$$ \genfrac{(}{)}{}{}{q}{p}=\genfrac{(}{)}{}{}{p}{q}. $$
And $p\equiv q\equiv 3\mod 4$ if and only if
$$
\genfrac{(}{)}{}{}{q}{p}=-\genfrac{(}{)}{}{}{p}{q}.
$$
**Remark.** By repeatedly using **Theorem 5**, item 1 of **Theorem 1**, and previous results on $d=2,-1$, we can compute Legendre symbol for any $d$.

The proof above is due to Gauss (introducing Gauss's lemma in his third proof of Gaussian reciprocity) and Ferdinand Gotthold Eisenstein (the same Eisenstein with the the famous and surprisingly useful Eisenstein criterion; contributing the elegant method of counting lattice points). Now we give another proof, employing the so-called Gauss sums in finite fields.

Let $p\neq q$ be two odd primes and $F=\mathbb{F}_{q^{p-1}}$. By section 5 of [[Summary on Field Extensions]], $F^*$ is an acyclic group of order $q^{p-1}-1$. Since $\mathbb{F}^*_p$ has order $p-1$, we see that $p\mid q^{p-1}-1$. Therefore, there exists $\zeta\in F$ of order $p$. Note that for any $i\neq p$, $\zeta^i$ generates the same order $p$ subgroup of $F^*$. Moreover, we have
$$ x^p-1=(x-1)(x-\zeta)\cdots(x-\zeta^{p-1})\in F[x]. $$
Consider the Gauss sum
$$ G:=\sum_{i=1}^{p-1}\genfrac{(}{)}{}{}{i}{p}\zeta^i\in F.\tag{2.7} $$
We derive two expressions for $G^q$. On one hand, we have
$$
\begin{align*}
G^q
&=\sum_{i=1}^{p-1}\genfrac{(}{)}{}{}{i}{p}^q\zeta^{iq}\\
&=\sum_{i=1}^{p-1}\genfrac{(}{)}{}{}{i}{p}\zeta^{iq}\\
&=\genfrac{(}{)}{}{}{q}{p}\sum_{i=1}^{p-1}\genfrac{(}{)}{}{}{iq}{p}\zeta^{iq}\\
&=\genfrac{(}{)}{}{}{q}{p}G.\tag{2.8}
\end{align*}
$$
On the other hand, suppose we can prove
$$ G^2=(-1)^{\frac{p-1}{2}}p,\tag{2.9} $$
then
$$
\begin{align*}
G^q
&=G\cdot G^{2\cdot\frac{q-1}{2}}\\
&=(-1)^{\frac{(p-1)(q-1)}{4}}p^{\frac{q-1}{2}}G\\
&=(-1)^{\frac{(p-1)(q-1)}{4}}\genfrac{(}{)}{}{}{q}{p}G.\tag{2.10}
\end{align*}
$$
Comparing equation $\ref{eq:2.8}$ and $\ref{eq:2.10}$ and cancel $G$, we get Gaussian reciprocity. Now it remains to prove $\ref{eq:2.9}$. Note that
$$ \sum_{i=1}^p\zeta^i=0,\quad \sum_{i=1}^{p-1}\genfrac{(}{)}{}{}{i}{p}=0. $$
So we have
$$
\begin{align*}
G^2
&=\sum_{i,j}\genfrac{(}{)}{}{}{ij}{p}\zeta^{i+j}\\
&=\sum_{i,k}\genfrac{(}{)}{}{}{k}{p}\zeta^{(1+k)i}\quad (j\equiv ik\mod p)\\
&=\sum_{k=1}^{p-1}\genfrac{(}{)}{}{}{k}{p}\sum_{i=1}^{p-1}\zeta^{(1+k)i}\\
&=\genfrac{(}{)}{}{}{-1}{p}(p-1)+\sum_{k=1}^{p-2}\genfrac{(}{)}{}{}{k}{p}\cdot(-1)\\
&=\genfrac{(}{)}{}{}{-1}{p}(p-1)+\genfrac{(}{)}{}{}{-1}{p}\\
&=p\genfrac{(}{)}{}{}{-1}{p}.
\end{align*}
$$
Then $\ref{eq:2.9}$ follows from **Corollary 1.3**.
**Remark.** This proof is more intuitive in my opinion. The Legendre symbol is a very good function modulo $p$ and using it as the weight function the power of a $p$-th unit root in $F$ gives many beautiful properties. Moreover, this method can be used to prove higher reciprocities. See [[Gauss-Jacobi-sums.pdf]].
### 3. Jacobi Symbols
**Definition.** Let $P>1$ be an odd integer, $P=p_1\cdots p_s$ with $p_j$ prime. We define
$$ \genfrac{(}{)}{}{}{d}{P}=\genfrac{(}{)}{}{}{d}{p_1}\cdots\genfrac{(}{)}{}{}{d}{p_s}\tag{3.1}. $$
**Theorem 1.** Let $P,P_1,P_2>1$ be odd, $d,c\in\mathbb{Z}.$
1. $\genfrac{(}{)}{}{}{1}{P}=1$; when $(d,P)>1$, $\genfrac{(}{)}{}{}{d}{P}=0$; when $\genfrac{(}{)}{}{}{d}{P}=1$, $\genfrac{(}{)}{}{}{d}{P}=\pm1$.
2. $\genfrac{(}{)}{}{}{d}{P}=\genfrac{(}{)}{}{}{d+P}{P}$.
3. $\genfrac{(}{)}{}{}{dc}{P}=\genfrac{(}{)}{}{}{d}{P}\genfrac{(}{)}{}{}{c}{P}$.
4. $\genfrac{(}{)}{}{}{d}{P_1P_2}=\genfrac{(}{)}{}{}{d}{P_1}\genfrac{(}{)}{}{}{d}{P_2}$.
5. When $(P,d)=1$, $\genfrac{(}{)}{}{}{d^2}{P}=\genfrac{(}{)}{}{}{d}{P^2}=1$.
**Proof.** Easy.
$$\tag*{$\square$}$$
**Lemma 2.** Suppose $a_j\equiv 1\mod m$ for $1\leq j\leq s$. Put $a=a_1\cdots a_s$. Then
$$ \frac{a-1}{m}\equiv\frac{a_1-1}{m}+\cdots+\frac{a_s-1}{m}\mod m. $$