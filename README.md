# Lorentz Transformations from Projective Temporal Ordering (LC-O1)

This repository contains the source of the paper
*Lorentz Transformations from Projective Temporal Ordering
(LC-O1 of the Lorentz-Capacity Sub-Programme)*
(`Beau2026lco1`).

## Overview

The Lorentz-capacity programme derives relativistic kinematics from the bounded
Born-Infeld capacity budget of admissible projection on
$\mathrm{Heis}_3(\mathbb{Z}/q\mathbb{Z})$. The technical note
`Beau2026n` and the temporal residual paper `Beau2026tp` established that the
projective temporal capacity satisfies

$$F^\tau = \sqrt{1-\beta^2} = \frac{1}{\gamma},$$

closing time dilation ($d\tau/dn = 1/\gamma$) and the light cone
($\beta = 1 \Rightarrow F^\tau = 0$). The remaining open problem, stated in
Section 7.2 of `Beau2026tp`, is the reconstruction of the full effective
observer transformation between inertial observers, including length
contraction. The present paper closes this open problem (LC-O1).

## Main Result

Given two inertial observers with relative normalised capacity load $\beta$,
the unique proper orthochronous isometry of the reconstructed flat effective
interval mapping one temporal axis to the other is the standard Lorentz boost

$$\tau' = \gamma(\tau - \beta x),\qquad
  x' = \gamma(x - \beta\tau),\qquad
  y' = y,\qquad z' = z,$$

with $\gamma = (1-\beta^2)^{-1/2}$, and length contraction follows as the
reciprocal spatial projection onto the simultaneity hyperplane of the moving
splitting:

$$\ell = \frac{\ell_0}{\gamma}.$$

The argument rests on a strict separation of three structural layers, each
imported from a previously closed result:

1. **Born-Infeld capacity sphere** (`Beau2026c`, `Beau2026m`): the Euclidean
   capacity constraint $(F^\tau)^2 + \beta^2 = 1$ supplies $\beta$ and
   $1/\gamma$ from projective data. It is *not* the Minkowski interval.
2. **Effective Lorentzian co-metric** (`Beau2026q5b`, `Beau2026q11`): the
   homogeneous Q5b/Q11 closure gives the completed effective co-metric
   $g^{\mu\nu} = 2\,\eta^{\mu\nu}$, whose isometry group is $\mathrm{SO}(3,1)$.
3. **Inertial observer and boost**: an inertial observer is identified with a
   future-directed unit timelike splitting $u$ of $\eta$. The rapidity is
   fixed by the capacity load via $\xi = \mathrm{arctanh}\,\beta$, and the
   Lorentz boost is the unique proper orthochronous isometry of $\eta$ mapping
   one admissible splitting to another at that load.

Length contraction is then a direct corollary of the boost: the difference in
simultaneity hyperplanes between two inertial splittings, given the interval
structure of Layer 2, produces the standard $\ell = \ell_0/\gamma$ relation.

## Key features

- **No new spectral or projective hypothesis.** All inputs are previously
  closed; LC-O1 only identifies inertial observers with unit timelike
  splittings and applies the standard uniqueness of isometries of $\eta$ in
  each rapidity class.
- **Strict layer separation.** The Born-Infeld capacity sphere is not a
  Lorentzian structure; the Lorentz group acts as the isometry group of
  $\eta$, not of the BI sphere. The BI sphere determines which splittings are
  admissible; the Lorentz group determines how to pass between them.
- **Length contraction as derived corollary.** It is a consequence of the
  boost and the simultaneity hyperplane geometry, not an independent capacity
  law.
- **Closure of LC-O1.** The full effective observer transformation, including
  length contraction, is reconstructed from projective temporal ordering data
  and the effective metric normalisation.

## Status

- Inertial splitting and rapidity identification: **proved**
- Uniqueness of the inertial boost (Lemma): **proved**
- Lorentz transformations from projective temporal ordering (Theorem):
  **proved**
- Length contraction (Corollary): **proved**
- Closure of LC-O1: **proved**

## Position in the sub-programme

```
LorCap -> TempProj -> LC-O2 -> LC-O2-O1
                            \-> LC-O1
```

## Dependencies

| Paper | Role |
|-------|------|
| N (`Beau2026n`) | Lorentz factor from projective capacity saturation |
| TempProj (`Beau2026tp`) | Temporal residual map; statement of LC-O1 (Section 7.2) |
| PTO (`Beau2026pto`) | Projective temporal ordering observable; scalar clock factor $d\tau/dn$ |
| Q5b (`Beau2026q5b`) | BFS shell stratification; emergence of the effective Lorentzian metric |
| Q11 (`Beau2026q11`) | Closure of the effective co-metric $g^{\mu\nu} = 2\,\eta^{\mu\nu}$ |
| C (`Beau2026c`) | Born-Infeld admissibility budget (Layer 1) |
| M (`Beau2026m`) | Admissible non-injective transitions as the primitive of physical description |

## Repository Contents

```
lc-o1/
|-- out/              # Compiled PDF
|-- tex/
|   |-- lc-o1.tex
|   |-- cosmochrony-bibliography.bib
|-- compile.sh
|-- zenodo.json
|-- README.md
```

## Compilation

```bash
bash compile.sh
```

## Citation

> J. Beau, *Lorentz Transformations from Projective Temporal Ordering*,
> Preprint, 2026.

## Acknowledgements

Portions of the editorial refinement benefited from iterative interactions with
large language models used as analytical assistants.
All claims, interpretations, and final formulations remain the sole
responsibility of the author.
