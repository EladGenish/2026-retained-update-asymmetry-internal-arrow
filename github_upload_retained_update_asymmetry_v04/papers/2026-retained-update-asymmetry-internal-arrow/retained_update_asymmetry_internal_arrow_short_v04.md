# Retained Update-Asymmetry and the Internal Arrow of Time

**Author:** Zoe / Elad Genish  
**Status:** v0.4-release-candidate; frozen except for typos, formatting, missing citations, and clarity fixes  
**Associated supplement:** full v0.7-v0.9 test history, tables, plots, code, and configuration files  

---

## Abstract

This paper presents a finite-formal-system account of temporal appearance as **retained update-asymmetry**. The central claim is that, inside finite formal toy systems, an internal temporal direction becomes legible when retained structure from prior updates asymmetrically constrains admissible continuation while exact reversal remains unavailable. The account does not treat time as an external clock, primitive sequence, or independent container, and it does not derive physical time, the thermodynamic arrow, quantum measurement, or spacetime geometry. Its narrower claim is a regime diagnostic: past/present/future-like roles and an internal arrow-like direction can be generated inside formal systems when retention, partial irreversibility, admissible-future constraint, and remaining future openness co-occur. The v0.8b and v0.9 tests separate retained update-asymmetry from succession, exact memory, external order, and entropy-style spread. The nonzero internal-arrow cases are concentrated in retained/lossy regimes, while no-memory, exact-memory, external-order, and entropy-style controls fail for distinct reasons. The paper’s contribution is therefore not that records, irreversibility, or relational order matter in general, but that these ingredients can be separated and tested through a strict conjunction diagnostic.

---

## 1. Thesis and Motivation

The thesis of this paper is:

> **Time-like order can be generated inside a finite formal system when retained structure constrains admissible updates under partial irreversibility while leaving future continuation open.**

The core slogan is:

> **Time is what retained update-asymmetry looks like from inside a stable relational system.**

More precisely:

> **In finite formal systems, an internal temporal direction becomes legible when retained structure from prior updates asymmetrically constrains admissible future configurations while exact reversal remains unavailable.**

Many accounts of emergent time risk using temporal notions to explain time. If a model says that time emerges from updates, transitions, processes, or sequences, it may be accused of smuggling temporality into its base. This paper avoids that move by refusing to define time as mere succession.

Succession alone is not enough. A system can move from one state to another without internally possessing a past or future. Perfect memory is also not enough. A system can store its previous configurations, but if it can perfectly reverse or reconstruct the transition, the asymmetry between past and future is weakened or suppressed.

The proposed condition is stricter. Temporal appearance requires retained structure, constrained admissible continuation, loss of full reversibility, and remaining future openness. The past must remain active as constraint. The future must remain open as admissible continuation. The update relation must be asymmetric enough that the system cannot simply undo itself.

The target regime tested here is therefore:

1. **Retention:** prior structure remains active inside the current system.
2. **Partial irreversibility:** the system cannot exactly reconstruct or reverse the prior transition.
3. **Admissible-future constraint:** retained structure filters what can happen next.
4. **Future openness:** more than one non-trivial continuation remains possible.
5. **Internal directional evidence:** retained traces make forward direction inferable above chance.

The v0.9 arrow diagnostics sharpen the target. The question is not only whether a system receives a positive temporal-emergence score. The question is whether direction becomes inferable from inside the retained structure of the system. A directed acyclic order may be visible to an outside observer, and an entropy-style gradient may be measurable under coarse-graining, but neither is sufficient for internally generated temporal appearance unless the system itself retains traces that constrain admissible continuation.

---

## 2. Primitive Terms

The account uses five primitive or near-primitive terms.

**Configuration.** A configuration is a relational state of a system. It is not yet a moment. It becomes temporally meaningful only when it participates in update-asymmetry.

**Update.** An update is a transformation relation between configurations. The word should not be read as an event occurring in time. At the base level, an update is a relation of transformation or admissible succession between configurations.

**Retention.** Retention is the carrying-forward of structure from one configuration into another. Retention may be exact or lossy. Exact retention preserves recoverability. Lossy retention preserves constraint without preserving full reversibility.

**Admissibility.** Admissibility is the set of configurations compatible with current retained structure. A future is not simply whatever comes next. It is what remains admissible under the current retained constraints.

**Asymmetry.** Asymmetry occurs when one configuration constrains another without being equivalently constrained by it. In temporal terms, a retained past constrains the present and future, while the future is not yet retained in the same way.

These terms support the working definitions:

