# Inna Zakharevich: scissors congruence, K-theory, and motives

Working mathematical reading notes, begun 2026-10-09. These are study notes rather than a complete or peer-reviewed bibliography. Original papers and their authors are linked throughout.

## Start here

- [Definitions and conceptual map](notes/00-conceptual-map.md): scissors relations, Grothendieck groups/rings, spectra, and motivic measures.
- [Early polytope and scissors-congruence papers](notes/01-polytopes-and-scissors.md): the 2012/2013 constructions and the 2016 survey.
- [Assemblers and higher K-theory](notes/02-assemblers-and-k1.md): the 2017 assembler construction and the first higher invariant.
- [Grothendieck ring of varieties and the Lefschetz class](notes/03-lefschetz-and-varieties.md): filtration and failure of cancellation.
- [Later and joint work](notes/04-later-work.md): Goncharov, traces, multiplicative structure, and squares categories.
- [Thomas C. Hales, *What Is Motivic Measure?*](notes/05-hales-motivic-measure.md): a likely match for the remembered early-2000s paper by “Thomas” about scissors congruence and motivic equivalence.
- [Comparisons, questions and study tasks](notes/06-comparisons-and-questions.md): what the constructions share and what they do **not** identify.
- [Existing code and related implementations](notes/07-existing-code-and-nearby-software.md): direct Grothendieck-ring solver, symbolic motives, visual scissors congruence, interval exchanges, Sage/polymake and K-theory formalization; explicitly distinguishes these from the still-unverified existence of a full assembler-spectrum implementation.
- [Bibliography / acknowledgments](references.md).

## Main research thread

A scissors relation records that an object is made by decomposing and reassembling pieces. Zakharevich's central move is to retain these relations in a **K-theory spectrum**, not just an abelian group. The classical scissors group becomes degree zero; higher homotopy groups may preserve further geometric data.

Hales's 2005 exposition describes **arithmetic motivic measure**, including scissor rings built from formulas and varieties with additional congruence relations. It is related to the Grothendieck ring of varieties but **is not simply the same object**.

## Identification of the “Thomas” paper

Likely **Thomas C. Hales**, [*What Is Motivic Measure?*](https://arxiv.org/abs/math/0312229), arXiv December 2003; *Bulletin of the American Mathematical Society* **42** (2005), 119–135, [DOI](https://doi.org/10.1090/S0273-0979-05-01053-0). The paper explicitly develops *scissor and congruence relations* and discusses virtual Chow motives. This is a **probable identification**, not a definitive confirmation of the remembered author.

## Conventions

- Notes distinguish definitions/results stated in sources from our extrapolations and open questions.
- “Scissors congruent,” “equal in the Grothendieck ring,” and “equal as virtual Chow motives” are different statements.
- Source links point to publisher pages, arXiv, or the author's public research pages; do not copy full articles into this repository.
