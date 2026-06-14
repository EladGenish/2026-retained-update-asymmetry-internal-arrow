\documentclass[11pt]{article}
\usepackage[a4paper,margin=1in]{geometry}
\usepackage{amsmath,amssymb}
\usepackage{booktabs,longtable,array}
\usepackage{hyperref}
\usepackage{enumitem}
\usepackage{microtype}
\usepackage{caption}
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage{lmodern}
\setlist{nosep}
\hypersetup{colorlinks=true,linkcolor=black,citecolor=black,urlcolor=blue}
\newcommand{\scoreT}{\mathrm{TES}}
\newcommand{\scoreA}{\mathrm{IAS}}
\newcommand{\Config}{\mathcal{C}}
\newcommand{\Hist}{\mathcal{H}}
\newcommand{\Adm}{\mathcal{A}}
\newcommand{\Trace}{\mathcal{Z}}
\newcommand{\Update}{\mathcal{U}}
\title{Retained Update-Asymmetry as a Formal Condition for Internal Temporal Directedness:\\Adversarial Diagnostics Across Finite Update Systems}
\author{Elad Genish}
\date{2026}
\begin{document}
\maketitle
\begin{abstract}
This paper proposes retained update-asymmetry as a formal condition under which temporal directedness becomes internally legible in finite update systems. The claim is not that physical time, thermodynamic irreversibility, quantum measurement, or spacetime geometry has been derived. The narrower claim is diagnostic: when retained structure constrains admissible continuation, exact reversal is unavailable, and future continuation remains non-trivially open, a system can support internally directed past-like, present-like, and future-like roles. The paper defines finite systems as tuples $S=(\Config,\Update,\Hist,R,K)$, protects the internal state $I_t=(C_t,Z_t)$ from observer-side leakage, and evaluates a strict conjunction diagnostic across adversarial controls. In the v1 finite-grid benchmark, the target retained/lossy regime produces 1024 positive cells out of 3125, while no-retention, exact-memory, external-clock, shuffled-trace, entropy-only, random-trace, future-closed, trace-decoupled, observer-order-only, and perfect-reverse controls produce zero internal-arrow positives. The result supports retained update-asymmetry as a regime condition for internal temporal directedness in finite formal systems, while leaving physical and computational-mechanics extensions as future work.
\end{abstract}

\section{Introduction}
Many accounts of emergent time risk explaining time by quietly relying on temporal notions: update, transition, process, sequence, or before-and-after. This paper avoids that route by treating temporal directedness not as primitive succession, but as a relation between retained structure, admissible continuation, irreversibility, and openness inside a finite formal system.

The guiding question is simple: what must be present inside a system for a direction to become legible from the system's own retained structure, rather than from an observer's clock, a hidden trajectory index, or an externally imposed order? The proposed answer is \emph{retained update-asymmetry}. Prior structure must remain active as a constraint; it must constrain admissible continuation; it must not allow exact reversal; and it must leave more than one non-trivial continuation open.

This gives a strict diagnostic rather than a universal measure of time. A system does not count as temporally directed merely because it changes. It also does not count merely because it has memory, entropy-style spread, or an externally visible order. The target condition is conjunctive: retained structure, partial irreversibility, admissible-future constraint, future openness, and internal directional evidence must co-occur.

The contribution is therefore methodological and formal. The paper turns the retained-asymmetry thesis into explicit objects, metrics, controls, and a reproducible validation package. The v1 benchmark is designed to make the theory harder to fake: controls are allowed to contain tempting direction signals, but they do not count unless the signal is internally retained, irreversibly asymmetric, and coupled to admissible continuation.

\section{Relation to Existing Machinery}
The closest established neighbor is computational mechanics. In computational mechanics, causal states group histories by their predictive equivalence over futures, and $\epsilon$-machines provide minimal predictive models of stochastic processes. Shalizi and Crutchfield describe causal-state representations as minimal and unique representations consistent with accurate prediction, while Crutchfield, Ellison, and Mahoney connect prediction, retrodiction, crypticity, stored information, and causal irreversibility in ``Time's Barbed Arrow'' \cite{shalizi_crutchfield_2001,crutchfield_ellison_mahoney_2009}.