- **Past** = retained update-structure.
- **Present** = active update-resolution.
- **Future** = unresolved admissible continuation.
- **Temporal direction** = retained structure conditions later configurations without later configurations equivalently conditioning it.

---

## 3. The Retained-Asymmetry Relation

Let **C** be a set of configurations.

Define the retained-asymmetry relation **A ≺ B** (“A is retained-asymmetrically prior to B”) when:

1. **A** is retained as a constraint in **B**;
2. **B** is admissible partly because **A** has been incorporated, compressed, or preserved;
3. **B** is not equivalently retained as a constraint in **A**.

The relation **≺** should not initially be interpreted as ordinary chronological “earlier than.” It is more basic than temporal order. It is a relation of **retention-asymmetry**.

Temporal order appears when a stable system can internally distinguish:

- what has already been retained as constraint;
- what is being actively resolved;
- what remains admissible but unresolved.

Thus:

**Past** = retained update-structure.  
**Present** = active update-resolution.  
**Future** = unresolved admissible continuation.

---

## 4. Worked Example: Exact Memory Versus Lossy Retained Constraint

This section gives a small numerical example of the mechanism. It is not a new simulation result; it is only a transparent toy calculation showing why the diagnostic separates no memory, exact memory, and lossy retained constraint.

Let the configuration space be the four two-bit strings:

`00`, `01`, `10`, `11`

Suppose the current configuration is `10`. An outside observer may know that the system reached `10` after an update, but the question is what is internally retained by the system itself.

### 4.1 No memory

The no-memory system stores only `10`. If all four previous configurations remain compatible with the present state once memory is ignored, then retained structure has not reduced the past cone:

- raw past histories = 4;
- constrained past histories = 4;
- retention strength = 1 - log2(4) / log2(4) = 0.

If retained structure does not filter any possible next state, then:

- raw next configurations = 4;
- admissible next configurations = 4;
- constraint strength = 1 - 4/4 = 0.

Even if the update rule is irreversible from an external perspective, the temporal-emergence product is zero because there is no internally retained past and no retained constraint on the future.

### 4.2 Exact memory

The exact-memory system stores the full predecessor. Suppose it stores `01 -> 10`. Retention is maximal: the past is fully recoverable. But if exact memory also gives exact reversal, then reverse recoverability = 1 and irreversibility = 0.

The diagnostic therefore returns zero even though memory is present:

- retention strength = 1;
- reverse recoverability = 1;
- irreversibility = 1 - reverse recoverability = 0;
- temporal-emergence score = 0.

This is why the paper rejects the simple claim that “more memory means more time.” Exact memory can preserve a past while suppressing the asymmetry that makes an internal arrow legible.

### 4.3 Lossy retained constraint

The lossy-retained system stores a compressed trace rather than the full predecessor. Suppose the retained trace says only that the predecessor had odd parity. That trace is compatible with `01` and `10`, but not with `00` or `11`. It reduces possible pasts without uniquely reconstructing the exact past.

For illustration:

- raw past histories = 4;
- constrained past histories = 2;
- retention strength = 1 - log2(2) / log2(4) = 0.5.

Suppose the same retained trace filters the next configurations, leaving only two admissible continuations. Then:

- raw next configurations = 4;
- admissible next configurations = 2;
- constraint strength = 1 - 2/4 = 0.5.

Suppose exact reversal is unavailable, so reverse recoverability = 0.5 and irreversibility = 0.5. Suppose the bounded future cone remains non-trivial, giving future openness = 0.5. The product is then:

`0.5 x 0.5 x 0.5 x 0.5 = 0.0625`

The number is not important as a physical magnitude. What matters is the structural difference: the trace is retained enough to constrain histories and futures, but lossy enough not to restore exact reversibility. The past-like role is retained constraint, the present-like role is active update-resolution, and the future-like role is unresolved admissible continuation.

| Case | Retention | Irreversibility | Constraint | Future openness | Product | Failure / success reason |
|---|---:|---:|---:|---:|---:|---|
| No memory | 0.0 | nonzero possible | 0.0 | nonzero possible | 0.0000 | No internally retained past or future filtering |
| Exact memory | 1.0 | 0.0 | any | any | 0.0000 | Perfect reverse recoverability suppresses asymmetry |
| Lossy retained constraint | 0.5 | 0.5 | 0.5 | 0.5 | 0.0625 | Retains constraint without exact reversal |

The simulations test whether this schematic distinction survives across richer formal-system families and controls.

## 5. Failure Controls

