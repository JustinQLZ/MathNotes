#Analysis #Real-Analysis #Harmonic-Analysis 
**Theorem 1. (Average Continuity)** Let $p\in[1,\infty)$, $f\in L^p(\mathbb{R}^n)$ and $f_h(x):=f(x+h)$, then$$
||f-f_h||_p\to0\text{ as }h\to0.
$$**Theorem 2. (Smooth Approximation)** Let $p\in[1,\infty)$, then $C_c^{\infty}(\mathbb{R}^n)$ is dense in $L^p(\mathbb{R}^n)$.
**Remark.** A classical counterexample for theorem 1 and 2 when $p=\infty$ is the step function. However, we have:
**Proposition.** Let $f\in L^{\infty}(\mathbb{R}^n)$, then $f$ is uniformly continuous on the complement of a null set if and only if$$
||f-f_h||_{\infty}\to0\text{ as }h\to0.
$$**Remark.** The convergence in $L^{\infty}$ is equivalent to uniform convergence on the complement of a null set!
**Corollary 1. (Riemann-Lebesgue Lemma)** Let $\{g_n\}$ be a sequence in $L^1[a,b]$ with a uniform boundary $M$ such that $\forall c\in[a,b]\,\int_a^cg_n\,dx\to0$, then $\forall f\in L^1[a,b]$ $$
\int_a^bf\cdot g_n\,dx\to0.
$$$[a,b]$ can be replaced by a infinite interval or $\mathbb{R}$.
In particular, $g_n(x)=\sin2\pi nx$ and $g_n(x)=\cos2\pi nx$ satisfies the condition on $[0,1]$.
**Remark.** Proof of many basic convergence theorems in Fourier analysis, such as Dini, Jordan, etc., follows from introducing a sequence of kernel functions $\{K_N\}$ to deal with the sum and simplifying the integral sequence into a difference of some $\hat{g}(k)=\int_0^1g(x)\,e^{2\pi ikx}\,dx$ which goes to 0 by R-L lemma.

TBD
The two theorems are equivalent.
