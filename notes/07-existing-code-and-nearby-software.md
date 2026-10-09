# Existing code and nearby computational work (survey, 2026-10-09)

**Scope:** software implementing mathematical ideas in or near Inna Zakharevich's scissors congruence, assembler K-theory, and Grothendieck-ring work. This survey separates **direct implementations** of cut-and-paste geometry / motivic class calculations from *mathematical infrastructure* and formalization. Links point to original projects; none of their source has been copied into this repository. The surveyed projects were inspected through their publicly accessible repository README and, for several, code files. We did not install or execute them.

**Main finding:** substantive computation exists for polygon dissection, interval exchanges, Grothendieck classes of specific varieties, Chow-motive expressions, Hodge realizations, and polyhedral operations. I could **not confirm** a published, general-purpose implementation of Zakharevich's **assembler-to-K-theory-spectrum** functor, nor a program computing the higher homotopy groups of general assemblers. That is a search limitation, not a proof none exists.

## Closest matches

### 1. Jesse Vogel's Grothendieck-ring solver — direct algebraic cut-and-paste

- Repository: https://github.com/jessetvogel/grothendieck-ring
- Author: **Jesse Vogel**, whose solver repository is explicitly cited in a peer-reviewed paper, [Márton Hablicsek and Jesse Vogel, *Virtual Classes of Representation Varieties of Upper Triangular Matrices via Topological Quantum Field Theories*](https://sigma-journal.com/2022/095/) (*SIGMA* **18** (2022), 095, [arXiv:2008.06679](https://arxiv.org/abs/2008.06679)).
- Related research: [Jesse Vogel, *On the motivic Higman conjecture*](https://doi.org/10.1016/j.jalgebra.2024.03.024) (*Journal of Algebra* **651** (2024), 19–69) gives explicitly algorithmic motivic-class and E-polynomial calculations, including representation varieties in selected low ranks; [*Motivic invariants of character stacks*](https://jessetvogel.nl/academic/files/theses/PhD_Thesis_Jesse_Vogel.pdf), Vogel's thesis, develops the computational backdrop. Also see [Andreas Gross, Leo Herr, David Holmes, Pim Spelier, Jesse Vogel, *The log Grothendieck ring of varieties*](https://doi.org/10.1112/blms.70204), published 2026, for extensions to log varieties (not claimed implemented by the solver).
- Code: [solver/grothendieck_solver.py](https://github.com/jessetvogel/grothendieck-ring/blob/master/solver/grothendieck_solver.py), plus notebooks.
- Language: Python with SymPy, IPython.
- Observed structure: `System(gens, eqs, op_eqs)` for varieties described by polynomial **equations** and **inequations**; `Solver.compute_grothendieck_class(system)` uses explicit rewrite tactics. The tactics in source include elimination of linear variables, factoring, product decompositions, quadratic hypersurfaces, Gröbner bases and a closed/open split for `f != 0`.
- README's actual example: the complex variety defined by `xy=1` with `x != 3` is assigned `q - 2`, where `q=[A^1_C]`.
- Closest connection: the relation `[X]=[Z]+[X\\setminus Z]` is embodied by the decomposition algorithm. It is **not** the assembler spectrum, but could provide a concrete finite scissor-relation testbed.
- Limits: tactics are partial, and code returns `None` when unable to reduce an input. Not every class in `K_0(Var_C)` is a polynomial in `q`; the solver cannot legitimately represent the general ring that way. No root LICENSE file observed when surveying the repository; **link/reference only** unless permission is established.

### 2. CIAMOD *motives* — symbolic Chow-motive expressions

- Repository: https://github.com/CIAMOD/motives
- Source package: [motives](https://github.com/CIAMOD/motives/tree/master/motives).
- Authors (as listed by project): **Daniel Sánchez Sánchez, David Alfaya Sánchez, Jaime Pizarroso Gonzalo**.
- Paper: [Daniel Sanchez, David Alfaya, Jaime Pizarroso, *Motives meet SymPy: studying λ-ring expressions in Python*](https://doi.org/10.3934/era.2025093), *Electronic Research Archive* **33** (2025), 2118–2147; [arXiv:2501.00563](https://arxiv.org/abs/2501.00563).
- Language: Python/SymPy. Repository README labels its current release `0.3.3`, GPLv3.
- Computes symbolic simplification/comparison of expressions in λ-rings, Grothendieck ring of Chow motives, alternating/symmetric powers, and classes of selected moduli spaces and stacks. Implements mathematical identities rather than generic numeric point counting.
- **Connection to Hales:** he imposes motivic/Chow-motive congruence in his motive-valued measure, so this is closer to the **target** of a motivic measure than the raw Grothendieck ring `K_0(Var_k)`.
- **Important distinction:** this is not an implementation of Zakharevich's assembler spectrum or a proof that equality in a Chow-motive realization implies equality in `K_0(Var_k)`.

### 3. Dima Smirnov's interactive scissors-congruence demonstration — geometric cut/move animation

- Repository: https://github.com/dmsm/scissors-congruence
- Demo: https://dmsm.github.io/scissors-congruence/
- Source: [js/polygons.js](https://github.com/dmsm/scissors-congruence/blob/gh-pages/js/polygons.js), [js/transformations.js](https://github.com/dmsm/scissors-congruence/blob/gh-pages/js/transformations.js).
- JavaScript with Two.js, PolyK.js, jQuery and math.js. Interactive drawings of polygons; decomposition and animated transformation based on the Wallace–Bolyai–Gerwien theorem.
- **Connection to Zakharevich:** visual examples of `[P]=sum_i [P_i]` with the additional identification of pieces by rigid isometries; excellent small `K_0` examples. It is not a higher-K-theory implementation.
- **Caution:** polygon geometry uses numbers in the browser. An animation is not a formal exact certificate of disjoint covering or rigid-motion equality. A root LICENSE file was not observed; don't copy source solely on the presumption that GitHub visibility permits it.

### 4. `flatsurf/intervalxt` — interval exchanges (direct link to Zakharevich's `K_1` example)

- Repository: https://github.com/flatsurf/intervalxt
- Language: **C++**, with Python wrappers; GPL-3.0-or-later.
- Implements interval exchange transformations (IETs), Rauzy induction and the Boshernitzan algorithm. Some component-minimality tests are explicitly documented by maintainers as possibly incomplete.
- **Strong mathematical link:** [Zakharevich, *On K1 of an assembler* §4](https://arxiv.org/abs/1506.06197) relates the first K-group of the assembler of intervals to the **abelianization of the group of interval exchange transformations**. That makes concrete IET code unusually relevant: its self-cutting/reassembly permutations represent the geometric data feeding `K_1`.
- Not a program calculating `K_1` for arbitrary assemblers; one still must implement the correct categorical generators, relations, and their map into the mathematical abelianization.

### 5. `flatsurf/surface-dynamics` and SageMath's interval exchange implementation

- Repository: https://github.com/flatsurf/surface-dynamics (SageMath/Python; GPL-2.0-or-later).
- Docs: https://flatsurf.github.io/surface-dynamics/
- Sage has IET permutations, Rauzy diagrams, induced maps, and methods to display interval exchanges. See the [Sage documentation](https://wiki.sagemath.org/dynamics/examples).
- This is an alternative/complement to `intervalxt` when testing permutation conventions, composing cut-and-paste operations, and examining dynamical examples.

## Motivic realizations and verification of weaker invariants

### 6. Pieter Belmans's *Hodge diamond cutter*

- Repository: https://github.com/pbelmans/hodge-diamond-cutter
- Author: **Pieter Belmans**; Sage/Python; GPLv3; citation [Zenodo DOI 10.5281/zenodo.3893509](https://doi.org/10.5281/zenodo.3893509).
- Computes and manipulates Hodge diamonds for classes of smooth projective varieties.
- A **realization/invariant** of varieties, not an exhaustive test of scissors equivalence or of class equality in the Grothendieck ring.
- Companion verification project by **Pieter Belmans, Jishnu Bose, Sarah Frei, Benjamin Gould, Alicia Lamarche, Jack Petok, Cristian Rodriguez Avila, James Hotchkiss and Saket Shah**: [pbelmans/decomposing-fano-schemes](https://github.com/pbelmans/decomposing-fano-schemes). It checks an image of a proposed Grothendieck-ring identity **after applying the E-polynomial motivic measure**. Thus it verifies a necessary specialized equality, not necessarily equality in the source ring.

### 7. SageMath: point counting on finite-field schemes

- Software: https://github.com/sagemath/sage
- Documentation: https://doc.sagemath.org/html/en/reference/schemes/sage/schemes/generic/scheme.html
- Example API: a scheme over `GF(q)` can support `count_points(n)`, counting over the finite extensions of degree at most `n`.
- **Link to Hales/Denef–Loeser:** finite-field point counting is a **motivic measure** (where defined) sending classes to integers. It is **not injective** in general, so equal point counts cannot establish equality in the original Grothendieck ring.

## Computational geometry that could supply correct pieces

### 8. `polymake`

- Repository: https://github.com/polymake/polymake (read-only GitHub mirror of upstream).
- Documentation: https://polymake.org/
- Handles polyhedra, faces, incidences, subdivisions, volumes, and triangulations.
- Its `congruent(P1,P2)` returns a **scale factor** for an isomorphism induced by a scaled orthogonal matrix. For the usual scissors-congruence notion, **only factor 1** is a rigid isometry. Similarity with scale != 1 is not allowed.
- In practice useful for producing and checking polyhedral decompositions, but it does **not** by itself compute Dehn invariants, scissors groups, or `K(assembler)`.
- Precise bookkeeping is required for open/closed boundary strata, which ordinary mesh/render APIs may not preserve.

### 9. SageMath polyhedra

- Source: https://github.com/sagemath/sage/tree/develop/src/sage/geometry/polyhedron
- Exact rational geometry is supported with `base_ring=QQ` and algebraic reals with `AA`, while `RDF` uses floating-point approximation.
- Use **exact** coordinates/certificates for mathematical decisions; use floating point only for rendering.

## K-theory formalization, but not Zakharevich's spectrum

### 10. UniMath's Grothendieck-group formalization

- Repository: https://github.com/UniMath/UniMath/tree/master/UniMath/Ktheory
- [GrothendieckGroup.v](https://github.com/UniMath/UniMath/blob/master/UniMath/Ktheory/GrothendieckGroup.v), credited in that directory to **Daniel R. Grayson**.
- Coq formalization of the Grothendieck group of an **exact category**.
- Useful as a model for a *proof assistant representation of a `K_0` quotient*. An exact category and an assembler are different inputs, and this package does **not** supply the assembler's Waldhausen S-construction or its higher homotopy groups.

## What was not found, or must not be conflated

- No confirmed general executable implementation of Zakharevich's `Assembler -> Spectrum` functor.
- No confirmed formalization of **her assembler axioms and associated spectrum** in Agda, Idris/Idriç, Lean or Coq.
- No verified general-purpose executable 3D **Dehn-invariant** classifier that produces exact certificates. Numerical dihedral angles alone cannot decide equality in the abstract tensor product containing Dehn invariants.
- **No** assertion that all above projects compute the same ring, much less the same spectrum.
- IET simulation is mathematically close to the **interval assembler's `K_1`**, not a proof of a general spectral claim.
- Hodge polynomials, point counts, and Chow-motive realizations can **lose information** present in `K_0(Var_k)`.

## Practical conceptual bridge between the code bases

The strongest common model is a **record of a cut with a witness**, not just a drawing or symbolic result:

```
Geometry / variety X
  -> certified family of allowed disjoint pieces (Xi -> X)
  -> relation [X] = sum [Xi]                 (K0)
  -> permitted identifications of pieces    (isomorphism / isometry)
  -> sequence or loop of such relations     (candidate data for K1)
  -> realization: Chow motive, Hodge, counts (generally non-injective)
```

The honest boundary between software and mathematical theorem would be a typed or proof-checked certificate that each dissection covers exactly what its parent claims, and that each piece is identified by an **allowed** morphism. Then `K_0` relations and finite approximations to `K_1` generators might be computed without equating numerical visual coincidence with equality of geometric objects.

### Concrete experiments (not work already performed)

1. Start with `dmsm` polygon demonstrations and make exact affine transformations plus a decomposition certificate (note third-party license conditions).
2. Reproduce Vogel's `xy=1, x!=3 -> q-2` in an independently specified finite Grothendieck presentation; derive the closed/open relation in a transparent trace.
3. Compare IET permutation composition in Sage and `intervalxt`, then map a simple two- or three-interval exchange into the pair-of-morphisms picture of Zakharevich's `K_1` paper.
4. For selected varieties, compare the class computed by Vogel's solver, its Chow-motive expression in `motives` (where expressible), its Hodge realization, and finite-field point counts (where applicable). Preserve the *map and its assumptions* at each stage.
5. Add a tiny assembler in a proof assistant, but **do not claim** it computes a spectrum until the categorical/simplicial construction has been formally provided.

## Attribution and source licenses

Thanks individually to **Jesse Vogel**, **Daniel Sánchez Sánchez**, **David Alfaya Sánchez**, **Jaime Pizarroso Gonzalo**, **Dima Smirnov**, **Pieter Belmans**, **Daniel R. Grayson**, and contributors to the `flatsurf`, `SageMath`, `polymake`, and `UniMath` projects. Thanks also to the explicitly named authors of the Fano-scheme calculation above.

The cited source repositories retain their own copyright and licenses; the existence of a GitHub repository does not grant a copying license. The purpose here is **research and attribution**, not code redistribution. For more contributors, follow each project's `AUTHORS`, paper bibliography, and official attribution files before copying anything.
