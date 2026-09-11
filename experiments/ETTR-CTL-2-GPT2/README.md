# ETTR-CTL-2 — GPT-2 Small

## Experiment

**Experiment ID:** ETTR-CTL-2

**Title:** A Two-Model Empirical Reconstruction of Contextual Transport

ETTR-CTL-2 is the GPT-2 Small component of the empirical ETTR/Contextual Transport Logic research program.

The experiment investigated whether selected transport structures inspired by Contextual Calculus and Contextual Transport Logic could be operationalized and empirically evaluated on Transformer representations.

---

## Model

- Model: `openai-community/gpt2`
- Architecture: GPT-2 Small
- Layers: 12
- Hidden dimension: 768
- Attention heads: 12
- Vocabulary size: 50257
- Maximum position embeddings: 1024
- Activation: `gelu_new`
- Selected layer: 10

---

## Computational environment

The primary implementation used the Hugging Face native GPT-2 implementation.

- Transformers: 5.16.1
- Hardware: NVIDIA Tesla T4
- Representation precision: FP16

A TransformerLens implementation was also audited for equivalence. The audit identified a numerical/backend parameterization mismatch. The Hugging Face native implementation was therefore retained as the authoritative numerical backend.

---

## Dataset

Dataset version: **v1.1**

The final dataset contained:

- 192 records;
- 12 templates;
- 16 ordered pairs per template;
- 32 single-token GPT-2 target names;
- an exact crossed clean/corrupt design.

Dataset v1.0 was rejected because of target-token asymmetry.

The v1.1 dataset was accepted as the operative experimental dataset.

---

## Operational sectors

Three measurable Transformer pathways were used:

### S1 — contextual interaction

Attention output.

### S2 — state propagation

Residual/state propagation entering the selected Transformer block.

### S3 — feature transformation

MLP output.

These are **operational sectors**, not a claim that the Transformer has exactly three ontologically fundamental computational components.

---

## Main findings

The behavioral baseline supported held-out contextual separation, although substantial template/pair heterogeneity was present.

Controlled sector intervention instrumentation passed.

Finite sector transport was operationalized, but the results were heterogeneous.

A contextual carrier based on the layer-10 Transformer block output was identified and evaluated.

The frozen contextual realization did **not** generalize successfully to held-out data.

The robust negative result remained present across primary summary statistics and grouped bootstrap analyses.

---

## Contextual realization

The selected contextual realization candidate was:

`dK4_pc10_pd10_tkfull_linear_ta1000.0`

Calibration normalized coherence defect:

`0.8573122753`

Held-out test mean normalized coherence defect:

`1.0653109898`

Held-out test median:

`1.0132859945`

The held-out result was classified as:

`FROZEN_CONTEXTUAL_REALIZATION_GENERALIZATION_NOT_SUPPORTED`

---

## Triadic analysis

An exploratory full-factorial analysis produced a nonzero three-way contrast.

However, the result was not treated as proof of triadic irreducibility.

The analysis exhibited suspicious repeated-template behavior and only a very small incremental predictive contribution.

Therefore:

**Triadic irreducibility was NOT established.**

The subsequent contextual realization analysis also did not establish a robust triadic computational advantage.

---

## Scientific conclusion

The experiment supports the operationalization of selected ETTR/CTL structures on GPT-2 Small, but does not establish that GPT-2 empirically realizes the complete mathematical CTL framework.

In particular:

- CTL kernel: supported;
- behavioral contextual separation: supported with heterogeneity;
- operational sectors: supported as measurable sectors;
- controlled intervention instrumentation: supported;
- sector transport: supported with heterogeneity;
- contextual carrier: supported;
- frozen contextual realization generalization: not supported;
- `Phi_C` reconstruction: not supported;
- triadic irreducibility: not established;
- geometric realization: not tested.

The overall experiment was classified as:

`NEGATIVE_RESULT_ROBUST_ACROSS_PRIMARY_SUMMARIES`

Negative and unresolved findings are retained as part of the scientific record.

---

## Reproducibility

This directory contains the human-readable and machine-readable record of the experiment.

Files:

- `README.md` — experiment overview
- `scientific_record.md` — detailed scientific history
- `experiment_config.json` — experimental configuration
- `results_summary.json` — machine-readable results
- `dataset_manifest.json` — dataset identity and design
- `hashes.txt` — SHA-256 integrity record

Large numerical artifacts are intended to be archived separately where appropriate.

---

## Scientific caution

This experiment should not be interpreted as evidence that:

> "GPT-2 implements Contextual Transport Logic."

The scientifically justified conclusion is narrower: selected formal structures and finite transport procedures were operationalized and tested on GPT-2 Small, with mixed and ultimately negative held-out results for the stronger contextual realization claim.

