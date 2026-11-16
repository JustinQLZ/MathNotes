#Analysis #Real-Analysis #Harmonic-Analysis  
Here I conclude some core ideas and inequities dealing with convolution of functions. This is motivated by difficulties I encountered concerning checking commutativity of limits, which require lots of estimation of the convolution of some $f$ such that$$
|f(x)|\leq\frac{C}{(1+|x|)^{1+\delta}}
$$and the Gaussian Kernel. So we'll use $f_{\epsilon}=G_{\epsilon}*f$ as an example.

### General Inequity
A. (Hölder) $f\in L^p,g\in L^{p'}$, then $||f\cdot g||_1\leq ||f||_p\cdot||g||_{p'}$.
This can be used to prove the existence of convolution. But we could have better:
**Theorem.** Let $p,q\in[1,\infty]$ and $q=p'$. If $f\in L^p$ and $g\in L^q$, then $h=f*g$ is a uniformly continuous and bounded function.
**Proof.** Apply Hölder's inequity to $f$ and $g(x-\cdot)$, we see that $h$ is bounded. For any $x,z\in \mathbb{R}^d$,$$h(x+z)-h(x)=\int_{\mathbb{R}^d}f(y)[g(x+z-y)-g(x-y)]\,dy=(f*(\tau_zg-g))(x)
$$Apply Hölder's inequity in the same manner we see that$$
|h(x+z)-h(x)|\leq||f||_p\cdot||\tau_zg-g||_q
$$Notice that by symmetry we may assume that $q\neq\infty$. Then the conclusion follows from the [average continuity](On%Average%Continuity%and%Smooth%Approximation.md) of functions in $L^q$.$$\tag*{$\square$}$$B. (Young) $f\in L^p,g\in L^q$, $p,q,r\in [1,\infty]$ satisfying $\frac{1}{r}+1=\frac{1}{p}+\frac{1}{q}$, then$$
||f*g||_r\leq||f||_p\cdot||g||_q
$$In particular, with $r=p,q=1$, we see that $||f*g||_p\leq||f||_p\cdot||g||_q$. With $g$ "good", we often have $f*g\in L^p$ for $f\in L^p$.
C. (Minkowski) For any $p\in [1,\infty]$, $||f*g||_p\leq\int_{\mathbb{R}^d}||f(x-y)g(y)||_{L^p_x}\,dy$.
Then we could try to simplify the inner term by, for example, the [weight trick](The%20Weight%20Function%20Trick%20for%20Estimating%20Integrals.md).
D. (Jessen) $\omega\in L^+(E)$, $\int_E\omega\,dx=1$, $f$ is measurable on $E$, $f(E)\subset [a,b]$, $\varphi$ is convex (bowl-like), if $f\cdot\omega,\varphi\circ f\in L^1(E)$, then $$\varphi\Big(\int_Ef\cdot\omega\,dx\Big)\leq\int_E(\varphi\circ f)\cdot\omega\,dx$$At last, when in desperation, try Jessen.
### Estimating by Parts
**Slogan.** The decay of convolution is controlled by the slower one.
This is particular useful when estimating the speed of decay. The idea is to divide the integral into $|y|<|x|/2$ and $|y|>|x|/2$. In the first part, $|x-y|>|x|-|y|>|x|/2$, so roughly speaking, at infinity $|x|$ is much larger than $|y|$. In the second part, $|y|$ could be large.
With concrete functions, we have$$
\int_{|y|<|x|/2}|f(x-y)|\cdot|G_{\epsilon}(y)|\,dy\leq\int_{|y|<|x|/2}\frac{C\,G_{\epsilon}(y)}{1+|x-y|^{1+\delta}}\,dy\leq\frac{C'}{1+|x|^{1+\delta}}
$$and$$
\int_{|y|>|x|/2}|f(y)|\cdot|G_{\epsilon}(x-y)|\,dy\leq \int_{|y|>|x|/2}\frac{C\,G_{\epsilon}(x-y)}{1+|y|^{1+\delta}}\,dy\leq\frac{C'}{1+|x|^{1+\delta}}
$$so we see that $f_{\epsilon}$ has the same speed of decay as $f$.
Now to see that the decay of convolution may not be controlled by the faster one, consider $e^{-x^2}$ and $\frac{1}{1+x^2}$. Denote $h$ as the convolution. For $x\gg 1$,$$
h(x)\geq\int_{x-1}^{x}\frac{e^{-(x-y)^2}}{1+y^2}\,dy\geq\frac{e^{-1}}{1+x^2}
$$
### Switching Variables
First recall a basic inequity$$
(a+b)^p\leq 2^p(a^p+b^p),\;a,b\geq0,\ p\in\mathbb{R},p^2+a^2+b^2\neq0.
$$So$$
1+|x|^p\leq 1+2^p(|y|^p+|x-y|^p)\leq C(1+|y|^p)(1+|x-y|^p)
$$and therefore$$
\frac{1}{1+|x-y|^p}\leq C\frac{1+|y|^p}{1+|x|^p}
$$This is a variation of Peetre's Inequity.
We expect $1+|y|^p$ to be absorbed by the good factor of convolution.$$
|f_{\epsilon}(x)|\leq\int_{\mathbb{R}}\frac{C}{1+|x-y|^{1+\delta}}G_{\epsilon}(y)\,dy\leq\frac{C}{1+|x|^{1+\delta}}
$$
