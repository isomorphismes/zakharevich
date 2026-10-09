# Zakharevich: polygons, polytopes, and scissors congruence

First pass, 2026-10-09. Papers are cited using author-preferred public name **Inna Zakharevich**. Abstract-level results are distinguished from our questions.

## Historical test case: Hilbert's third problem

Two polyhedra are scissors congruent when one can partition both into finitely many pieces that pair up under allowed geometric motions. Volume is necessary for scissors congruence, but in dimension three it is not sufficient: Dehn's invariant obstructs scissors congruence even when volumes agree. The same example motivates looking for *complete* families of invariants and for functorial organizing principles.

Distinguish:

- congruence of individual objects;
- scissors congruence after finite decompositions and reassembly;
- equality in the *group completion* of scissor classes.

These notions need not all coincide without additional hypotheses.

For the historical overview and subtleties see Zakharevich's survey.

## Paper 1. *Scissors Congruence as K-theory*

**Inna Zakharevich**, [arXiv:1101.3833](https://arxiv.org/abs/1101.3833) (first posted 2011); *Homology, Homotopy and Applications* **14** (2012), issue 1, 181–202. [DOI](https://doi.org/10.4310/HHA.2012.v14.n1.a9).

**Main result, as stated in the abstract.** A Waldhausen-category construction realizes traditional scissors congruence groups as the *degree-zero* part of algebraic K-theory. The upgrade from a group to a K-theory space/spectrum opens the possibility of higher invariants.

### Structural idea

Ordinary cut-and-paste encodes geometric decomposition and congruence into relations between formal classes. Waldhausen K-theory instead presents appropriate categorical data so that group completion and stabilization supply additional homotopy information.

An initial conceptual sketch (not the full category definition):

$$
\{\text{polytopes, cuts, identifications}\}
\rightsquigarrow\mathcal W
\rightsquigarrow K(\mathcal W),
\quad \pi_0 K(\mathcal W)\cong \text{scissors group}.
$$

### Detailed-reading tasks

1. Record the *precise* objects, weak equivalences, and cofibrations of the Waldhausen category.
2. Check what happens with boundary strata and whether lower-dimensional pieces are discarded or retained.
3. Prove from the definitions that the induced $K_0$ relation agrees with scissors decomposition.
4. Identify a computable nonzero positive-degree group.

## Paper 2. *Simplicial Polytope Complexes and Deloopings of K-theory*

**Inna Zakharevich**, [arXiv:1102.4278](https://arxiv.org/abs/1102.4278) (2011); *Homology, Homotopy and Applications* **15** (2013), issue 2, 301–330. [DOI](https://doi.org/10.4310/HHA.2013.v15.n2.a18).

**Main results, per abstract.** Formulas for the delooping of a simplicial polytope complex and for the cofiber of a morphism of simplicial polytope complexes. Classical and higher scissors groups of polytopes in sufficiently structured homogeneous $n$-manifolds are determined by local properties.

### What needs unpacking

- A *polytope complex* in the 2011 formulation has geometrically meaningful vertical decomposition arrows and horizontal congruence morphisms; the source treats these using double categories.
- A cofiber construction addresses what geometric information is contributed or removed by a map of complexes.
- Delooping is not cosmetic: it realizes the stable-homotopy structure underlying successive K-groups.

**Study question:** what does “determined by local properties” mean precisely? Locate the theorem's hypotheses on the homogeneous manifold, the allowed polytopes, and the local data. Do not infer unrestricted local-to-global behavior.

## Paper 3. *Perspectives on scissors congruence*

**Inna Zakharevich**, *Bulletin of the American Mathematical Society* **53** (2016), 269–294. [DOI](https://doi.org/10.1090/bull/1527).

A survey recommended as the easiest entry into the sequence. Classical problems include Euclidean, spherical, and hyperbolic polytopes, Dehn invariants, and the role of algebraic K-theory. The later Grothendieck-ring viewpoint generalizes “cutting and pasting” beyond polytopes.

### Reading prompts

- What equivalence relation exactly characterizes each scissors group?
- Which homomorphisms are **known complete**, which are only obstructions?
- How do the classical invariants connect to group homology, Bloch groups, and algebraic K-groups?
- Why should stable homotopy be a useful *upgrade* rather than a different notation for the same zero-degree group?

## Thesis connecting these papers

**Inna Zakharevich**, [*Scissors Congruence and K-theory*](https://pi.math.cornell.edu/~zakh/thesis.pdf), MIT PhD thesis, 2012. The thesis supplies a systematic account of the Waldhausen construction, operations on scissors problems, and spectra. It is a useful long-form companion; it is **not** to be reproduced in this repository.

## Cross references

- [Basic definitions](00-conceptual-map.md)
- [Assemblers](02-assemblers-and-k1.md)
- [Goncharov and Dehn complexes](04-later-work.md)