This paper does not claim to replace that machinery. Instead, it isolates a narrower diagnostic problem. Computational mechanics asks, among other things, what structure is required for optimal prediction and retrodiction of stochastic processes. Retained update-asymmetry asks when an internally available retained trace makes a temporal direction legible while exact reversal remains unavailable and future continuation remains open.

The distinction matters. A process can have predictive structure without satisfying the strict internal-arrow conjunction used here. Conversely, a retained trace can carry past information without constraining admissible futures. The present diagnostic therefore treats prediction alone, memory alone, observer-visible order alone, and entropy-style spread alone as insufficient. The v1 computational-mechanics comparison is only a proxy comparison; it does not reconstruct causal states or infer full $\epsilon$-machines. A proper causal-state benchmark is reserved for future work.

The paper is also adjacent to work on reversibility and information loss. Landauer's principle links logical irreversibility and heat generation in computation, and Bennett's reversible computation work shows how computation can be organized to preserve reversibility by retaining sufficient history \cite{landauer_1961,bennett_1973}. The present framework uses a formal analogue of this contrast: exact recoverability suppresses the target asymmetry, while lossy retained constraint can preserve enough past structure to constrain futures without restoring full reversibility.

\section{Formal Framework}
Let a finite update system be a tuple
\begin{equation}
S=(\Config,\Update,\Hist,R,K),
\end{equation}
where $\Config$ is a finite configuration space, $\Update$ is an update relation or kernel over configurations, $\Hist_t$ is the experimenter-side history available for evaluation, $R$ is a retention operator, and $K$ is a consistency relation used to determine admissible continuations.

At each internal point, the protected internal state is
\begin{equation}
I_t=(C_t,Z_t),
\end{equation}
where $C_t\in\Config$ is the current configuration and
\begin{equation}
Z_t = R(\Hist_t,C_t)
\end{equation}
is the retained trace. The trace may be empty, exact, lossy, corrupted, shuffled, overcompressed, or decoupled from future admissibility depending on the system family or control.

The admissible future set determined by the protected internal state is
\begin{equation}
\Adm(I_t)=\{c'\in\Config:K(I_t,c')=1\}.
\end{equation}
This is the set of continuations compatible with the current configuration and retained trace. Crucially, observer-side step indices, file order, seed IDs, raw hidden histories, and external topological ranks are forbidden inputs unless they are actually retained inside $Z_t$.

The retained-asymmetry relation can now be stated as follows. A configuration $A$ is retained-asymmetrically prior to $B$ when: (i) structure from $A$ is retained as a constraint in the internal state associated with $B$; (ii) admissible continuation from $B$ is partly filtered by that retained structure; and (iii) $B$ is not equivalently retained as a constraint in $A$. This relation is not ordinary chronological earlier-than. It is a relation of retained constraint asymmetry from which temporal roles may become legible.

\section{Diagnostic Components}
The diagnostic is deliberately strict and multiplicative. It is not a universal measure of time; it is a conjunction test. The four primary components are retention strength, irreversibility, constraint strength, and future openness.

Retention strength measures how much retained structure reduces uncertainty about predecessor information relative to the current configuration alone. A convenient normalized form is
\begin{equation}
\rho_t = 1 - \frac{H(P_t\mid C_t,Z_t)}{H(P_t\mid C_t)},
\end{equation}
where $P_t$ denotes the relevant predecessor variable or predecessor set. If $Z_t$ gives no reduction in predecessor ambiguity, then $\rho_t=0$.

Irreversibility measures failure of exact reconstruction from the protected internal state:
\begin{equation}
\iota_t = 1-P(\widehat{P_t}=P_t\mid C_t,Z_t).
\end{equation}
Exact memory can preserve the past while making exact reversal available. In this diagnostic, that suppresses the arrow condition because the target is retained asymmetry, not maximal recoverable memory.

