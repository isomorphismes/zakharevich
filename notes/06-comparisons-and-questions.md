# Comparisons and open questions: which equivalence is meant?

First pass, 2026-10-09. Goal: make “scissors congruence,” “motivic equivalence,” and “higher scissors K-theory” precise enough to prevent false identifications.

## Comparison diagram

For a field $k$, the following objects need separate definitions:

$$
\begin{array}{ccl}
K_0(\mathrm{Var}_k)
&=& \text{classes of varieties modulo closed-complement cutting};\\
K(\mathrm{Var}_k)
&=& \text{one of the geometric K-theory spectra built to lift these classes};\\
K_0(\mathrm{ChowMot}_k)
&=& \text{Grothendieck ring of Chow motives (where defined)}.
\end{array}
$$

The first is a ring of **classes**. The second is a **spectrum** with $\pi_0K(\mathrm{Var}_k)\cong K_0(\mathrm{Var}_k)$ for the intended model. The third is a ring built from motives, with a different congruence relation.

There is a motivic realization in suitable characteristic-zero settings

$$
K_0(\mathrm{Var}_k)\longrightarrow K_0(\mathrm{ChowMot}_k),
$$

subject to its customary hypotheses and conventions. There is **no automatic reverse isomorphism**.

For $k=\mathbb Q$, Hales's exposition uses a motive-valued scissor quotient $K$ and

$$
S_{\mathrm{mot}} = K[\mathbb L^{-1}]\otimes\mathbb Q.
$$

This construction can forget elements of the ordinary Grothendieck ring, first via motivic identifications and again by localization. Calling both objects “the motivic Grothendieck ring” without further qualification is dangerous.

## Five propositions to keep separate

**1.** $X$ and $Y$ are isomorphic as varieties.

**2.** $X$ and $Y$ are piecewise isomorphic (a finite decomposition into paired isomorphic locally closed strata).

**3.** $[X]=[Y]$ in $K_0(\mathrm{Var}_k)$.

**4.** The associated motives have the same **virtual class** in a Grothendieck ring of motives.

**5.** $[X]=[Y]$ after $\mathbb L$-localization, rationalization, or completion.

Typically 1 $\Rightarrow$ 2 $\Rightarrow$ 3. Under a suitably defined realization, 3 $\Rightarrow$ 4, and 3 $\Rightarrow$ 5 when the target maps are defined. Reverse implications require hypotheses and may be false.

Equality of classes in a group completion does **not** formally imply a direct scissors decomposition with no stabilizing terms.

## Elementary worked examples

### Cutting the affine line

For $X=\mathbb A^1_k$, $Z=\{0\}$, the Grothendieck relation reads

$$[\mathbb G_{m,k}]=\mathbb L-1.$$

Over $\mathbb F_q$, counting gives $\#\mathbb G_m(\mathbb F_q)=q-1$, respecting $[\mathbb A^1]\mapsto q$. This tests additivity and point-counting as a **ring map**.

### Projective line

$$[\mathbb P^1_k]=[\mathbb A^1_k]+[\mathrm{pt}]=\mathbb L+1.$$

Over $\mathbb F_q$, this specializes to $q+1$. The fact that both count formulas work **does not prove** that point-counting is an injective invariant of $K_0(\mathrm{Var}_{\mathbb F_q})$.

### Nonzero cubes (Hales)

Set $M=[u^2+3=0]$ and use the [formula derived in the Hales notes](05-hales-motivic-measure.md#worked-example-nonzero-cubes-2-example-211):

$$[\text{nonzero cubes}]=(\mathbb L-1)(1-M/3).$$

Prime-field checks, avoiding characteristic 2 and 3:

| $q$ | $-3$ a square? | $\#M(\mathbb F_q)$ | Predicted nonzero cubes |
| ---: | :---: | ---: | ---: |
| 5 | no | 0 | 4 |
| 7 | yes | 2 | 2 |
| 11 | no | 0 | 10 |
| 13 | yes | 2 | 4 |

This tests that a **single motive-valued expression** remembers field-dependent cases after specialization. The formulas alone are not a proof of the motivic-counting theorem.

### Failure of cancelling $\mathbb L$

For $\alpha\ne0$ with $\mathbb L\alpha=0$, we have $\alpha=0$ in $K_0(\mathrm{Var}_k)[\mathbb L^{-1}]$. Thus the ordinary and localized rings cannot be identified in general.

## Spectra questions

1. **Does higher K-theory distinguish two scissors presentations with the same $K_0$?** Produce a pair of assemblers and compute at least $K_1$.
2. **Can a motivic measure be lifted?** What categorical functor/sequence of functors is needed to get $K(\mathrm{Var}_k)\to K(\mathcal E)$? Read the 2019 derived $\ell$-adic zeta-functions paper.
3. **Which higher group is seen by which invariant?** Compare $K_1$ self-scissors data and the 2024 trace into $H_1(G;\mathbb R)$.
4. **Does making $\mathbb L$ invertible destroy geometric information in positive degrees too?** Define localization at the level of an $E_\infty$-ring spectrum before making claims.
5. **How do squares K-theory's four-term relations compare with assembler finite covers?** Are they compatible through a natural functor, or do they encode different classes of operations?
6. **Which version of “motive” is under discussion?** Chow motives, Voevodsky motives, or $\mathbb A^1$-stable motivic spectra are *not synonyms*. Hales's 2005 paper uses Chow motives and arithmetic motivic measure, while Zakharevich's K-theory **spectra** belong to a different construction. The word “motivic” is not enough to assert a direct equivalence.

## Suggested proof-reading order

- [Hales §2.5–2.6](05-hales-motivic-measure.md): write out the diagram of quotient rings and prove easy commutativity statements.
- [Zakharevich assemblers](02-assemblers-and-k1.md): define $K(\mathcal C)$ and recover its $\pi_0$.
- [Lefschetz motive](03-lefschetz-and-varieties.md): explain noninjectivity of multiplication by $\mathbb L$ using the dimension filtration.
- [Derived zeta functions](04-later-work.md): identify an explicit functor defining the spectrum map.
- [Stable homotopy study](https://github.com/isomorphisms/VanKoughnett): learn the suspension-spectrum, homotopy-orbit and infinite-loop-space tools needed above.

## Status / what is and is not established in these notes

- **Verified from primary descriptions:** titles/authors/publication information, Hales's scissor and motivic formulas, the $K_0$-of-assembler theorem, the abstract-level contributions of the later papers.
- **Worked out directly:** elementary classes of $\mathbb P^1$, $\mathbb G_m$, the finite-field cube counts.
- **Not yet checked line by line from the papers:** exact hypotheses of the assembler and localization theorems, proofs of the spectral sequence, the full relations in $K_1$, and full derivations of spectral lifts of motivic measures.

These are genuine open tasks for a second reading, not proofs already completed.