The theory is defined negatively as well as positively. The controls separate temporal appearance from nearby but insufficient structures.

### 5.1 Pure succession is insufficient

A no-memory system may still undergo state changes. It may display succession from an external observer's point of view. But internally, it lacks retained structure by which previous configurations remain active as constraints.

**Proposition 1:** If retention = 0, temporal appearance = 0.

Succession without retention does not generate an internally legible past. It only generates observer-described ordering.

### 5.2 Perfect reversibility is insufficient

A full-retention system stores exact previous configurations. At first, this looks like stronger temporality. However, if retention is perfect and reversal is available, the distinction between past and future is weakened. The system can reconstruct or undo the update relation.

**Proposition 2:** If reverse recoverability = 1, temporal appearance = 0.

A perfect record does not generate the strongest temporal appearance. It can collapse the asymmetry that temporal appearance requires.

### 5.3 Unconstrained openness is insufficient

A system may have many possible next states. But if those possibilities are not constrained by retained structure, they do not form a structured future. They are merely undirected openness.

**Proposition 3:** If constraint = 0, temporal appearance = 0.

The future becomes temporally meaningful only when it is conditioned by retained structure.

### 5.4 Over-constraint is insufficient

If retained structure constrains too strongly, future openness collapses. The system becomes rigid rather than temporal. It no longer has unresolved admissible continuation; it has only forced continuation.

**Proposition 4:** If future openness = 0, temporal appearance = 0.

A fully closed future is not a future in the relevant sense. It is frozen continuation.

### 5.5 External order is insufficient

A system may be externally ordered without generating internal temporal appearance. In the causal-DAG baseline, external order can be perfect for the observer while internal retention remains absent. In that case, the system has order but not internally retained temporal structure.

The safe conclusion is not that DAG methods or causal-order approaches are wrong. The conclusion is narrower:

> **External order is not sufficient for internally generated temporal appearance.**

### 5.6 Entropy-style direction is insufficient

Entropy-style spread may accompany arrow-like behavior, but it is not equivalent to the retained-update arrow tested here. In v0.9, entropy-style scores appear in some no-memory and exact-memory controls that still have zero internal-arrow score. The entropy diagnostic used in this project is coarse-grained and formal, not thermodynamic entropy.

The safe conclusion is:

> **Entropy-like spread does not replace retained structure coupled to admissibility.**

Together, the controls sharpen the main claim. Succession alone, memory alone, constraint alone, openness alone, external order alone, and entropy-style direction alone are insufficient. The target condition is conjunctive.

---

## 6. Diagnostic Scores

The toy-model programme uses a deliberately strict multiplicative diagnostic:

`temporal_emergence_score = retention_strength × irreversibility × constraint_strength × future_open_norm`

This score is not proposed as a universal physical measure of time. It is a diagnostic conjunction test. A system does not score positively merely because it has one component in isolation. It scores only when all four components coexist.

| Component | Role in the diagnostic | Failure if absent |
|---|---|---|
| Retention strength | Measures how much prior structure remains active in the current system | Pure succession has no internally legible past |
| Irreversibility | Measures loss of exact reverse recoverability | Perfect recoverability suppresses asymmetry |
| Constraint strength | Measures how strongly retained structure filters admissible next configurations | Openness becomes undirected |
| Future openness | Measures whether non-trivial continuation remains admissible | Over-constraint becomes frozen continuation |

The multiplication encodes the theory's central claim:

> Temporal appearance is strongest where retained structure partially preserves the past, constrains admissible continuation, prevents full reversal, and leaves future continuation open.

The v0.9 suite adds a harsher internal-arrow diagnostic:

`internal_arrow_score = temporal_emergence_score × arrow_accuracy_above_chance × (1 - exact_reverse_success) × record_constraint_correlation`

This score is also a conjunction diagnostic, not a physical magnitude. It is expected to be small because it multiplies several demanding conditions: temporal emergence, above-chance direction evidence, reversal resistance, and record/admissibility coupling.

### Why the scores are small

The absolute product scores are small by design. The diagnostic multiplies normalized components rather than adding them. A system with several moderate-to-high components can therefore produce a small final score. This is not a claim that the temporal effect is physically tiny, and it is not a probability that the system “has time.” It is a strict conjunction test.

For that reason, the important evidence is comparative and decomposed: which systems score zero, which systems score nonzero, and which component causes each failure. A no-memory system fails through retention and record coupling. An exact-memory system fails through reversibility. An external-DAG system can have perfect observer-visible order while failing through internal retention. Entropy-style scores can be nonzero while internal arrow remains zero. The decomposition is therefore part of the result, not a secondary detail.

