# The Grothendieck ring of varieties and the Lefschetz class

First pass, 2026-10-09. Focus: what information survives cutting and pasting, and what information disappears when the affine-line class is inverted?

## Paper 6. *The annihilator of the Lefschetz motive*

**Inna Zakharevich**, [arXiv:1506.06200](https://arxiv.org/abs/1506.06200) (2015), *Duke Mathematical Journal* **166** (2017), issue 11, 1989–2022. [DOI](https://doi.org/10.1215/00127094-0000016X).

### Objects and notation

For a field $k$,

$$
K_0(\operatorname{Var}_k)=
\mathbb Z\langle [X]\text{ for }k\text{-varieties}\rangle/
\left([X]-[Z]-[X\setminus Z]\right)
$$

where $Z\subseteq X$ is closed and isomorphic varieties define the same generator. Multiplication comes from fiber product over $k$:

$$[X][Y]=[X\times_kY].$$

Write $\mathbb L=[\mathbb A^1_k]$ (often called the Lefschetz class). Then

$$
\operatorname{Ann}(\mathbb L)=
\{\alpha\in K_0(\operatorname{Var}_k):\mathbb L\alpha=0\}.
$$

This is the kernel of multiplication by $\mathbb L$ and is what the paper investigates.

A basic identity is $[\mathbb P^n]=1+\mathbb L+\dots+\mathbb L^n$, using the cell decomposition of projective space.

### Why the annihilator is meaningful

A relation $\mathbb L([X]-[Y])=0$ means the products $X\times\mathbb A^1$ and $Y\times\mathbb A^1$ have **equal classes in the Grothendieck ring**, not necessarily that these product varieties are isomorphic or piecewise isomorphic. Even if products are cut-and-paste equivalent, affine-line cancellation need not hold.

When we pass from $K_0(\mathrm{Var}_k)$ to its localization $K_0(\mathrm{Var}_k)[\mathbb L^{-1}]$, any element annihilated by a positive power of $\mathbb L$ becomes zero. Thus localization is not information-neutral.

### Zakharevich's method, at first pass

The paper builds a K-theoretic framework for varieties with a **dimension filtration**, studies a resulting spectral sequence, and identifies graded information in terms of birational data. The homotopy-theoretic structures make failure of affine-line cancellation visible.

A key ingredient in the filtration analysis is the appearance of spaces related to automorphism groups of function fields $k(X)$ for birational classes of $n$-dimensional varieties. Schematically the graded pieces involve suspension spectra built from $B\operatorname{Aut}_k(k(X))$; consult the theorem for its exact wedge, suspension, and basepoint conventions.

This is a striking bridge:

$$
\text{dimension filtration on varieties}
\longrightarrow
\text{birational equivalence classes and field automorphisms}
\longrightarrow
\text{spectral sequence / obstruction}.
$$

**Source-level claim:** the analysis constructs/locates failures of the cut-and-paste cancellation behavior. The inference “the map $\times\mathbb A^1$ should be injective” is **false** in general.

### Questions to settle from proofs

1. What are the exact hypotheses on the base field? In particular, which arguments use characteristic zero and resolution of singularities?
2. State the theorem giving the associated-graded spectrum **literally**, including suspension shifts.
3. Identify the spectral sequence page and the classes whose differentials/extensions detect kernel of $\mathbb L$.
4. Compare the paper's obstruction to Borisov's zero-divisor example and the Larsen–Lunts stable-birational quotient. Do not assume two constructions of zero divisors are the same.
5. Which part of the argument uses geometry of birational maps, and which part uses general facts about K-theory of assemblers?
6. Does an equality after $\mathbb L$-localization say anything useful about equality before localization? Usually no without a torsion-freeness/injectivity hypothesis.

## A comparison with Hales's 2005 motivic construction

Hales writes $\mathbb L=[\mathbb A^1]$ as well, but his motive-valued target imposes additional equivalences (equal virtual Chow motive for smooth projective varieties) and then rationalizes/localizes/completes for counting and volume.

In Zakharevich's paper, the **unlocalized $K_0(\mathrm{Var}_k)$** is mathematically essential precisely because it can see elements annihilated by $\mathbb L$.

Conclusion: similar notation $\mathbb L$ does **not** imply equal ambient rings. A proposed comparison should explicitly specify a map and the equivalence relations factored out.

## Source links

- [Inna Zakharevich, *The annihilator of the Lefschetz motive*](https://arxiv.org/abs/1506.06200)
- [Inna Zakharevich, *The K-theory of assemblers*](https://arxiv.org/abs/1401.3712)
- [Thomas C. Hales, *What Is Motivic Measure?*](https://arxiv.org/abs/math/0312229)