Constraint strength measures whether retained structure constrains future admissibility:
\begin{equation}
\kappa_t = 1-\frac{H(C_{t+1}\mid C_t,Z_t)}{H(C_{t+1}\mid C_t)}.
\end{equation}
A retained trace that does not alter admissible futures is a record, but not a future-structuring record under this theory.

Future openness measures whether non-trivial continuation remains. One normalized entropy form is
\begin{equation}
\omega_t = \frac{H(C_{t+1}\mid C_t,Z_t)}{\log |\Adm_{\max}|},
\end{equation}
with the additional guardrail that forced continuation counts as a collapse of future openness for the target temporal role.

The temporal-emergence score is
\begin{equation}
\scoreT_t=\rho_t\iota_t\kappa_t\omega_t.
\end{equation}
The stricter internal-arrow score is
\begin{equation}
\scoreA_t = \scoreT_t\,\alpha_t\,\beta_t\,\gamma_t,
\end{equation}
where $\alpha_t$ is direction accuracy above chance, $\beta_t$ is reversal resistance, and $\gamma_t$ is record/admissibility coupling. A system can therefore show a direction signal and still fail the internal-arrow diagnostic if the signal comes from exact memory, observer order, clock leakage, or uncoupled records.

\section{Worked Micro-Example}
The micro-example compares three systems: NoMemory, ExactMemory, and LossyRetainedConstraint. Its purpose is not to prove the general claim, but to show the mechanism transparently.

In NoMemory, the internal state stores only the current configuration. It does not retain enough predecessor structure to reduce past ambiguity, and it does not use retained structure to filter future admissibility. Retention and constraint therefore collapse, and the product score is zero.

In ExactMemory, the internal state stores the full predecessor. This produces maximal recoverable past information, but it also permits exact reverse reconstruction. Since irreversibility is defined as one minus exact reverse success, the irreversibility component collapses. The system has memory but lacks the retained asymmetry targeted by the diagnostic.

In LossyRetainedConstraint, the internal state stores a compressed trace. The trace reduces past ambiguity without uniquely reconstructing the predecessor, and it filters admissible futures while leaving multiple continuations open. This gives nonzero retention, irreversibility, constraint, and future openness.

\begin{table}[h]
\centering
\small
\caption{Micro-example component structure.}
\begin{tabular}{p{0.23\textwidth}ccccp{0.28\textwidth}}
\toprule
Case & Retention & Irreversibility & Constraint & Openness & Result \\
\midrule
NoMemory & 0 & possible & 0 & possible & Zero: no internally retained past or future filtering. \\
ExactMemory & high & 0 & possible & possible & Zero: exact reverse recoverability suppresses asymmetry. \\
LossyRetainedConstraint & nonzero & nonzero & nonzero & nonzero & Positive: retained constraint without exact reversal. \\
\bottomrule
\end{tabular}
\end{table}

\section{Adversarial Validation Design}
The v1 benchmark is designed around a firewall. A classifier or diagnostic may only use protected internal-state features derived from $I_t=(C_t,Z_t)$ and admissible continuation computed from that state. It may not use time index, file order, seed identity, raw history, external DAG rank, or labels unless those are explicitly present in $Z_t$.

The finite-grid benchmark sweeps five parameter values, $\{0,0.25,0.5,0.75,1\}$, over the relevant components. Eleven controls are matched against the target retained/lossy condition: NoRetention, ExactMemory, ExternalClockLeak, ShuffledTrace, EntropyOnly, RandomTrace, FutureClosed, TraceDecoupled, ObserverOrderOnly, and PerfectReverse. The goal is not merely to find positive cases. The goal is to show that tempting non-target direction signals fail for the right reason.

\section{Results}
\subsection{Finite-Grid Control Summary}
In the v1 finite-grid benchmark, TargetLossy produces 1024 positive cells out of 3125, or 32.768 percent. Every adversarial control produces zero positive cells under the strict internal-arrow diagnostic.