The purpose of the diagnostic is not to measure time itself. It is to test whether the internal-arrow condition survives controls that separate succession, memory, external order, entropy-style direction, and retained update-asymmetry.

---

## 7. Systems and Validation Setup

The completed validation suite moves beyond the original bitstring toy model. It keeps the same primitives: configuration, update, retention, admissibility, asymmetry, past as retained structure, present as active update-resolution, and future as unresolved admissible continuation.

The v0.8b and v0.9 suites use five formal-system families:

1. **Cellular automata** — reversible exact, irreversible no-memory, and coarse-retained variants.
2. **Event logs** — no log, exact log, partial compressed log, and corrupted log variants.
3. **Hidden Markov filtering** — no-memory, perfect-state, and partial-filter variants.
4. **Compression chains** — no-memory, exact memory, lossy invariant, and over-compressed variants.
5. **Causal DAGs** — external-order and internal-trace variants.

The validation configuration is:

- 30 deterministic seeds per system cell;
- memory depths `[1, 2, 3, 5]`;
- strictnesses `[1, 2, 3]`;
- 600 bootstrap rounds;
- deterministic configuration files saved for the v0.8b and v0.9 runs.

Finite steps, cut points, graph depths, and bootstrap counts remain observer-side diagnostics. They are not added to the internal model state. The internal model state remains configuration plus retained structure.

### 7.1 Operational mapping across system families

Because the validation suite uses heterogeneous finite systems, the same abstract term is implemented differently in each family. The table below states the intended mapping. Full implementation details belong in the supplement and code, but the public paper needs enough mapping to show that the same construct is being tracked rather than a different idea in each family.

| Family | Retention means | Admissibility / constraint means | Irreversibility means | Future openness means | Main caution |
|---|---|---|---|---|---|
| Cellular automata | Coarse retained features of previous local/global configurations | Candidate future states filtered by retained coarse features | Failure to reconstruct the exact predecessor from the retained state | Size/diversity of the bounded future cone after filtering | Coarse retention must not be confused with an external time index |
| Event logs | No log, exact log, partial compressed log, or corrupted log | Future transitions compatible with the retained log features | Exact logs allow reversal; partial/corrupted logs resist exact reconstruction | Remaining compatible continuations after log-based filtering | Exact records can erase the target asymmetry |
| HMM/filtering | A partial belief/filter state rather than no memory or perfect hidden-state access | Continuations compatible with the current filter state | Loss of full hidden-state recoverability | Future cone available under the partial filter | Strict filters can close future openness |
| Compression chains | Exact memory, lossy invariant, or over-compressed code | Continuations compatible with the compressed retained code | Compression prevents exact predecessor recovery | Non-trivial continuations that remain code-compatible | Over-compression fails only if openness collapses |
| Causal DAGs | Either no internal trace, or a retained internal trace added to external order | Continuation constrained by internal trace, not by observer-visible DAG order alone | Exact reverse reconstruction remains unavailable only when trace is lossy | Available continuations under trace-constrained DAG dynamics | External DAG order is observer-visible order, not internal retention |

A schematic diagnostic loop is:

```text
for each generated trajectory:
    expose only configuration + retained structure as the internal state
    estimate retained past constraint from the current retained structure
    estimate admissible future constraint from continuations compatible with that retained structure
    estimate reverse recoverability from whether the predecessor can be exactly reconstructed
    estimate future openness from the non-triviality of remaining admissible continuations
    compute the conjunction score and the internal-arrow diagnostics
```

The update rule and finite horizon are used by the experimenter to run and evaluate the system. They are not added as clock-time or step-index variables inside the system state. This is why the current claim is a formal diagnostic over internal retained structure, not a literal embedded observer model.

---

## 8. v0.8b Cross-System Regime Result

v0.8b is the cross-system validation pass. It asks whether retained update-asymmetry survives beyond the original bitstring toy model as a regime claim.

The result is mixed but positive. Retained/lossy candidates score positively across several families when lossy retention, nonzero irreversibility, admissible-future constraint, and remaining future openness co-occur. The mechanism fails when memory is absent, retention is exact/reversible, order is externally imposed without internal retention, retained traces are disconnected from admissibility, or retained traces close future openness.

A compact summary of the central v0.8b comparisons is:

| Family | Positive retained/lossy case | Product mean | 95% CI | Key control result | Interpretation |
|---|---|---:|---:|---|---|
| cellular automata | CA_CoarseRetained | 0.0395 | [0.0362, 0.0427] | ReversibleExact and IrreversibleNoMemory score 0.0000 | Coarse retained memory plus irreversible updating separates from both controls. |
| event log | Event_CorruptedLog / Event_PartialCompressedLog | 0.0530 / 0.0507 | [0.0485, 0.0576] / [0.0460, 0.0547] | NoLog and ExactLog score 0.0000 | Partial/corrupted records outperform absent and exact records. |
| HMM/filtering | HMM_PartialFilter | 0.0179 | [0.0162, 0.0196] | NoMemory and PerfectState score 0.0000 | Partial filtering works, but fails when strictness closes future openness. |
| compression chain | Compression_OverCompressed / Compression_LossyInvariant | 0.0618 / 0.0311 | [0.0542, 0.0685] / [0.0278, 0.0344] | NoMemory and ExactMemory score 0.0000 | Compression supports the theory only when lossy, irreversible, constraining, and still open. |
| causal DAG | CausalDAG_InternalTrace | 0.0048 | [0.0032, 0.0065] | ExternalOrder has DAG-rate 1.0000 but product score 0.0000 | External order alone is insufficient; internal retention makes only a weak positive case. |

Several qualifications matter.

First, event logs support the regime interpretation strongly. NoLog scores zero because retained structure is absent. ExactLog scores zero because exact reversible retention removes irreversibility and admissible-future filtering. PartialCompressedLog and CorruptedLog score positively because they preserve recoverable past structure imperfectly, constrain admissible continuation, and leave the future open.

Second, HMM/filtering is weaker and more conditional. HMM_PartialFilter is positive, while NoMemory and PerfectState score zero. But HMM_PartialFilter fails in strictness-3 regimes when future openness goes to zero. This is a useful failure mode, not a defect. The conjunction claim predicts that over-constraint should suppress temporal appearance.

Third, the compression-chain result forces caution. Compression_OverCompressed beats Compression_LossyInvariant in v0.8b. This should not be hidden. It means the intermediate-constraint claim must be stated carefully: over-constraint fails only when it collapses future openness. Compression can still score if it remains lossy, irreversible, constraining, and open.

Fourth, the causal-DAG result is the weakest positive family. CausalDAG_ExternalOrder has perfect DAG structure but zero product and geometric score because retention is zero. CausalDAG_InternalTrace becomes weakly positive by adding internal retention, but remains weak because future openness is low. This supports the distinction between externally imposed order and internally retained temporal appearance, while leaving the current DAG implementation suggestive rather than decisive.

The failure table records 126 weak or zero-score cells. The main failure modes are absent memory, exact/reversible memory, external order without internal retention, retained traces disconnected from admissibility, retained traces that close future openness, and strictness too high in some HMM/filtering regimes. The failure table is part of the discipline of the model: a system does not count as temporally strong merely because it has order, memory, constraint, or openness in isolation.

The v0.8b verdict is therefore:

> Retained update-asymmetry survives beyond the original bitstring toy model as a formal regime claim. It appears when lossy retention, nonzero irreversibility, admissible-future constraint, and remaining future openness co-occur. It does not win automatically.


---

## 9. v0.9 Internal-Arrow Result

v0.9 extends the v0.8b cross-system validation by asking a sharper question: can retained update-asymmetry generate an **internal arrow of time**, not merely a positive temporal-emergence score?

The arrow is defined as the direction inferable from retained update-asymmetry inside the system. Simulation step indices, finite horizons, and trajectory order remain observer-side diagnostics only; they are not added to the internal model state.

The v0.9 suite adds five observer-side tests over trajectories generated by the same internal systems:

1. **Direction classification:** distinguish forward from reversed local transitions using configuration, retained memory, admissibility, past ambiguity, and future-cone properties, but not the raw simulation step index.
2. **Retrodiction/prediction asymmetry:** compare recoverable or ambiguous past structure against admissible future openness.
3. **Reversal resistance:** test whether the final state can reconstruct its predecessor exactly or only partially from internal retained structure.
4. **Record gradient:** measure whether retained traces remain useful for constraining futures, not merely whether records accumulate numerically.
5. **Entropy/coarse-graining comparison:** compare a coarse entropy-style arrow with the retained-update arrow without treating entropy as the theory's primitive.

The central v0.9 result is:

> The nonzero internal-arrow cases are concentrated in retained/lossy regimes, while no-memory, exact-memory, external-order, and entropy-style controls fail for distinct reasons.

