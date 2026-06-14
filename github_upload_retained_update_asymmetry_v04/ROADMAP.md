# Reproducibility Notes

The v1 validation package is designed around open reproduction. From the repository root, the intended commands are:

```bash
python -m pytest tests -q
python experiments/run_v1_micro_example.py
python experiments/run_v1_finite_benchmark.py
python experiments/run_v1_classifier_firewall.py
python experiments/run_v1_family_validation_from_v09.py
python experiments/run_v1_comp_mech_proxy_from_v09.py
python tools/build_v1_compiled_report.py
```

One-command wrappers:

```bash
pwsh ./reproduce_v1.ps1
bash ./reproduce_v1.sh
```

## Firewall rule

Classifier or diagnostic inputs may use only protected internal-state features derived from:

```text
I_t = (C_t, Z_t)
```

Forbidden inputs include observer-side step index, file order, seed ID, raw hidden history, external DAG rank, and label-oracle information unless such information is actually retained inside `Z_t`.

## Current status

The compiled report documents completed finite-grid adversarial validation and a classifier firewall diagnostic. It does not yet claim full transition-level forward/reverse classifier results or true epsilon-machine reconstruction.