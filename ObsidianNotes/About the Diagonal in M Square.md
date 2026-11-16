#Algebraic-Topology #Geometry #Topology 
This material is extended from Bott. & Tu., sec 11.
Let $M$ be a smooth compact oriented manifold and for any smooth map $f:M\rightarrow M$, denote $\Gamma_f\subset M\times M$ the graph of $f$. $\Gamma_f$ is diffeomorphic to $M$, with the diffeomorphisms given by $\iota=\mathbb{1}\times f$ and $\pi$, the projection onto the first variable. Also denote $\rho$ the projection onto the second variable. The diagonal of $M\times M$, denote $\Delta$, is the graph of the identity of $M$. $\Delta$ has many technical applications in algebraic topology.

Let $\{\omega_i\}$ be a basis of $H^*(M)$, $\{\tau_j\}$ be the dual basis under Poincaré duality, i.e., $\int_M\omega_i\wedge\tau_j=\delta_{ij}$. By the Künneth formula, $H^*(M\times M)=H^*(M)\bigotimes H^*(M)$ with $\{\pi^*\omega_i\wedge\rho^*\tau_j\}$ as a basis. For any closed $\eta$ on $M\times M$, suppose $\eta=\sum c_{ij}\pi^*\omega_i\wedge\rho^*\tau_j$, let's calculate its integration on $\Delta$.
$$
\begin{align}
\int_{\Delta}\eta &=\sum c_{ij}\int_{\Delta}\pi^*\omega_i\wedge\rho^*\tau_j\\
&=\sum c_{ij}\int_{M}\iota^*\pi^*\omega_i\wedge\iota^*\rho^*\tau_j\\
&=\sum c_{ij}\int_M\omega_i\wedge\tau_j\\
&=\sum c_{ij}\,\delta_{ij}\\
&=\sum_ic_{ii}
\end{align}
$$
For any smooth $f:M\rightarrow M$, suppose $f^*\omega_i=\sum_j {c'}_{ij}\,\omega_j$. Let $\eta_f$ be the Poincaré dual of $\Gamma_f$, we can calculate the coefficients as follows:
**Proposition.** $\eta_f=\sum(-1)^{(deg\,\tau_k)\,(deg\,\omega_k)\,+\,(deg\,\tau_k)\,(deg\,\omega_l)\,+\,(\deg\,\omega_l)\,(\deg\,\omega_k)}{c'}_{lk}\,\pi^*\omega_k\wedge\rho^*\tau_l$. In particular, $\eta_{\Delta}=\sum(-1)^{(deg\,\omega_i)}\pi^*\omega_i\wedge\rho^*\tau_i$.
**Proof.** We show this by calculating $\int_{\Gamma_f}\pi^*\tau_k\wedge\rho^*\omega_l$ in two ways. On one hand, we have
$$
\begin{equation}
\int_{\Gamma_f}\pi^*\tau_k\wedge\rho^*\omega_l=\int_M\iota^*\pi^*\tau_k\wedge\iota^*\rho^*\omega_l=\int_M\tau_k\wedge f^*\omega_l={c'}_{lk}(-1)^{(deg\,\tau_k)\,(deg\,\omega_l)}
\end{equation}
$$
On the other hand, by the definition of the Poincaré dual of a compact oriented submanifold,
$$
\begin{align}
\int_{\Gamma_f}\pi^*\tau_k\wedge\rho^*\omega_l &=\int_{M\times M}\pi^*\tau_k\wedge\rho^*\omega_l\wedge\eta_f\\
&=\sum c_{ij}\int_{M\times M}\pi^*\tau_k\wedge\rho^*\omega_l\wedge\pi^*\omega_i\wedge\rho^*\tau_j\\
&=\sum c_{ij}(-1)^{(deg\,\tau_k\,+\,\deg\,\omega_l)(deg\,\omega_i)}\int_{M\times M}\pi^*(\omega_i\wedge\tau_k)\wedge\rho^*(\omega_l\wedge\tau_j)\\
&=(-1)^{(deg\,\tau_k\,+\,\deg\,\omega_l)(deg\,\omega_k)}c_{kl}
\end{align}
$$
Therefore
$$
c_{kl}=(-1)^{(deg\,\tau_k)\,(deg\,\omega_k)\,+\,(deg\,\tau_k)\,(deg\,\omega_l)\,+\,(\deg\,\omega_l)\,(\deg\,\omega_k)}{c'}_{lk}
$$
$$\tag*{$\square$}$$
If we define the Lefschetz number of $f$ to be
$$
L(f)=\sum_q(-1)^{q}\, trace\,H^q(f)
$$
and define the Euler characteristic of $M$ to be
$$
\chi(M)=\sum_q(-1)^{q}\,dim\,H^q(M)=L(\mathbb{1}_M)
$$
then we have
**Corollary.** $\int_{\Delta}\eta_f=L(f)$. In particular, $\int_{\Delta}\eta_{\Delta}=\chi(M)$.
**Proof.** Just combine previous calculations together.$$\tag*{$\square$}$$
Next we need a lemma:
**Lemma.** The tangent bundle of $\Delta$, denote $T_{\Delta}$, is isomorphic to the normal bundle of $\Delta$ in $M\times M$, denote $N_{\Delta}$.
**Proof.** $\iota:M\rightarrow M\times M$ is a diffeomorphism onto $\Delta$, so $\iota^*T_{\Delta}=T_M$. Also there's an isomorphism $T_{M\times M}\bigr|_{\Delta}\cong T_M\oplus T_M$. It follows from the commutative diagram
$$
\begin{CD}
0 @>>>T_{\Delta} @>(v,v)\,\mapsto\,(v,v)>> T_{M\times M}\bigr|_{\Delta}@>>>N_{\Delta}@>>>0\\
  @.               @VV\sim V                      @VV\sim V\\
0@>>>T_M@>>v\,\mapsto\,(v,v)>T_M\oplus T_M@>>>T_M@>>>0\\
\end{CD}
$$ that $N_{\Delta}\cong T_M\cong T_{\Delta}$.$$\tag*{$\square$}$$
Since $\eta_{\Delta}$ is the [Thom class] of $N_{\Delta}$ regarded as a tubular neighborhood of $\Delta$ in $M\times M$, and the restriction of $\Phi(N_{\Delta})$ onto the zeros section is the Euler class $e(N_{\Delta})$, we have
$$
\begin{align}
\int_{\Delta}\eta_{\Delta} &=\int_{\Delta}\Phi(N_{\Delta})\\
&=\int_{\Delta}e(N_{\Delta})\\
&=\int_{\Delta}e(T_{\Delta})\\
&=\int_{M}e(T_M)
\end{align}
$$
We get another definition of the Euler characteristic. In summary, we have
**Theorem.** Let $M$ be a smooth compact oriented manifold, then all following identical numbers are the Euler characteristic of $M$.
1. $I(0_{T_M},0_{T_M})$, where $0_{T_M}$ is the zero section of $T_M$
2. $\sum_{V_p=0} ind_p\,V$, where $V$ is a vector field on $M$ with isolated zeros
3. $I(\Delta, \Delta)$
4. $\sum_q(-1)^{q}\,dim\,H^q(M)$
5. $L(\mathbb{1}_M)$, the Lefschetz number of the identity of $M$
6. $\int_{\Delta}\eta_{\Delta}$
7. $\int_{M}e(T_M)$
8. (If $n=dim\,M$ is even) $\frac{2}{\gamma_n}\int_MK\,\Omega$, for a given Riemann structure on $M$, where $\Omega$ is a positive volume form, $K$ is the Gaussian curvature of $M$ relative to $\Omega$, and $\gamma_n$ is the area of $S^n$
9. The alternating sum of the number of simplicials in an arbitrary simplicial decomposition of $M$
