# Reference code

The four requested projects, registered on 2026-10-09 as **Git submodules pinned to exact upstream commits**. These entries reference the original repositories; their source files are not vendored or relicensed by this repository. GitHub opens each submodule at its recorded revision. A submodule checkout obtains the actual source locally.

| Directory | Project and purpose | Pinned revision |
| --- | --- | --- |
| [grothendieck-ring](https://github.com/jessetvogel/grothendieck-ring/tree/69cbb069723514dcfc17b6b4cdd248657133fd30) | Jesse Vogel's Python/SymPy solver for selected Grothendieck classes of varieties | `69cbb069723514dcfc17b6b4cdd248657133fd30` |
| [ciamod-motives](https://github.com/CIAMOD/motives/tree/6a4565a870618e677e90d66c1f10f4f67538ccad) | CIAMOD's symbolic Chow-motive and lambda-ring expressions | `6a4565a870618e677e90d66c1f10f4f67538ccad` |
| [scissors-congruence](https://github.com/dmsm/scissors-congruence/tree/0cbc5201da2650899a9011ad97ebb409aab64762) | Interactive polygon-dissection demonstration | `0cbc5201da2650899a9011ad97ebb409aab64762` |
| [unimath](https://github.com/UniMath/UniMath/tree/62837f6a3967df2568e2580ab8a6dbc5878d1011) | UniMath, including Daniel R. Grayson's K-theory material: number seven in the requested list | `62837f6a3967df2568e2580ab8a6dbc5878d1011` |

The machine-readable version record is [sources.lock.json](sources.lock.json). Mathematical comparisons and limitations are in the [software survey](../notes/07-existing-code-and-nearby-software.md).

## Source entry points

- **Grothendieck-ring solver:** [solver/grothendieck_solver.py](https://github.com/jessetvogel/grothendieck-ring/blob/69cbb069723514dcfc17b6b4cdd248657133fd30/solver/grothendieck_solver.py). Begin with `System`, `Solver.compute_grothendieck_class`, and the closed/open decomposition tactics. Its incomplete tactics are not a decision procedure for equality in the entire Grothendieck ring.
- **CIAMOD motives:** [motives/](https://github.com/CIAMOD/motives/tree/6a4565a870618e677e90d66c1f10f4f67538ccad/motives), with [tests/](https://github.com/CIAMOD/motives/tree/6a4565a870618e677e90d66c1f10f4f67538ccad/tests). Its Chow-motive expressions must not be confused with unrestricted classes in the Grothendieck ring of varieties.
- **Scissors congruence:** [js/polygons.js](https://github.com/dmsm/scissors-congruence/blob/0cbc5201da2650899a9011ad97ebb409aab64762/js/polygons.js) and [js/transformations.js](https://github.com/dmsm/scissors-congruence/blob/0cbc5201da2650899a9011ad97ebb409aab64762/js/transformations.js). Treat the browser animation separately from exact mathematical certificates.
- **UniMath K-theory:** [UniMath/Ktheory/GrothendieckGroup.v](https://github.com/UniMath/UniMath/blob/62837f6a3967df2568e2580ab8a6dbc5878d1011/UniMath/Ktheory/GrothendieckGroup.v) and its [README](https://github.com/UniMath/UniMath/blob/62837f6a3967df2568e2580ab8a6dbc5878d1011/UniMath/Ktheory/README.md). The full UniMath repository is referenced so that surrounding library imports are preserved. This is a Grothendieck-group formalization for exact categories, not a formalization of Zakharevich's assembler-to-spectrum construction.

## Obtain the pinned source

From the root of an existing checkout of this repository:

```sh
git submodule update --init -- \
  "reference code/grothendieck-ring" \
  "reference code/ciamod-motives" \
  "reference code/scissors-congruence" \
  "reference code/unimath"
```

This checks out the recorded commits, not whatever the upstream branches later become. Consult each project's own build instructions before installing dependencies. UniMath also has nested submodules; initialize those only when needed for its upstream build. A plain download of this repository's ZIP does not include the upstream source trees.

## Attribution and licenses

Thanks to **Jesse Vogel** for the Grothendieck-ring solver; **Daniel Sánchez Sánchez**, **David Alfaya Sánchez**, and **Jaime Pizarroso Gonzalo** for CIAMOD motives; **Dima Smirnov** for the scissors-congruence demonstration; and **Daniel R. Grayson** and the **UniMath Development Team** for the formalization and its supporting library. Upstream contributor lists, bibliographies, and notices remain with their respective projects.

- **CIAMOD motives:** the pinned [LICENSE](https://github.com/CIAMOD/motives/blob/6a4565a870618e677e90d66c1f10f4f67538ccad/LICENSE) contains GNU GPL version 3. The actual filename is `LICENSE`, despite the README's `LICENSE.md` link.
- **UniMath:** retain the pinned [LICENSE.md](https://github.com/UniMath/UniMath/blob/62837f6a3967df2568e2580ab8a6dbc5878d1011/LICENSE.md), including its UniMath Development Team copyright and notice-preservation condition.
- **Grothendieck-ring solver and scissors-congruence demo:** reuse permission was not established by the earlier survey. They are registered here as upstream references, not copied source. Review the upstream terms or obtain permission before incorporating their code into another implementation; bundled third-party libraries may have separate terms.

No upstream source was modified, installed, executed, or built as part of this registration. None of these references has been made a runtime or build dependency of the parent repository.
