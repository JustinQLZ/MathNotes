#Algebra #Commutative-Algebra #Artinian-Rings #Noetherian-Rings
### Assumptions
Rings are assumed to be commutative with identity, and we assume the following facts are proved:
1. Let $A$ be a ring such that there exists maximal ideals $\mathfrak{m}_1, ..., \mathfrak{m}_k\subset A\enspace s.t.\,\mathfrak{m}_1...\mathfrak{m}_k=0$, then $A$ is Noetherian $\iff$ it's Artinian.
2. A Noetherian space only has finitely many irreducible components and irreducible components (Atiyah, Exercise 6.7) in $Spec\,A$ corresponds to minimal primes of $A$ (Atiyah, Exercise 1.20).
3. All ideals in a Noetherian ring has primary decompositions, in particular, $(0)$ has one.
## Proofs
**Proof 1.** $dim\,A=0\implies Spec\,A=Max\,A$. Let $(0)=\mathfrak{q}_1\cap, ...,\cap\mathfrak{q}_r$ be a primary decomposition and denote $\mathfrak{m}_i=r(\mathfrak{q}_i)\in Max\,A$, and denote $\mathfrak{n}$ the nilradical of $A$. $A$ is Noetherian$\implies\exists k\in\mathbb{N}\enspace\mathfrak{n}^k=0$. So $\mathfrak{n}=r(0)=\mathfrak{m_1}\cap,...,\cap\mathfrak{m_r}\supset\mathfrak{m}_1...\mathfrak{m}_r\implies\mathfrak{m}_1^k...\mathfrak{m}_r^k=0\implies$ A is Artinian.$$\tag*{$\square$}$$
**Proof 2.** Denote $\mathfrak{n}$ the nilradical of $A$. $dim\,A=0\implies Spec\,A=Max\,A$. Then use Assumption 2 to show that $Max\,A$ is finite, then use $n^k=0$.$$\tag*{$\square$}$$
