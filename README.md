# Retained Update-Asymmetry and the Internal Arrow of Time

**Author:** Elad Genish
**Status:** v0.4 release candidate
**Project type:** short formal/philosophical paper with toy-system diagnostics

## Overview

This repository contains a short paper proposing a finite-formal-system account of temporal appearance as **retained update-asymmetry**.

The central idea is that an internal arrow-like direction becomes legible inside a formal system when retained structure from prior updates constrains admissible continuation, while exact reversal remains unavailable.

In simple terms:

> Time-like order appears when the past remains active as constraint, the future remains open as admissible continuation, and the system cannot simply reverse itself back into its prior state.

The paper does **not** claim to derive physical time, spacetime geometry, thermodynamic time, quantum measurement, or real cosmological time. Its claim is narrower: it proposes and tests a formal diagnostic regime for when past/present/future-like roles become internally legible inside finite toy systems.

## Core Claim

The paper argues that temporal appearance requires the conjunction of:

1. **Retention** — prior structure remains active inside the current system.
2. **Partial irreversibility** — the prior state cannot be exactly reconstructed or reversed.
3. **Admissible-future constraint** — retained structure filters what can happen next.
4. **Future openness** — more than one non-trivial continuation remains possible.
5. **Internal directional evidence** — retained traces make forward direction inferable above chance.

The central diagnostic is deliberately strict: a system does not count as temporally strong merely because it has order, memory, entropy-style spread, or succession. It scores positively only when the relevant components co-occur.

## Paper Contents

The paper includes:

* a definition of retained update-asymmetry;
* primitive terms such as configuration, update, retention, admissibility, and asymmetry;
* a worked toy example contrasting no memory, exact memory, and lossy retained constraint;
* failure controls for pure succession, perfect reversibility, unconstrained openness, over-constraint, external order, and entropy-style direction;
* a cross-system validation summary using cellular automata, event logs, HMM/filtering, compression chains, and causal DAG variants;
* an internal-arrow diagnostic separating retained update-asymmetry from external order and entropy-style spread.

## Main Result

The validation results support a narrow regime claim:

Retained/lossy systems score positively when lossy retention, nonzero irreversibility, admissible-future constraint, and remaining future openness co-occur.

The controls fail for distinct reasons:

* no-memory systems lack internally retained past structure;
* exact-memory systems suppress asymmetry through reverse recoverability;
* external-order systems may have observer-visible ordering without internal retention;
* entropy-style spread may appear without generating the retained-update arrow;
* over-constrained systems can collapse future openness.

The result is therefore not “memory creates time” or “entropy creates time.” The proposed result is more specific: **retained lossy constraint plus irreversibility plus admissible openness can generate an internal arrow-like diagnostic inside finite formal systems.**

## Repository Files

Suggested repository structure:

```text
/
├── README.md
├── paper/
│   ├── retained_update_asymmetry_internal_arrow_short_v04.pdf
│   ├── retained_update_asymmetry_internal_arrow_short_v04.docx
│   └── retained_update_asymmetry_internal_arrow_short_v04.md
└── supplement/
    └── future location for v0.7-v0.9 test history, tables, plots, code, and configuration files
```

## Scope and Limitations

This is a formal toy-system paper. It should be read as a diagnostic framework, not as a completed physical theory of time.

The paper does not claim that:

* physical time has been derived;
* thermodynamic entropy has been replaced;
* spacetime geometry has been generated;
* quantum measurement has been solved;
* an embedded conscious observer has been modelled.

Instead, the paper asks a narrower question:

> Under what formal conditions can a system internally distinguish past-like retained constraint, present-like active resolution, and future-like admissible openness?

## Citation

If citing this project informally, use:

```text
Genish, E. (2026). Retained Update-Asymmetry and the Internal Arrow of Time. v0.4 release candidate.
```

## Status

This version is treated as a release candidate. The main paper is frozen except for typos, formatting, missing citations, and clarity fixes. Larger extensions should be placed in a supplement or future paper rather than added to this version.