The system-level arrow statistics are:

| Family | System | Internal arrow | Direction accuracy | Exact reverse | Record coupling | Entropy arrow | Temporal score | Retention | DAG-rate |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| event_log | Event_CorruptedLog | 0.039777 | 0.967 | 0.152 | 0.906 | 0.060 | 0.0523 | 0.360 | 0.883 |
| event_log | Event_PartialCompressedLog | 0.038498 | 0.952 | 0.064 | 0.924 | 0.098 | 0.0471 | 0.314 | 0.756 |
| cellular_automata | CA_CoarseRetained | 0.028518 | 0.990 | 0.031 | 0.854 | 0.065 | 0.0338 | 0.202 | 0.956 |
| compression_chain | Compression_LossyInvariant | 0.019628 | 0.786 | 0.276 | 0.974 | 0.050 | 0.0308 | 0.514 | 0.394 |
| HMM/filtering | HMM_PartialFilter | 0.018154 | 0.860 | 0.000 | 0.971 | 0.145 | 0.0200 | 0.262 | 0.347 |
| compression_chain | Compression_OverCompressed | 0.010834 | 0.616 | 0.114 | 0.932 | 0.035 | 0.0584 | 0.525 | 0.622 |
| causal_dag | CausalDAG_InternalTrace | 0.003918 | 1.000 | 0.202 | 0.919 | 0.119 | 0.0047 | 0.425 | 1.000 |
| causal_dag | CausalDAG_ExternalOrder | 0.000000 | 0.500 | 0.000 | 0.000 | 0.109 | 0.0000 | 0.000 | 1.000 |
| cellular_automata | CA_IrreversibleNoMemory | 0.000000 | 0.500 | 0.380 | 0.000 | 0.027 | 0.0000 | 0.000 | 0.633 |
| cellular_automata | CA_ReversibleExact | 0.000000 | 0.952 | 1.000 | 0.000 | 0.085 | 0.0000 | 0.000 | 0.867 |
| compression_chain | Compression_ExactMemory | 0.000000 | 0.989 | 1.000 | 0.000 | 0.100 | 0.0000 | 1.000 | 0.725 |
| compression_chain | Compression_NoMemory | 0.000000 | 0.500 | 0.000 | 0.000 | 0.118 | 0.0000 | 0.000 | 0.000 |
| event_log | Event_ExactLog | 0.000000 | 0.993 | 1.000 | 0.000 | 0.072 | 0.0000 | 1.000 | 0.842 |
| event_log | Event_NoLog | 0.000000 | 0.500 | 0.000 | 0.000 | 0.098 | 0.0000 | 0.000 | 0.000 |
| HMM/filtering | HMM_NoMemory | 0.000000 | 0.500 | 0.000 | 0.000 | 0.091 | 0.0000 | 0.000 | 0.000 |
| HMM/filtering | HMM_PerfectState | 0.000000 | 0.986 | 1.000 | 0.000 | 0.075 | 0.0000 | 1.000 | 0.692 |

A component-wise reading is essential because the strict product score is small by design. The following compact diagnostic table shows the main success and failure patterns.

| Case | Temporal score | Direction evidence | Reversal resistance | Record coupling | Internal arrow result | Interpretation |
|---|---:|---:|---:|---:|---:|---|
| Event_CorruptedLog | 0.0523 | high | high | high | 0.039777 | Strongest retained/lossy internal-arrow case |
| Event_PartialCompressedLog | 0.0471 | high | very high | high | 0.038498 | Partial record beats exact record because it constrains without exact reversal |
| CA_CoarseRetained | 0.0338 | very high | very high | high | 0.028518 | Coarse retained trace supports direction while preserving openness |
| Compression_OverCompressed | 0.0584 | weak/moderate | high | high | 0.010834 | High temporal score but weak direction evidence reduces arrow score |
| CausalDAG_ExternalOrder | 0.0000 | chance | not relevant | zero | 0.000000 | Perfect external order without internal retention fails |
| Event_ExactLog | 0.0000 | high | zero | zero | 0.000000 | Exact memory classifies direction but reverses too well |
| Event_NoLog | 0.0000 | chance | not relevant | zero | 0.000000 | Succession without retention fails |

The interpretation is mixed but positive.

The strongest retained/lossy case is Event_CorruptedLog, with mean internal_arrow_score = 0.039777. The score is small because it multiplies temporal emergence, above-chance direction evidence, reversal resistance, and record/admissibility coupling.