\begin{longtable}{p{0.24\textwidth}rrrp{0.34\textwidth}}
\caption{Adversarial finite-grid control summary.}\\
\toprule
Control & Positive cells & Mean internal & Max internal & Failure mode \\
\midrule
\endfirsthead
\toprule
Control & Positive cells & Mean internal & Max internal & Failure mode \\
\midrule
\endhead
TargetLossy & 1024 & 0.010828 & 1 & Target retained/lossy regime. \\
NoRetention & 0 & 0 & 0 & Absent retention and absent record/admissibility coupling. \\
ExactMemory & 0 & 0 & 0 & Exact reverse recoverability suppresses asymmetry. \\
ExternalClockLeak & 0 & 0 & 0 & Rejected by classifier-input firewall. \\
ShuffledTrace & 0 & 0 & 0 & Trace shuffled away from admissible futures. \\
EntropyOnly & 0 & 0 & 0 & Entropy-style spread without retained admissibility. \\
RandomTrace & 0 & 0 & 0 & Random trace not coupled to past/future structure. \\
FutureClosed & 0 & 0 & 0 & Admissible future collapsed to forced continuation. \\
TraceDecoupled & 0 & 0 & 0 & Retained trace does not constrain admissible futures. \\
ObserverOrderOnly & 0 & 0 & 0 & Order visible to observer but not internally retained. \\
PerfectReverse & 0 & 0 & 0 & Perfect reverse reconstruction. \\
\bottomrule
\end{longtable}

\subsection{Direction Evidence Audit}
The direction audit separates direction evidence from internal-arrow validity. ExactMemory, PerfectReverse, ObserverOrderOnly, and ExternalClockLeak can show high direction evidence, but none count as internal-arrow positives. This is central: the diagnostic is not merely rewarding any signal that indicates a direction.

\begin{longtable}{p{0.20\textwidth}cccc}
\caption{Direction evidence audit.}\\
\toprule
Control & Allowed & Max above chance & High-dir./zero-int. & Rejected \\
\midrule
\endfirsthead
\toprule
Control & Allowed & Max above chance & High-dir./zero-int. & Rejected \\
\midrule
\endhead
TargetLossy & True & 1 & 0 & 0 \\
NoRetention & True & 0 & 0 & 0 \\
ExactMemory & True & 0.900 & 3125 & 0 \\
ExternalClockLeak & False & 1 & 3125 & 3125 \\
ShuffledTrace & True & 0 & 0 & 0 \\
EntropyOnly & True & 0 & 0 & 0 \\
RandomTrace & True & 0 & 0 & 0 \\
FutureClosed & True & 0 & 0 & 0 \\
TraceDecoupled & True & 0 & 0 & 0 \\
ObserverOrderOnly & True & 1 & 3125 & 0 \\
PerfectReverse & True & 0.900 & 3125 & 0 \\
\bottomrule
\end{longtable}

\subsection{Classifier Firewall}
The classifier firewall tests whether different feature regimes are too permissive. The strict allowed conjunction identifies the target positive finite-grid regime. Additive components and retention-only modes achieve high apparent performance but produce false positives. Forbidden external order performs at chance, while the label oracle is perfect but explicitly invalid.

\begin{table}[h]
\centering
\small
\caption{Classifier firewall summary.}
\begin{tabular}{p{0.29\textwidth}cccp{0.27\textwidth}}
\toprule
Mode & Allowed & Balanced accuracy & AUC & Reading \\
\midrule
internal\_conjunction & True & 1.000 & 1.000 & Strict target identification. \\
additive\_components & True & 0.878 & 0.949 & Too permissive; several false positives. \\
retention\_only & True & 0.783 & 0.748 & Too permissive; memory alone is insufficient. \\
external\_order & False & 0.500 & 0.453 & Chance-level under firewall. \\
label\_oracle & False & 1.000 & 1.000 & Perfect but invalid. \\
\bottomrule
\end{tabular}
\end{table}

