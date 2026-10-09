# Assemblers and their higher K-theory

First pass, 2026-10-09. The central construction is a **spectrum** attached to a categorical system of finite, disjoint covers.

## Paper 4. *The K-theory of assemblers*

**Inna Zakharevich**, [arXiv:1401.3712](https://arxiv.org/abs/1401.3712) (submitted 2014), *Advances in Mathematics* **304** (2017), 1176–1218. [DOI](https://doi.org/10.1016/j.aim.2016.08.045).

**Claim of the paper's abstract:** an assembler formally encodes cutting and pasting. Its K-theory spectrum has

$$
\pi_0 K(\mathcal C)\ \cong\
\mathbb Z\langle\operatorname{Ob}(\mathcal C)\rangle \big/
\big\langle [A]-\sum_{i=1}^{r}[A_i]\ 
\big|\ \{A_i\to A\}\text{ an allowed disjoint cover}\big\rangle ,
$$

under the paper's assumptions. Positive homotopy groups furnish further geometric invariants. There are analogues of Quillen's **localization** and **dévissage** theorems.

### Categorical model

An assembler is a small Grothendieck site with added restrictions ensuring the morphisms and coverings behave like inclusions and finite disjoint decompositions. At minimum, track these three sorts of input:

1. Objects: geometric pieces or algebraic varieties.
2. Morphisms: inclusion-like arrows (monomorphisms in the assembler setting).
3. Covering families: finite families of mutually disjoint pieces allowed to reconstruct a target.

An assembler is not merely a set of relations. Different categories can have the **same presentation of $\pi_0$** but distinct higher K-theory because the morphisms and the compatibility of decompositions differ.

### Examples highlighted by the paper

- Polytopes and their scissors-congruence groups.
- Algebraic varieties and their Grothendieck group, the additive part of $K_0(\mathrm{Var}_k)$.

For multiplicative structure we should distinguish an arbitrary assembler spectrum from the extra compatible monoidal data that produce an $E_\infty$-ring spectrum; see the later paper below.

### Mathematical tasks

- Extract the full definition of assembler, including initial object, pullbacks/refinements, and every disjointness requirement.
- Work through a *finite-set* assembler. Determine the resulting spectrum; do not assume a result merely from its $\pi_0=\mathbb Z$.
- Find and formulate the localization sequence. Which subassembler is being quotiented, and what is the homotopy cofiber?
- For varieties, verify rigorously that the relevant cover relation gives $[X]=[Z]+[X\setminus Z]$ despite this being a **closed-plus-open** decomposition.
- Determine which input data control positive $\pi_n$ and whether refinements induce equal higher classes.

## Paper 5. *On K_1 of an assembler*

**Inna Zakharevich**, [arXiv:1506.06197](https://arxiv.org/abs/1506.06197) (2015), *Journal of Pure and Applied Algebra* **221** (2017), issue 7, 1867–1898.

The paper describes generators and some relations in $K_1$ for a class of Waldhausen categories with split cofibrations and applies the machinery to assemblers. Geometrically, the degree-one information is related to **self-scissors-congruences** and examples such as interval-exchange constructions.

**Caution:** the paper advertises a *partial* description of relations; it should not be paraphrased as a full generators-and-relations theorem in general.

### A self-scissors-congruence (intuition, not the formal definition)

Start with $X$, partition it into pieces $X_i$, transport/identify the pieces, and reassemble an object identified with $X$:

$$
X\ \xleftarrow{\text{decomposition}}\ \coprod_i X_i
\ \xrightarrow{\text{piecewise transport}}\ X.
$$

The resulting loop-like datum may contribute to $K_1$. A self-map that acts trivially on the *class* $[X]$ need not act trivially on the **space** or spectrum whose $\pi_0$ contains $[X]$.

This is the key distinction between a relation in $K_0$ and a path/loop or coherence phenomenon.

### Reading tasks

- Copy the precise definition of a generator and compare with an elementary interval exchange.
- Write down the specified relations, clearly marking any relations that remain unknown.
- Check whether $\pi_1$ is constructed using plus-constructions, Waldhausen $S_\bullet$, or explicit loops in the underlying space.
- Find one fully calculated nonzero $K_1$ example.

## Subsequent multiplicative development

**Inna Zakharevich**, [*E_\infty-ring structures on the K-theory of assemblers and point counting*](https://arxiv.org/abs/2209.08640) (arXiv 2022).

Compatible multiplicative/monoidal structure upgrades assembler K-theory to an $E_\infty$-ring spectrum and permits comparisons with point-counting invariants of varieties. This matters because $K_0(\mathrm{Var}_k)$ is a **ring** and not only an additive group.

**Question:** what is gained at the spectrum level from multiplicativity compared with a ring homomorphism out of $K_0$?

## Connection to spectra lectures

To understand what Zakharevich actually adds beyond $\pi_0$, follow the construction
$\mathcal C\mapsto K(\mathcal C)$ through at least one suspension/delooping and relate it to $\Omega^\infty K(\mathcal C)$, the underlying infinite loop space. See [the user's stable homotopy lecture-notes repository](https://github.com/isomorphisms/VanKoughnett).

## Sources

- [Zakharevich (2017), publisher](https://www.sciencedirect.com/science/article/pii/S0001870816311720)
- [Zakharevich (2015/17), K1](https://arxiv.org/abs/1506.06197)
- [Zakharevich (2022), E-infinity and point counting](https://arxiv.org/abs/2209.08640)
