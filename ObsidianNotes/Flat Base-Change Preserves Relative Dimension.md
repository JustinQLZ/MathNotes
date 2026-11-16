#Algebraic-Geometry 
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath}
\begin{document}
\begin{tikzcd}

	g'^{-1}(y')\arrow[d]\arrow[r]&X'\arrow[d,"g'"]\arrow[r,"f'"]&X\arrow[d,"g"]\\
	\mathrm{Spec}\,k(y')\arrow[r,"i"]&Y'\arrow[r,"f"]&Y

\end{tikzcd}
\end{document}
```
First notice that $\dim X-\dim Y=\dim X'-\dim Y'$ if and only if $\dim X'-\dim X=\dim Y'-\dim Y$.
Let $g$ be a flat morphism and all schemes be of finite type over a field $k$. We know that $g'$ is flat. So for arbitrary closed point $y'\in Y'$, we have $\dim g'^{-1}(y')=\dim X'-\dim Y'$. The bottom row composite equals$$\mathrm{Spec}\,k(y')\rightarrow\mathrm{Spec}\,k(f(y'))\rightarrow Y.$$So $g'^{-1}(y')=g^{-1}(f(y'))\times_{k(f(y'))}k(y')$ and $\dim g'^{-1}(y')=\dim g^{-1}(f(y'))$. Since $f(y')$ is also a closed point, $\dim g^{-1}(f(y')=\dim X-\dim Y$, and the proof is done.