Exact-memory controls can classify direction well, but they reverse too well. Event_ExactLog, Compression_ExactMemory, and HMM_PerfectState have exact reverse success near 1.000, which collapses the internal-arrow composite. This supports the claim that exact memory is not the same thing as an internal arrow.

No-memory controls sit at chance-level direction classification and have zero record/admissibility coupling, even where they have admissible continuations or entropy-like spread. This supports the claim that succession or openness alone is insufficient.

CausalDAG_ExternalOrder has DAG-rate = 1.000 and entropy_arrow_score = 0.109, but retention, direction-above-chance, record coupling, temporal emergence, and internal arrow all remain zero. CausalDAG_InternalTrace improves to internal_arrow_score = 0.003918 by adding internal trace, but remains weak because future openness is low. This supports the distinction between external order and internal temporal appearance.

Entropy-style scores appear in no-memory and exact-memory controls that still have zero internal-arrow score. The highest entropy-arrow system is HMM_PartialFilter, but the strongest internal-arrow systems are event-log variants. Entropy may correlate with some arrows, but it does not replace retained structure coupled to admissibility.

The v0.9 failure table records 112 weak or zero-arrow cells. Main failures are absent memory, exact/reversible memory, external order without internal retention, weak above-chance direction evidence, weak record/admissibility coupling, and retained traces that close future openness.

The v0.9 verdict is:

> The v0.9 arrow suite gives formal evidence that retained update-asymmetry can induce an internal arrow in finite systems when lossy retention, nonzero irreversibility, admissible-future constraint, and future openness co-occur. The arrow is not equivalent to external order, exact memory, or entropy-gradient alone. The result remains a regime claim, not a physical derivation of the thermodynamic arrow.


---

## 10. Relation to Nearby Work and Non-Claims

This account sits near several existing approaches, but it should not be collapsed into them. The aim is not to replace those approaches. The aim is to isolate one formal condition under which temporal roles become internally legible in finite update systems.

### 10.1 Computational mechanics

The closest formal cousin is computational mechanics. In that literature, causal states and epsilon-machines provide minimal predictive representations of a stochastic process: histories are grouped according to the futures they make predictable. This is strongly adjacent to the present paper because both projects treat retained structure as future-relevant information rather than as a mere archive.

The connection becomes even closer in work on prediction, retrodiction, crypticity, and causal irreversibility. That literature explicitly compares forward-time and reverse-time representations and asks how much information is stored in the present. This overlaps with the present paper's concern with lossy retention, exact reversal, record usefulness, and direction inference.

The difference is the target. Computational mechanics primarily develops optimal predictive and retrodictive structure for stochastic processes. The present paper asks a narrower temporal-appearance question: under what finite-system conditions do past/present/future-like roles and an internal arrow-like direction become legible? Its contribution is the explicit conjunction diagnostic across heterogeneous formal systems: retention, partial irreversibility, admissible-future constraint, and remaining future openness, followed by an internal-arrow diagnostic that separates exact memory, no memory, external order, entropy-style spread, and retained/lossy traces.

So computational mechanics should be treated as a major neighbor, not as a rival to be dismissed. It gives the paper a clearer nearby formal literature. The novelty claim is not “causal states did not exist”; it is that retained update-asymmetry is isolated here as a formal regime condition for internal temporal appearance and tested against controls designed to separate temporal appearance from succession, memory volume, external order, and entropy-style direction.

### 10.2 Records, the Past Hypothesis, and thermodynamic arrows

The paper also sits near philosophical work on records, the epistemic arrow, and the Past Hypothesis. In that tradition, one major question is why present records appear to be records of the past rather than the future, and whether this asymmetry depends on a low-entropy boundary condition.

The present paper does not derive the physical record asymmetry and does not replace Past-Hypothesis or thermodynamic accounts. Its claim is local and formal: in finite systems, retained traces can make one update direction internally legible when they constrain admissible continuation without enabling exact reversal. This can be read as a non-thermodynamic formal analogue of record asymmetry, but not as a physical explanation of why our universe has records of the past.

The distinction is important. Thermodynamic-record accounts normally ask how physical records arise in a universe with time-symmetric micro-laws and special boundary conditions. This paper instead asks how a finite formal system can internally separate retained structure, active update-resolution, and admissible continuation. The entropy-style diagnostic is included only as a comparison/control. Entropy-like spread can be nonzero while the retained internal-arrow score remains zero.

### 10.3 Causal order and causal-set approaches