\subsection{Family Validation Derived from v0.9}
The family validation table is derived from existing v0.9 aggregate outputs rather than a fresh v1 family sweep. It should therefore be read as continuity evidence, not as a new v1 rerun. Across five families, the best retained/lossy candidate separates from a matched control with zero internal-arrow score.

\begin{table}[h]
\centering
\small
\caption{Family validation from v0.9 aggregate output.}
\begin{tabular}{p{0.20\textwidth}p{0.25\textwidth}rp{0.22\textwidth}r}
\toprule
Family & Best retained/lossy candidate & Candidate score & Best control & Control score \\
\midrule
causal\_dag & DAG\_InternalTrace & 0.003918 & DAG\_ExternalOrder & 0 \\
cellular\_automata & CA\_CoarseRetained & 0.028518 & CA\_NoMemory & 0 \\
compression\_chain & Comp\_LossyInvariant & 0.019628 & Comp\_ExactMemory & 0 \\
event\_log & Event\_CorruptedLog & 0.039777 & Event\_ExactLog & 0 \\
hmm\_filtering & HMM\_PartialFilter & 0.018154 & HMM\_NoMemory & 0 \\
\bottomrule
\end{tabular}
\end{table}

The causal-DAG distinction is especially important. DAG\_ExternalOrder has a DAG-rate of 1 but retention 0 and internal-arrow score 0. DAG\_InternalTrace has a DAG-rate of 1, retention 0.425, and internal-arrow score 0.003918. External order can be perfect for an observer while failing to generate internal temporal directedness.

\subsection{Computational-Mechanics Proxy}
The v1 package includes a preliminary neighbor comparison. It does not infer causal states or reconstruct $\epsilon$-machines. It only compares retained-arrow-style proxies, entropy-arrow proxies, and several related quantities against the internal-arrow score. Retained-arrow proxies align strongly with the internal score because they share diagnostic ingredients; entropy-arrow proxy values are not sufficient by themselves.

\begin{table}[h]
\centering
\small
\caption{Selected computational-mechanics proxy comparison.}
\begin{tabular}{p{0.34\textwidth}rrrr}
\toprule
Proxy metric & Pearson & Spearman & Mean & Max \\
\midrule
retained\_arrow\_score & 0.999 & 1.000 & 0.011 & 0.046 \\
entropy\_arrow\_score & -0.134 & -0.207 & 0.084 & 0.145 \\
constraint\_strength & 0.618 & 0.703 & 0.364 & 0.902 \\
forward\_record\_usefulness & 0.692 & 0.857 & 0.200 & 0.627 \\
record\_constraint\_correlation & 0.795 & 0.864 & 0.405 & 0.974 \\
exact\_reverse\_success & -0.389 & -0.152 & 0.326 & 1.000 \\
\bottomrule
\end{tabular}
\end{table}

\section{Interpretation}
The finite-grid result supports a regime claim: retained update-asymmetry appears when retained/lossy traces constrain admissible futures, exact reversal is unavailable, and future openness remains nonzero. The important evidence is not only that TargetLossy scores positively. It is that matched controls fail for distinct reasons.

NoRetention fails because there is no internally retained past or future filtering. ExactMemory fails because full recoverability suppresses asymmetry. ExternalClockLeak is rejected because it uses forbidden observer-side information. ShuffledTrace and TraceDecoupled fail because retained traces do not constrain futures. EntropyOnly fails because entropy-style spread is not enough. FutureClosed fails because admissible continuation collapses. ObserverOrderOnly fails because order is visible to the observer but not retained internally. PerfectReverse fails because exact reconstruction remains available.

This is the central separation: external order is not internal temporal directedness. A directed graph, a clock, an ordered file, or a perfect trajectory label can make direction obvious to an observer. The question here is whether direction is inferable from retained structure inside the system under the target constraints.

