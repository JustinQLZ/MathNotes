#Algebraic-Geometry 
This list is a lite version of [Section 65.4 (02WE): Lists of useful properties of morphisms of schemes—The Stacks project](https://stacks.math.columbia.edu/tag/02WE).

### Properties of morphisms which are stable under base extension and composition:
1. closed, open and locally closed immersions
2. quasi-compact
3. universally closed, universally open, universal homeomorphism
4. (quasi-)separated, proper, flat, smooth
5. surjective, universally injective
6. (quasi-)affine
7. (locally) of finite type, (locally) quasi-finite, finite, integral

 The property of a morphism being (locally) projective is stable under base extension and we have [Lemma 29.43.14 (0C4P)—The Stacks project](https://stacks.math.columbia.edu/tag/0C4P). But if we use the definition of Hartshorne, projective is stable under composition in any cases.
 
**Remark.** As intuitions: algebraic properties stable under tensor products (flatness, finiteness, etc.) should be stable under base extension, properties motivated by geometry (smoothness) or topology (separatedness, properness) should be stable under base extension, and those defined via base extension (projective relates to projective n-spaces) or intentionally defined to be stable under base extension (universally xxx) should be stable under base extension.

Also here's a formal proposition from Hartshorne Ex. II.4.8:
**Proposition.** Let $\mathscr{P}$ be a property of morphism of schemes such that:
1. a closed immersion has $\mathscr{P}$;
2. a composition of two morphisms having $\mathscr{P}$ has $\mathscr{P}$;
3. $\mathscr{P}$ is stable under base extension.
Then
4. a product of morphisms having $\mathscr{P}$ over $S$ has $\mathscr{P}$;
5. if $f:X\rightarrow Y$ and $g:Y\rightarrow Z$ are two morphisms, and if $g\circ f$ has $\mathscr{P}$ and $g$ is separated, then $f$ has $\mathscr{P}$;
6. If $f:X\rightarrow Y$ has $\mathscr{P}$, then $f_{red}:X_{red}\rightarrow Y_{red}$ has $\mathscr{P}$.
