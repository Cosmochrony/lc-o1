# Lorentz Transformations from Projective Temporal Ordering (LC-O1)

This repository contains the source of the paper
*Lorentz Transformations from Projective Temporal Ordering
(LC-O1 of the Lorentz-Capacity Sub-Programme)*
(`Beau2026lco1`).

## Overview

The Lorentz-capacity programme studies relativistic kinematics from the bounded
Born-Infeld capacity budget of admissible projection on
$\mathrm{Heis}_3(\mathbb{Z}/q\mathbb{Z})$. The technical note
`Beau2026n` and the temporal residual paper `Beau2026tp` give, under a quadratic budget hypothesis and the
identifications stated there, the projective temporal capacity

$$F^\tau = \sqrt{1-\beta^2} = \frac{1}{\gamma}.$$

The problem LC-O1, stated in Section 7.2 of `Beau2026tp`, is the reconstruction of the full effective
observer transformation between inertial observers, including length contraction. The present paper
closes it conditionally on a supplied co-metric and on the hypothesis [H-cone].

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

The argument rests on a strict separation of three structural layers, each with a stated status:

1. **Born-Infeld capacity sphere** (`Beau2026n`, expressing the bound [A-cap] of `Beau2026c`): the Euclidean
   capacity constraint $(F^\tau)^2 + \beta^2 = 1$ supplies $\beta$ and
   $1/\gamma$ from projective data. It is *not* the Minkowski interval.
2. **Effective Lorentzian co-metric** (supplied, of the form of `Beau2026q11` Corollary 6.1):
   $g^{\mu\nu} = \mathrm{diag}(-A_\tau, 2\lambda, 2\lambda, 2\lambda)$ with $A_\tau$ and $\lambda$
   independent and fixed by no source. After a rescaling of $\tau$ it is proportional to $\eta$, whose
   isometry group is $\mathrm{SO}(3,1)$; the normalisation $g^{\mu\nu} = 2\,\eta^{\mu\nu}$ is a choice of units.
3. **Inertial observer and boost**: an inertial observer is identified with a
   future-directed unit timelike splitting $u$ of $\eta$. Under **[H-cone]** (the light-cone speed of the
   co-metric equals the Born-Infeld bound per ordering step; the coupling datum that Q11 leaves open), the
   rapidity is fixed by the capacity load via $\xi = \mathrm{arctanh}\,\beta$, and the
   Lorentz boost is the unique proper orthochronous isometry of $\eta$ mapping
   one admissible splitting to another at that load.

Length contraction is then a direct corollary of the boost: the difference in
simultaneity hyperplanes between two inertial splittings, given the interval
structure of Layer 2, produces the standard $\ell = \ell_0/\gamma$ relation.

## Key features

- **One named kinematic hypothesis.** The inputs are conditional (supplied co-metric, quadratic budget,
  identifications of `Beau2026tp`); LC-O1 identifies inertial observers with unit timelike splittings, names
  [H-cone], and applies the standard uniqueness of isometries of $\eta$ in each rapidity class.
- **Strict layer separation.** The Born-Infeld capacity sphere is not a
  Lorentzian structure; the Lorentz group acts as the isometry group of
  $\eta$, not of the BI sphere. The BI sphere determines which splittings are
  admissible; the Lorentz group determines how to pass between them.
- **Length contraction as derived corollary.** It is a consequence of the
  boost and the simultaneity hyperplane geometry, not an independent capacity
  law.
- **Conditional closure of LC-O1.** The full effective observer transformation, including
  length contraction, is reconstructed from projective temporal ordering data, a supplied co-metric and
  [H-cone].

## Status

- Uniqueness of the inertial boost (Lemma): **proved** for $\eta$
- Lorentz transformations from projective temporal ordering (Theorem): **proved** under a supplied co-metric
  of the form of Q11 Corollary 6.1 and [H-cone]
- Length contraction (Corollary): **proved** under the same hypotheses
- [H-cone]: **hypothesis**, not derived (Q11-O1)

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
| Q5b (`Beau2026q5b`) | Rank-three co-metric under [H-L] and [H-lift]; rank-four extension open |
| Q8 (`BeauQ8`) | $A_H = A_Z = 2\lambda$ with $\lambda$ free, for a supplied invariant form |
| Q10 (`Beau2026q10`) | No coefficient value derived |
| Q11 (`Beau2026q11`) | Conditional form $\mathrm{diag}(-A_\tau, 2\lambda, 2\lambda, 2\lambda)$; coupling datum open |
| C (`Beau2026c`) | Capacity bound [A-cap] (Layer 1) |
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