\section{Scope and Limitations}
The claim remains deliberately narrow. This paper does not derive physical time, replace the thermodynamic arrow, solve the Past Hypothesis, replace causal-set approaches, or model an embedded conscious observer. It also does not reconstruct $\epsilon$-machines or claim to reproduce computational mechanics.

The family validation is derived from v0.9 aggregate output, not rerun as a new v1 family sweep. The classifier artifact is a firewall diagnostic over the finite grid, not yet a full transition-level forward/reverse classifier with out-of-distribution generalization. The computational-mechanics section is preliminary and should be replaced by actual causal-state or $\epsilon$-machine reconstruction where feasible.

These limitations are not defects in the release. They define the boundary between the present paper and future work. The present result is a formal diagnostic regime claim over finite update systems.

\section{Reproducibility}
The validation package is designed for open reproduction. The repository includes or is intended to include the simulation specification, benchmark implementation, experiment scripts, compiled validation report, and one-command reproduction scripts. The key commands are:
\begin{verbatim}
python -m pytest tests -q
python experiments/run_v1_micro_example.py
python experiments/run_v1_finite_benchmark.py
python experiments/run_v1_classifier_firewall.py
python experiments/run_v1_family_validation_from_v09.py
python experiments/run_v1_comp_mech_proxy_from_v09.py
python tools/build_v1_compiled_report.py
\end{verbatim}
One-command scripts are also supplied:
\begin{verbatim}
pwsh ./reproduce_v1.ps1
bash ./reproduce_v1.sh
\end{verbatim}

\section{Next Work}
The next technical step is a true transition-level forward/reverse classifier using only protected internal-state features. The second step is out-of-distribution testing across seeds and families. The third step is a genuine computational-mechanics benchmark: infer causal states or reconstruct approximate $\epsilon$-machines where feasible, then compare statistical complexity, excess entropy, crypticity, causal irreversibility, and the retained-update diagnostic.

Only one applied-adjacent probe should be added at first, and only if it tests the existing primitives without adding new theory. The strongest candidate is an event-log, hash-chain, or versioned-record process, because it naturally separates exact logs, partial records, corruption, reconstruction, and admissible continuation.

\section{Conclusion}
Retained update-asymmetry is supported as a formal regime condition for internally generated temporal directedness in finite update systems. The strongest current evidence is adversarial rather than merely positive: the retained/lossy target regime scores positively, while controls for no retention, exact memory, entropy-style spread, external order, clock leakage, shuffled traces, decoupled traces, closed futures, and perfect reversal fail. The result does not prove that physical time is emergent. It does show that internal temporal directedness can be isolated as a strict formal diagnostic over retained structure, irreversibility, admissible continuation, and future openness.

\begin{thebibliography}{9}
\bibitem{landauer_1961}
Landauer, R. (1961). Irreversibility and heat generation in the computing process. \emph{IBM Journal of Research and Development}, 5(3), 183--191.

\bibitem{bennett_1973}
Bennett, C. H. (1973). Logical reversibility of computation. \emph{IBM Journal of Research and Development}, 17(6), 525--532.

\bibitem{crutchfield_young_1989}
Crutchfield, J. P., and Young, K. (1989). Inferring statistical complexity. \emph{Physical Review Letters}, 63(2), 105--108.

\bibitem{shalizi_crutchfield_2001}
Shalizi, C. R., and Crutchfield, J. P. (2001). Computational mechanics: Pattern and prediction, structure and simplicity. \emph{Journal of Statistical Physics}, 104, 817--879.

\bibitem{crutchfield_ellison_mahoney_2009}
Crutchfield, J. P., Ellison, C. J., and Mahoney, J. R. (2009). Time's barbed arrow: Irreversibility, crypticity, and stored information. \emph{Physical Review Letters}, 103, 094101.

\bibitem{feng_crooks_2008}
Feng, E. H., and Crooks, G. E. (2008). The length of time's arrow. \emph{Physical Review Letters}, 101, 090602.
\end{thebibliography}
\end{document}