# Optimal Quantum Johnson Block Designs: Orbit Decomposition, Steiner Supports, and Stability

JIANG ZHICHENG — ORCID: [0009-0001-4772-4490](https://orcid.org/0009-0001-4772-4490)

This repository contains the paper and the complete verification code for
minimum effective size in the quantum Johnson block-design framework of
Misawa (*Quantizing Delsarte Theory*, arXiv:2610.09900v1).

> Cite as: JIANG ZHICHENG, *Optimal Quantum Johnson Block Designs: Orbit
> Decomposition, Steiner Supports, and Stability*, 2026.
> DOI: [10.5281/zenodo.24442937](https://doi.org/10.5281/zenodo.24442937).
> arXiv: forthcoming.

## Results

- **Trace bound and Steiner equality (Theorem 3).** For strength $t$, every
  design has effective size at least $d\binom{v}{t}/\binom{k}{t}$; equality
  requires rank-one blocks supported on a Steiner $t$-$(v,k,1)$ system.
- **Multi-orbit formula (Theorem 4).** For a point-$t$-transitive group, the
  invariant minimum is $d$ times the smallest orbit-size-times-irreducible-
  dimension product over block orbits; minimizers are disjoint unions of
  projective spaces. No transitivity on $k$-element blocks is assumed.
- **Projective three-point classification (Theorem 6).** The
  $\operatorname{PGL}_2$ strength-three minimum is
  $\binom{q+1}{3}(q-3)$ for every prime power $q \geq 7$; values 224, 420,
  720, 1760, 3640, 8840 at $q = 7, 8, 9, 11, 13, 16$.
- **Cyclic partitions (Theorem 7).** At strength one, partitions attain the
  trace bound whenever $k$ divides $v$.
- **Finite-subfield lines (Theorem 9).** For $q = r^e$, $e \geq 2$, affine
  lines over the subfield $\mathbb{F}_r$ form a Steiner $2$-$(q,r,1)$
  system and attain the strength-two minimum
  $(q-r-1)q(q-1)/[r(r-1)]$; e.g. 60 at $q=9$, 220 at $q=16$.
- **Purity stability (Theorem 11).** Near-optimal block-transitive designs
  are quantitatively close in Hilbert–Schmidt distance to a true minimizer.

Scope, stated in the paper: the minima 15 / 60 / 420 at $v=9$, $k=3$ are
minima at strengths 1 / 2 / 3 — different constrained problems, not
improvements of one another. The strength-three minimum 420 is already
attained and cannot be lowered. The $q=5$ strength-three optimum is
unresolved (bracket 40–80). No quantum coding advantage is claimed.

## Files

- `Quantum_Johnson_Orbit_Steiner_Stability_EN_20261122_2018.pdf`
  — research manuscript, 11 pages (English).
- `Quantum_Johnson_Full_Paper_Code_and_Contribution_Review_20261122_2235.zip`
  — supplementary package: verification code, audit trail, literature
  summaries, legacy material, SHA-256 manifest. It does not contain the
  manuscript folder; the paper is the PDF above.

## Reproduce

Python 3.12, in a clean directory, never with `python -O`:

```bash
# Three exact suites (needs numpy and sympy)
python -m pip install -r requirements.txt
python verify_all.py
```

Reference outputs from the reviewed run are in the package
(`code/*_results.json`). Finite exact regression confirms the implemented
instances and arithmetic; it does not replace the all-parameter proofs.

No Lean or other formal proof checker was used. No independent peer review
has been completed yet.

## License

Paper: CC BY 4.0. Code: MIT.
