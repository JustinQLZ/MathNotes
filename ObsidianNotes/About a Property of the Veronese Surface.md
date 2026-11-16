#Algebra #Commutative-Algebra #Algebraic-Geometry 
This is an exercise from Hartshorne, see Hartshorne, Exercise I.2.12-13. The Veronese Surface, denote $V$, is by definition the image of the 2-uple embedding $\rho_2:\mathbb{P}^2\rightarrow\mathbb{P}^5$.
**Theorem.** Let $Z\subset V$ be a closed curve, i.e. a variety of dimension 1, then there exists a hypersurface $H\subset\mathbb{P}^5$ such that $H\cap V=Z$.

### The Proof
**Lemma.** Any factor of a homogeneous polynomials in $k[x_0,\dots,x_n]$ is homogeneous.
**Proof.** Take $\alpha:k[x_0,\dots,x_n]\rightarrow k[x_1,\dots,x_n]$ as $\alpha(F)=F(1,x_1,\dots,x_n)$ and take $\beta:k[x_1,\dots,x_n]\rightarrow k[x_0,\dots,x_n]$ as $\beta(f)=x_0^{\text{deg}\,f}f(\frac{x_1}{x_0},\dots,\frac{x_n}{x_0})$. If $F$ is homogeneous, verify that
1. $\beta(f)$ is homogeneous,
2. $\alpha$ and $\beta$ are multiplicative,
3. $\alpha\circ\beta(f)=f$,
4. if $x_0$ does not divide $F$, then $\beta\circ\alpha(F)=F$, and that
5. $\alpha(F)\in k$ if and only if $F$ is a constant multiple of a power of $x_0$.
Now for any homogeneous $F$ of positive degree, after factoring a power of $x_0$, we may assume that $x_0$ does not divide $F$. Suppose $\alpha(F)$ factors into irreducible polynomials $f_1\cdots f_r$, then $$F=\beta\circ\alpha(F)=\beta(f_1\cdots f_r)=\beta(f_1)\cdots\beta(f_r).$$Now it suffices to prove that the $\beta(f_i)$'s are irreducible. Suppose, say, $\beta(f_1)$ is reducible, $\beta(f_1)=F_1F_2$ for nonconstant $F_1$ and $F_2$, then $$f_1=\alpha\circ\beta(f_1)=\alpha(F_1)\alpha(F_2)$$and since $f_1$ is irreducible, one of $F_1$ and $F_2$, say $F_1$, is constant. So $F_1$ is a constant multiple of a power of $x_0$, contradicting the assumption that $x_0$ does not divide $F$.$$\tag*{$\square$}$$
**Proof  of the Theorem.** Let $A=k[y_0,\dots,y_5]$, $B=k[x_0,x_1,x_2]$ and $\theta:A\rightarrow B$ the homomorphism sending $y_i$'s to all the monomials of degree 2 in $x_0,x_1,x_2$. Notice that by Hartshorne, Exercise I.2.12, (b) we have $V=Z(\text{ker}\,\theta)$. Also denote $Y=\rho_2^{-1}(Z)$, then $Y$ is a variety in $\mathbb{P}^2$ of dimension 1, so it's a hypersurface. Hence there exists a homogeneous irreducible polynomial $f\in B$ such that $I(Y)=(f)$. Notice that $f^2\in\text{im}\,\theta$, so there exists $g\in A$ such that $\theta(g)=f^2$. By the lemma, $g$ factors into homogeneous irreducible polynomials $g_1\cdots g_r$. Each of them defines a hypersurface $H_i=Z(g_i)\subset\mathbb{P}^5$.
For any $P\in V$,$$
\begin{align}
P\in Z & \iff Q=\rho_2^{-1}(P)\in Y\\
&\iff f(Q)=0\iff f^2(Q)=0\\
&\iff g(P)=g(\rho_2(Q))=\theta(g)(Q)=0\\
&\iff P\in Z(g)=H_1\cup\cdots\cup H_r.
\end{align}
$$Hence $Z=V\cap(H_1\cup\cdots\cup H_r)$. However, since $Z$ is irreducible, there exists $i$ such that $Z=V\cap H_i$.$$\tag*{$\square$}$$**Remark.** Remember that you can always take powers of polynomials with the variety unchanged. Notice also how does the irreducibility work at last.

