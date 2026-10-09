# Zakharevich: motives, higher invariants, and subsequent joint work

First pass, 2026-10-09. This is a selective path through the papers most directly connected to scissors congruence, spectra, Grothendieck rings, and motivic measures. It is **not** a comprehensive bibliography.

## Paper 7. *Derived ℓ-adic zeta functions* (2019)

**Jonathan Campbell, Jesse Wolfson, Inna Zakharevich**. *Advances in Mathematics* **354** (2019), article 106760. [Publisher / DOI](https://doi.org/10.1016/j.aim.2019.106760); [public manuscript](https://par.nsf.gov/servlets/purl/10147871).

This is one of the strongest bridges from Hales's question “what is motivic measure?” to Zakharevich's higher K-theoretic framework.

### Key point

A classical motivic measure takes a class $[X]$ in $K_0(\mathrm{Var}_k)$ to a class in another Grothendieck group (often by cohomology, point counting, or a zeta function). The authors give a recipe for **lifting appropriate motivic measures to maps of K-theory spectra**:

$$
K_0(\mathrm{Var}_k)\longrightarrow K_0(\mathcal E)
\quad\leadsto\quad
K(\mathrm{Var}_k)\longrightarrow K(\mathcal E).
$$

The right arrow requires **more structure** than merely knowing the left arrow is a group/ring homomorphism: a construction compatible with the categorical cut-and-paste relations is needed.

The special examples include $\ell$-adic local zeta functions over finite fields (using continuous Galois representations / Frobenius data), and compactly supported Euler characteristic for complex varieties.

The resulting maps prove that the higher K-theory spectrum of varieties contains nontrivial geometric data in positive homotopy groups.

### Technical questions

- Identify the specific source category (subtractive/SW-category) and target Waldhausen category.
- Why is compactly supported étale cohomology not functorial enough as given? The paper uses **compactification data** to repair the variance/functoriality needed for its W-exact functor.
- Explain the derived $\ell$-adic zeta-function target without collapsing it to the numerical Weil zeta function.
- How is the Frobenius action retained in $K_1$, and what additional information is visible beyond $\pi_0$?

## Paper 8. *Hilbert's third problem and a conjecture of Goncharov*

**Jonathan A. Campbell and Inna Zakharevich**. [arXiv:1910.07112](https://arxiv.org/abs/1910.07112) (2019), *Advances in Mathematics* **451** (2024), article 109757. [DOI](https://doi.org/10.1016/j.aim.2024.109757).

The paper reduces the generalized Hilbert's third problem—whether a prescribed family of generalized Dehn invariants suffices to distinguish scissors classes—to **injectivity of certain Cheeger–Chern–Simons invariants**. It also establishes a version of Goncharov's conjectural relationship between scissors congruence groups of polytopes and algebraic $K$-theory of $\mathbb C$.

The important distinction is logical:

- The *reduction* to injectivity is a theorem.
- Injectivity itself should not be assumed settled merely from this reduction.

**Reading questions:** what is the Dehn complex, how is it iterated by dimensions/geometries, and which graded piece of $K_*(\mathbb C)$ appears? Which regulators or Chern–Simons maps would detect missing scissors invariants?

## Paper 9. *E_\infty-ring structures on the K-theory of assemblers and point counting*

**Inna Zakharevich**, [arXiv:2209.08640](https://arxiv.org/abs/2209.08640) (2022).

Provides multiplicative structure on K-theory of assemblers with appropriate monoidal data. This is a necessary step if a categorified motivic measure is meant to preserve multiplication and not just cut-and-paste addition. Point-counting is investigated at higher K-theoretic levels.

**Question:** under exactly what hypotheses does the point-counting construction become a morphism of $E_\infty$ ring spectra rather than merely a map of spectra?

## Paper 10. *A trace map on higher scissors congruence groups*

**Anna Marie Bohmann, Teena Gerhardt, Cary Malkiewich, Mona Merling, Inna Zakharevich**. [arXiv:2303.08172](https://arxiv.org/abs/2303.08172) (2023), *International Mathematics Research Notices* **2024** issue 18, 12683–12710. [DOI](https://doi.org/10.1093/imrn/rnae153).

The authors construct an explicit, computable trace from higher scissors-congruence groups of polyhedra to group homology and exhibit nonzero higher classes. They also identify the K-theory of polyhedra as a **homotopy-orbit spectrum**.

For an action by a group $G$ of isometries, and volume as the measure, a representative instance has shape

$$
\operatorname{tr}\colon K_n(\mathcal P^X_G)\longrightarrow H_n(G;\mathbb R).
$$

The work is motivated in part by the absence of a general Dennis-trace theory for all cut-and-paste K-theory. It does **not** construct a Dennis trace in total generality.

**Question:** compute the trace on an explicit loop arising from a piecewise isometry and compare with an interval exchange.

## Paper 11. *Algebraic K-theory for squares categories*

**Jonathan Campbell, Josefien Kuijper, Mona Merling, Inna Zakharevich**. [arXiv:2310.02852](https://arxiv.org/abs/2310.02852) (2023); *Annals of K-Theory* **11** (2026), issue 1, 1–36.

The authors introduce *squares K-theory*, which allows a four-term relation arising from a good square diagram:

$$[A]+[D]=[B]+[C].$$

This generalizes the usual three-term exact/subtractive relation. Applications include cut-and-paste constructions for smooth manifolds and complete varieties, and a **derived motivic measure** valued in K-theory of homotopy sheaves.

**Reading questions:**

1. What is a “good square” as a diagrammatic axiom?
2. How do closed/open decomposition and pushout/pullback squares fit the same pattern?
3. What is the receiving spectrum for the derived motivic measure?
4. Does this resolve limitations of the assembler model, or provide a different generality?

## Research arc

$$
\text{scissors relations}
\to \text{assemblers / squares}
\to K(\mathcal C)
\to \text{traces, zeta-function maps, derived measures}.
$$

These developments are not simply a rephrasing of Hales's arithmetic motivic measure. They investigate **homotopical refinements**, whose relationship to individual motivic realizations requires actual maps of spectra and hypotheses.

## Sources

- [2019 derived zeta functions](https://doi.org/10.1016/j.aim.2019.106760)
- [2024 Goncharov paper](https://doi.org/10.1016/j.aim.2024.109757)
- [2022 E-infinity paper](https://arxiv.org/abs/2209.08640)
- [2024 trace paper](https://doi.org/10.1093/imrn/rnae153)
- [2026 squares categories](https://arxiv.org/abs/2310.02852)
