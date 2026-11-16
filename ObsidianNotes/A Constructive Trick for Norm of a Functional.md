#Analysis #Functional-Analysis #Harmonic-Analysis  
**Proposition.** Endow $C(T)$ with the infinite norm and $\mathbb{C}$ the canonical one. Then $T_N=S_Nf(0):C(T)\rightarrow\mathbb{C}$ has norm $L_N=\int_{-\frac{1}{2}}^{\frac{1}{2}}|D_N(t)|\,dt$.
One side is trivial, the hard part is to show that $||T_N||\geq L_N$. We need a sequence ${f_n}$ s.t.
1. $f_n\in C(T)$
2. $||f_n||_{\infty}\leq 1$
3. $\lim_{n\to\infty}T_N(f_n)=L_N$
To maximize $$T_N(f)=\int_{-\frac{1}{2}}^{\frac{1}{2}}f(t)D_N(t)\,dt,$$the ideal case is to have $f(t)D_N(t)=|D_N(t)|$, i.e. $f=\text{sgn}\,D_N=\frac{D_N}{|D_N|}$. So we need a sequence of continuous functions approaching it. The solution is$$f_n(t)=\frac{nD_N(t)}{1+n|D_N(t)|}.$$Verification:$$
\begin{align}
T_Nf_n-L_N=&\int_{-\frac{1}{2}}^{\frac{1}{2}}\frac{n|D_N(t)|^2}{1+n|D_N(t)}-|D_N(t)|\,dt\\
=&-\int_{-\frac{1}{2}}^{\frac{1}{2}}\frac{|D_N(t)|}{1+n|D_N(t)|}\,dt\to0\text{ as }n\to 0.
\end{align}
$$