Causal-order approaches, including causal-set programmes, use directed order as a fundamental or proto-spatiotemporal structure. The present account also uses directed order, but it does not attempt to recover spacetime geometry or function as a quantum-gravity theory. Its contribution is narrower: it distinguishes external order from internally retained temporal appearance.

The causal-DAG control is important for exactly this reason. It shows that a structure can be perfectly ordered for the observer while failing the internal-retention diagnostic. The safe claim is not that causal-set or DAG methods are wrong. It is only that external order is not sufficient for the specific internal-arrow diagnostic tested here.

### 10.4 Constructor-theoretic approaches

Constructor-theoretic approaches formulate physical theories in terms of possible and impossible transformations. The present account shares an interest in admissible transformations, but its focus is different: how retained structure internally generates the distinction between past, present, future, and internal direction.

### 10.5 Non-claims

The novelty claim is narrow:

> **This model isolates retained update-asymmetry as a candidate formal regime condition for temporal appearance and tests it against no-memory, reversible-memory, exact-memory, lossy-retention, external-order, and entropy-style controls.**

This paper does **not** claim:

1. to solve physical time;
2. to derive general relativity;
3. to derive entropy or the thermodynamic arrow;
4. to derive quantum measurement;
5. to derive cosmological boundary conditions;
6. that the toy score is a physical quantity;
7. that all arrows of time reduce to retained update-asymmetry;
8. that retained update-asymmetry wins generally or automatically across all systems.

It supports only a formal regime claim: a particular temporal architecture can be generated inside toy-model and finite formal systems without treating clock-time as primitive in the state description.

---

## 11. Conclusion

This paper has argued that temporal appearance can be treated as a retained-update relation rather than as primitive succession. The core structure is:

> retained structure → active update-resolution → unresolved admissible continuation

In this structure, the past is retained update-structure, the present is active update-resolution, and the future is unresolved admissible continuation. Temporal direction appears when retained structure conditions later configurations without later configurations equivalently conditioning it.

The main contribution is not the claim that time is relational, that records matter, or that irreversibility matters. Those themes already exist in nearby literatures. The contribution is the formal separation of several conditions that are often run together: succession, memory, external order, entropy-style direction, and internally retained temporal appearance.

The simulations support this separation. No-memory systems can have succession but lack retained past structure. Exact-memory systems can preserve the past but suppress asymmetry by enabling reversal. External-order systems can possess a perfect directed order for the observer while generating no internal arrow when retention is absent. Entropy-style spread can appear without internal temporal appearance. Retained/lossy systems produce the nonzero internal-arrow cases when retention, partial irreversibility, admissible-future constraint, and future openness co-occur.

The final current claim is therefore conditional and formal:

> **Internal temporal direction appears when retained/lossy structure makes forward direction inferable from internal traces while exact reversal remains unavailable.**

This is not a derivation of physical time. It is a finite-formal-system account of one regime in which past/present/future-like roles and an internal arrow-like direction can be generated without placing clock-time inside the state description.

---

## References and Nearby Literature

- Albert, David Z. *Time and Chance*. Cambridge, MA: Harvard University Press, 2000.
- Baron, Simon. “Causal theories of spacetime.” *Noûs*, 2024.
- Callender, Craig. “Thermodynamic Asymmetry in Time.” *Stanford Encyclopedia of Philosophy*. First published 2001; substantive revisions ongoing.
- Deutsch, David. “Constructor Theory.” arXiv:1210.7439.
- Ellison, Christopher J., John R. Mahoney, and James P. Crutchfield. “Prediction, Retrodiction, and the Amount of Information Stored in the Present.” *Journal of Statistical Physics* 136 (2009): 1005-1034.
- Price, Huw. *Time's Arrow and Archimedes' Point*. Oxford: Oxford University Press, 1996.
- Rovelli, Carlo. “Relational Quantum Mechanics.” arXiv:quant-ph/9609002.
- Shalizi, Cosma R., and James P. Crutchfield. “Computational Mechanics: Pattern and Prediction, Structure and Simplicity.” *Journal of Statistical Physics* 104 (2001): 817-879. arXiv:cond-mat/9907176.
- Sorkin, Rafael. “Geometry from order: causal sets.” Einstein Online.
- Stradis, Andreas. “Present Records of the Past Hypothesis.” *Synthese* (2024).
- Surya, Sumati. “The causal set approach to quantum gravity.” *Living Reviews in Relativity* / arXiv:1903.11544.

These are positioning references, not claims of direct derivation. The present model is a formal account of retained update-asymmetry, not a replacement for computational mechanics, causal-order programmes, or thermodynamic-arrow accounts.
