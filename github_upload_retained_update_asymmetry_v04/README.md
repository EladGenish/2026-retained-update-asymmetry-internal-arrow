# Retained Update-Asymmetry and the Internal Arrow of Time

**Author:** Elad Genish  
**Current status:** v1 formal paper draft + adversarial validation package  
**Repository:** `2026-retained-update-asymmetry-internal-arrow`

## Overview

This repository contains a formal paper and validation package for **retained update-asymmetry**: a proposed diagnostic condition for when temporal directedness becomes internally legible in finite update systems.

The core claim is deliberately narrow:

> Internal temporal directedness becomes legible when retained structure constrains admissible continuation, exact reversal remains unavailable, and future continuation remains non-trivially open.

The project does **not** claim to derive physical time, replace thermodynamics, solve quantum measurement, or generate spacetime geometry. It studies finite formal update systems and asks when past-like retained constraint, present-like active resolution, and future-like admissible openness can be separated from mere succession, exact memory, observer-visible order, entropy-style spread, and forbidden clock leakage.

## Main files

```text
paper/
  retained_update_asymmetry_internal_arrow_v1.tex   LaTeX source for the v1 paper
  retained_update_asymmetry_internal_arrow_v1.md    readable Markdown companion
  references.bib                                    bibliography file

validation/
  v1_adversarial_validation_report.md               compiled v1 validation report
  README.md                                         validation-package guide

docs/
  REPRODUCIBILITY.md                                reproduction commands and audit trail
  ROADMAP.md                                        next technical steps

CITATION.cff                                        citation metadata
```

## Main result

The v1 adversarial finite-grid benchmark reports:

- `TargetLossy`: **1024 / 3125 positive cells**.
- Matched controls: **0 positive cells** for NoRetention, ExactMemory, ExternalClockLeak, ShuffledTrace, EntropyOnly, RandomTrace, FutureClosed, TraceDecoupledFromAdmissibility, ObserverOrderOnly, and PerfectReverse.

The direction-evidence audit also shows that ExactMemory, PerfectReverse, ObserverOrderOnly, and ExternalClockLeak can show high direction evidence while still failing the internal-arrow diagnostic. This is the central separation: the diagnostic is not merely rewarding any direction signal.

## Reproducibility

The validation report lists the intended one-command reproduction scripts:

```bash
pwsh ./reproduce_v1.ps1
bash ./reproduce_v1.sh
```

and the underlying experiment commands:

```bash
python -m pytest tests -q
python experiments/run_v1_micro_example.py
python experiments/run_v1_finite_benchmark.py
python experiments/run_v1_classifier_firewall.py
python experiments/run_v1_family_validation_from_v09.py
python experiments/run_v1_comp_mech_proxy_from_v09.py
python tools/build_v1_compiled_report.py
```

## Scope

This is a formal diagnostic framework, not a completed physical theory of time. The strongest present claim is:

> Retained update-asymmetry is supported as a formal regime condition for internally generated temporal directedness in finite formal systems.

## Citation

```text
Genish, E. (2026). Retained Update-Asymmetry as a Formal Condition for Internal Temporal Directedness: Adversarial Diagnostics Across Finite Update Systems. v1 draft.
```