### Something Else
Here's my failed contempt.
**Definition.** Let $C=\bigoplus_{d\geq0}C_d$ be a graded ring and denote $C^{(m)}=\bigoplus_{d\geq0}C_{dm}$, called the m-th Veronese subring.
**Lemma.** If $C$ is a graded domain that is integrally closed, then $C^{(m)}$ is also integrally closed.
**Proof.** Let $f\in\text{Frac}\,C^{(m)}$ be integral over $C^{(m)}$, then there exists $s_1,\dots,s_n\in C^{(m)}$ such that$$
f^n+s_1f_{n-1}+\cdots+s_n=0.
$$ Since $C^{(m)}\subset C$ and $C$ is integrally closed, $f\in C\cap\text{Frac}\,C^{(m)}$. A simple calculation then shows that $f$ must lies in $C^{(m)}$.$$\tag*{$\square$}$$First observe that $\text{im}\,\theta$ is precisely the 2nd Veronese subring of $B$. Since $B$ is integrally closed, by the lemma, $\text{im}\,\theta$ is also integrally closed. Also, since $B=(\text{im}\,\theta)[x_0,x_1,x_2]$ and we have $(x_i)^2-x_i^2=0$, $\theta$ is integral. Hence $\theta$ satisfies the going-up property.
Now $\text{dim}\,\rho_2^{-1}(Z)=\text{dim}\,Z=1$, so $\rho_2^{-1}(Z)$ is a hypersurface in $\mathbb{P}^2$ and its ideal, denote $\mathfrak{p}$, is prime of height 1. Since $\theta$ satisfies the going-up property, $\mathfrak{q}=\text{im}\,\theta\cap\mathfrak{p}$ is also prime of height 1.
Now, the problem is that $\theta^{-1}(\mathfrak{p})$ is of height 1 over $\alpha$ but $\text{im}\,\theta\cong A/\alpha$ is not a UFD! Because $(x_0x_1)(x_0x_2)(x_1x_2)=(x_0^2)(x_1^2)(x_2^2)$. So we can't conclude that $\theta^{-1}(\mathfrak{p})=\alpha+(g)$.

Reorganizing the idea, let $\mathfrak{q}=I(Z)$, $\alpha=\text{ker}\,\theta$, we need$$
\begin{align}
Z&=V\cap H\\
&=Z(\alpha)\cap Z(g)\\
&=Z(\alpha+(g))=Z(\mathfrak{q})
\end{align}
$$i.e. $\mathfrak{q}=r(\alpha+(g))$, or identically $\mathfrak{q}/\mathfrak{\alpha}=r((\bar{g}))$. Where $g\in A$ is a homogeneous irreducible polynomial and $\bar{g}$ is its image under $\theta$. (We identify $\text{im}\,\theta$ and $A/\alpha$.) Meanwhile, we know that $Z(Y)=\mathfrak{p}$ is principal, say $\mathfrak{p}=(h)$, where $h$ is a homogeneous irreducible polynomial of degree $d$. Our attempt is to find $g$ out of $h$. If $A/\alpha$ is a UFD then $\mathfrak{p}\cap \text{im}\,\theta$ would be principal and we could just take $\bar{g}$ to be its generator, but this is not the case.
Here's the correction:
Case 1: $d$ is even. Then $h\in S=\text{im}\,\theta$. This is the case when $\mathfrak{p}\cap S$ is principal and is actually generated by $h$. Clearly $(h)_S\subset(h)_B\cap S$. Conversely, for any $f\in(h)_B\cap S$, there exists $u\in B$ such that $f=hu$. Hence $\text{deg}\,u=\text{deg}\,f-\text{deg}\,h$ is even and $u\in S$. Hence $f\in(h)_S$.
Case 2: d is odd. Here $h\notin S$ and $\mathfrak{p}\cap S$ is not principal. (verified) ==However, we only need it to be the radical of  a principal ideal!== The key is again the remark above! $h^2\in S$. Verify that $\mathfrak{p}\cap S=r((h^2)_S)$. And take arbitrary preimage of $h^2$ as $g$. Notice that this also works for case 1 and is essentially the first proof.