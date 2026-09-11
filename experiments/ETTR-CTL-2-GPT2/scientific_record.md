# ETTR-CTL-2 — GPT-2 Small
# Detailed Scientific Record

**Experiment ID:** ETTR-CTL-2

**Title:** A Two-Model Empirical Reconstruction of Contextual Transport

**Model:** GPT-2 Small (`openai-community/gpt2`)

**Selected layer:** 10

**Experimental status:** CLOSED

**Overall classification:** `NEGATIVE_RESULT_ROBUST_ACROSS_PRIMARY_SUMMARIES`

---

# 1. Experimental purpose

ETTR-CTL-2 was designed to investigate whether selected structures associated with Empirical Triadic Transport Reconstruction (ETTR) and Contextual Transport Logic (CTL) could be operationalized and empirically examined on a Transformer language model.

The experiment did not attempt to demonstrate that GPT-2 literally instantiates the complete mathematical structures of Contextual Calculus.

Instead, the experiment separated:

1. the mathematical framework;
2. its finite operationalization on Transformer representations; and
3. numerical execution on GPU hardware.

The mathematical definitions were not modified in response to implementation constraints.

---

# 2. Experimental design

The experiment used:

- GPT-2 Small;
- 192 contextual records;
- clean and corrupted conditions;
- 12 prompt templates;
- 16 ordered pairs per template;
- 32 target names;
- a fixed selected layer;
- three operational sectors;
- controlled sector interventions;
- finite transport-map estimation;
- contextual realization;
- exploratory triadic analysis;
- held-out evaluation.

The three operational sectors were:

- S1: contextual interaction / attention output;
- S2: state propagation across depth / residual state entering the block;
- S3: feature transformation / MLP output.

The sectors were operational measurement pathways rather than ontological claims about Transformer structure.

---

# 3. Phase 0A — CTL logical kernel

The formal CTL logical kernel was tested before the main empirical experiment.

All eight logical-kernel tests passed.

**Status: PASS**

Artifact:

`/content/ettr_ctl2/results/ctl_kernel_contract.json`

The logical kernel audit established the computational contract of the formal logic.

It did not establish empirical CTL realization inside GPT-2.

---

# 4. Phase 0B — Architecture and intervention audit

The GPT-2 architecture was audited.

The audit established:

- Transformers version: 5.16.1;
- model: `openai-community/gpt2`;
- layers: 12;
- hidden dimension: 768;
- attention heads: 12;
- vocabulary size: 50257;
- maximum positional embeddings: 1024;
- activation: `gelu_new`.

Layer 10 was selected.

The Hugging Face native implementation was used for the authoritative experiment.

The relevant sector hooks were:

- S1: `transformer.h.10.attn`;
- S2: block input;
- S3: `transformer.h.10.mlp`.

**Status: PASS**

---

# 5. Dataset development

The first dataset version was rejected.

The reason was target-token asymmetry.

A corrected dataset version, v1.1, was constructed with:

- exactly 192 records;
- 12 templates;
- 16 ordered pairs per template;
- 32 single-token GPT-2 names;
- exact crossed clean/corrupt design.

The final v1.1 dataset was accepted as the operative scientific dataset.

Historical identifiers recorded during the experiment include:

- scientific SHA-256 beginning `38a58ff...`;
- historical raw JSON SHA-256 beginning `1dcd...`.

The abbreviated values are retained exactly as recorded and should not be expanded without recovering the original artifact.

---

# 6. Behavioral baseline

The behavioral baseline established the task-level contextual separation.

Results:

- clean top-1 accuracy: 0.0052;
- corrupt top-1 accuracy: 0;
- mean clean margin: +1.672577;
- mean corrupt margin: -1.184263;
- overall mean margin: +0.488314.

Split means:

- train: +0.464910;
- calibration: +0.447998;
- test: +0.575439.

Bootstrap 95% CI:

\[
[0.125756,\;0.849913].
\]

Sign-flip p-value:

\[
p=0.007599.
\]

Variance decomposition indicated substantial heterogeneity:

- template variance ratio: 0.2351;
- pair variance ratio: 0.6647.

Classification:

`HELD_OUT_CONTEXTUAL_MARGIN_SUPPORTED`

Additional classification:

`SUBSTANTIAL_TEMPLATE_OR_PAIR_HETEROGENEITY`

No strong prompt-length correlation was detected.

---

# 7. Phase 1A — State extraction audit

HF-native layer-10 state extraction was performed for the three operational sectors.

Mean final-position clean/corrupt displacement norms were:

- S1: 19.11787;
- S2: 33.24892;
- S3: 15.83823.

All three perturbation matrices had rank 12.

PC1 variance proportions were:

- S1: 0.3261;
- S2: 0.4790;
- S3: 0.6007.

Cross-sector cosine values were:

- S1/S2: 0.3012;
- S1/S3: -0.2257;
- S2/S3: -0.0245.

The extraction audit passed.

**Status: PASS**

---

# 8. Phase 1B — Controlled sector intervention instrumentation

TransformerLens exploratory hooks were:

- P: `blocks.10.hook_resid_pre`;
- S: `blocks.10.hook_attn_out`;
- A: `blocks.10.hook_mlp_out`.

The calibration intervention set contained 48 records and three sector interventions per record, for 144 intervention conditions.

Hook integrity checks produced zero failures.

Sham/noninterference checks produced zero failures.

The intervention summaries were:

## P

- delta: 33.552713;
- recovery: -0.098062;
- median: 0.124403;
- reversal: 0.629708;
- clean-to-clean: -1.756836;
- clean-to-corrupt: +0.978841.

## S

- delta: 21.096608;
- recovery: -0.099907;
- median: 0.084910;
- reversal: 0.207301;
- clean-to-clean: -0.181152;
- clean-to-corrupt: -0.179036.

## A

- delta: 14.616817;
- recovery: +0.037923;
- median: 0.021286;
- reversal: 0.082642;
- clean-to-clean: -0.007650;
- clean-to-corrupt: -0.043783.

These results establish intervention instrumentation integrity.

They do not, by themselves, establish causal scientific relevance.

**Status: INSTRUMENTATION PASS ONLY**

---

# 9. R3 exploratory full factorial

An exploratory three-sector full-factorial analysis produced the following condition means:

| Condition | Result |
|---|---:|
| 000 | -3.8932 |
| 001 | -3.2651 |
| 010 | -4.3546 |
| 011 | -3.5846 |
| 100 | +0.9067 |
| 101 | +1.1379 |
| 110 | +5.0653 |
| 111 | +5.0653 |

The three-way contrast was:

\[
-0.373174.
\]

Pairwise contrasts were:

- PS: +4.43345;
- PA: -0.583414;
- SA: -0.044625.

Bootstrap 95% CI for the three-way contrast:

\[
[-0.4098,\;-0.3361].
\]

Bootstrap p-value:

\[
p=0.0001.
\]

The incremental triadic \(R^2\) was:

\[
0.00146.
\]

Grouped cross-validation delta RMSE:

\[
0.000895.
\]

Grouped CV F-test:

\[
p=0.084.
\]

The result was not accepted as evidence of triadic irreducibility.

Repeated template behavior appeared suspicious.

This analysis was therefore retained as exploratory evidence only.

**Triadic irreducibility: NOT ESTABLISHED**

---

# 10. TransformerLens equivalence audit

An equivalence audit compared TransformerLens and the Hugging Face implementation.

The parameterizations were not numerically identical.

The observed relative logit equivalence was approximately:

\[
0.999.
\]

The mismatch was classified as a numerical backend/parameterization mismatch.

The Hugging Face native implementation was retained as the authoritative backend.

This was treated as a numerical implementation issue, not as evidence against the mathematical framework.

---

# 11. HF-native state bank

The authoritative state bank was generated from the Hugging Face implementation.

Artifact:

`/content/ettr_ctl2/results/gpt2_phase1c1_state_bank.npz`

The P/S/A state matrices were:

\[
[192,768]
\]

in float16.

The state bank therefore provided the primary numerical representation for subsequent transport analysis.

---

# 12. Phase 1D.1 — Source-level residual audit

The GPT-2 layer-10 computation was audited against its actual implementation.

The relevant computation was:

\[
x
\rightarrow
\mathrm{LN}_1(x)
\rightarrow
\mathrm{Attention}
\rightarrow
x+\mathrm{Attention}
\rightarrow
\mathrm{LN}_2
\rightarrow
\mathrm{MLP}
\rightarrow
x+\mathrm{MLP}.
\]

A naive representation based simply on:

\[
x+a+m
\]

did not exactly reproduce the layer output.

The observed discrepancy was approximately:

\[
1.59\times10^{-4}
\]

relative, with maximum absolute discrepancy approximately:

\[
0.4258.
\]

The source-level residual semantics were therefore validated.

---

# 13. Contextual carrier identification

The candidate contextual carrier was the HF layer-10 block output at the final prompt position:

\[
R_{\mathrm{out}}^{(10)}(x)_{-1}
\in
\mathbb{R}^{768}.
\]

The train-only joint effective rank was:

\[
4.2479.
\]

The retained variance under different candidate dimensions was:

| \(d_K\) | Retention |
|---:|---:|
| 4 | 0.840754 |
| 8 | 0.919407 |
| 16 | 0.967531 |
| 32 | 0.990183 |
| 64 | 0.999205 |

This established a compact candidate contextual representation.

It did not establish that the underlying representation had intrinsic dimension 4.

---

# 14. Transport configuration selection

Selected transport configurations were:

| Sector | Dimension | Ridge |
|---|---:|---:|
| S1 | 64 | 100 |
| S2 | 64 | 100 |
| S3 | 64 | 10 |

Transport maps were selected using calibration performance.

The corresponding configuration manifest was:

`/content/ettr_ctl2/checkpoints/gpt2_phase1c3_selected_configs.json`

The transport maps were stored in:

`/content/ettr_ctl2/checkpoints/gpt2_phase1c3_selected_transport_maps.pkl`

PCA bases were stored in:

`/content/ettr_ctl2/checkpoints/gpt2_phase1c3_selected_pca_bases.pkl`

---

# 15. Contextual realization preflight

Candidate contextual realizations were evaluated at several carrier dimensions.

The candidate structure included:

- contextual carrier dimension \(d_K\);
- contextual PCA dimension;
- sector projection dimension;
- transport-map dimension;
- final contextual realization map.

The selected candidate was:

`dK4_pc10_pd10_tkfull_linear_ta1000.0`

It contained 3856 parameters.

Calibration mean normalized coherence defect:

\[
0.8573122753.
\]

Calibration median:

\[
0.7601979842.
\]

The candidate was selected on calibration data only.

---

# 16. Frozen held-out contextual realization

The selected contextual realization was frozen and evaluated on the held-out test set.

Test set size:

\[
N=48.
\]

Mean normalized coherence defect:

\[
1.0653109898.
\]

Median:

\[
1.0132859945.
\]

Standard deviation:

\[
0.2117352.
\]

Quantiles:

\[
q_{05}=0.8942034,
\]

\[
q_{25}=0.9673333,
\]

\[
q_{75}=1.0720689,
\]

\[
q_{95}=1.3908380.
\]

Minimum:

\[
0.8179572.
\]

Maximum:

\[
1.9806374.
\]

Absolute coherence defect mean:

\[
30.3436.
\]

The Phi-D-to-clean error mean was:

\[
29.6083.
\]

Phi-D-to-clean cosine:

\[
0.57665.
\]

The Phi-C-to-clean error mean was:

\[
0.525289.
\]

Phi-C-to-clean median error:

\[
0.381613.
\]

Phi-C-to-clean cosine:

\[
0.999922.
\]

The TK-to-clean error mean was:

\[
5.28990.
\]

TK-to-clean median:

\[
4.07392.
\]

TK-to-clean cosine:

\[
0.979617.
\]

The calibration-to-test mean defect gap was:

\[
0.208.
\]

The calibration-to-test median gap was:

\[
0.253.
\]

The frozen contextual realization therefore did not generalize successfully.

Classification:

`FROZEN_CONTEXTUAL_REALIZATION_GENERALIZATION_NOT_SUPPORTED`

---

# 17. Robustness analysis of the negative result

The negative held-out contextual realization result was tested against several robustness summaries.

Mean:

\[
1.0653109898.
\]

Median:

\[
1.0132859945.
\]

Median absolute deviation:

\[
0.048527.
\]

10% trimmed mean:

\[
1.027187.
\]

Fractions exceeding thresholds:

- >0.25: 100%;
- >0.50: 100%;
- >0.75: 100%;
- >1.00: 56.25%.

Template mean range:

\[
0.368.
\]

Pair mean range:

\[
0.6755.
\]

Robust outliers:

5.

Bootstrap mean 95% CI:

\[
[1.011149,\;1.131970].
\]

Bootstrap median 95% CI:

\[
[0.990756,\;1.025335].
\]

Template-grouped bootstrap 95% CI:

\[
[1.002389,\;1.138276].
\]

Pair-grouped bootstrap 95% CI:

\[
[1.009403,\;1.148491].
\]

Worst-quartile mean:

\[
0.981959.
\]

Lowest-half mean:

\[
0.956239.
\]

Maximum leave-one-out change:

\[
0.019475.
\]

These results supported the conclusion that the negative held-out result was not driven by one or two extreme observations.

Final classification:

`NEGATIVE_RESULT_ROBUST`

---

# 18. Interpretation of Phi-C and Phi-D

The analysis indicated a major asymmetry between the components used in the contextual realization.

Phi-C could closely reconstruct the clean representation under the evaluated comparison, with cosine approximately:

\[
0.999922.
\]

Phi-D was substantially weaker, with mean error:

\[
29.6083
\]

and cosine:

\[
0.57665.
\]

This identified Phi-D as a diagnostic weakness in the operational realization.

However, the experiment did not establish a causal explanation for why Phi-D was weak.

Therefore:

`PHI_D_WEAKNESS_DIAGNOSTIC`

but:

`PHI_D_CAUSAL_EXPLANATION_NOT_ESTABLISHED`

---

# 19. CTL interpretation

The formal CTL kernel was successfully implemented.

The experiment therefore supports the computational existence of the formal logical kernel.

However, formal CTL structure and empirical Transformer realization are distinct.

The experiment did not establish empirical identification of every mathematical object required for a complete CTL realization.

In particular:

- the formal logical kernel was supported;
- contextual carrier structure was operationalized;
- finite transport was operationalized;
- `Phi_C` was not robustly reconstructed;
- empirical coherence was not established;
- triadic irreducibility was not established;
- full geometric realization was not tested.

---

# 20. Triadic interpretation

The exploratory R3 full-factorial analysis generated a nonzero three-way contrast.

However, the following facts prevented interpretation as proof of mathematical triadic irreducibility:

1. the analysis was exploratory;
2. repeated-template behavior was suspicious;
3. the incremental predictive contribution was very small;
4. complexity-controlled held-out triadic comparison was not established;
5. a numerical three-way interaction is not equivalent to CTL mathematical irreducibility.

Therefore:

**TRIADIC IRREDUCIBILITY: NOT ESTABLISHED**

The existence of three measurable sectors also does not itself establish triadic irreducibility.

---

# 21. Negative-result synthesis

The central negative finding was that the selected contextual realization did not generalize from calibration to held-out test data.

The mean normalized coherence defect increased from:

\[
0.8573122753
\]

on calibration data to:

\[
1.0653109898
\]

on held-out test data.

The negative result remained robust under:

- mean;
- median;
- trimmed mean;
- MAD-based analysis;
- threshold exceedance;
- template-grouped bootstrap;
- pair-grouped bootstrap;
- leave-one-out analysis.

Therefore the result was classified:

`NEGATIVE_RESULT_ROBUST_ACROSS_PRIMARY_SUMMARIES`

---

# 22. Scientific closure

The experiment was closed after the primary contextual realization and robustness analyses.

The final scientific status was:

| Component | Status |
|---|---|
| CTL logical kernel | SUPPORTED |
| Dataset | SUPPORTED |
| Behavioral contextual margin | SUPPORTED WITH HETEROGENEITY |
| Operational sectors | SUPPORTED AS OPERATIONAL SECTORS |
| Controlled intervention | SUPPORTED |
| Sector transport | SUPPORTED WITH HETEROGENEITY |
| Contextual carrier | SUPPORTED |
| Train/calibration contextual realization | SUPPORTED AS TRAIN/CALIBRATION OPERATION |
| Frozen contextual realization generalization | NOT SUPPORTED |
| Negative robustness | SUPPORTED |
| `Phi_C` reconstruction | NOT SUPPORTED |
| `Phi_D` weakness | DIAGNOSTIC |
| `Phi_D` causal explanation | NOT ESTABLISHED |
| Triadic irreducibility | NOT ESTABLISHED |
| Geometric realization | NOT TESTED |

Overall:

`NEGATIVE_RESULT_ROBUST_ACROSS_PRIMARY_SUMMARIES`

---

# 23. Interpretation relative to the broader research program

The GPT-2 experiment should be regarded as a controlled empirical baseline rather than as a contemporary Transformer-general result.

GPT-2 Small is architecturally older and substantially smaller than modern open Transformer models.

Therefore the result should not be extrapolated automatically to architectures such as Llama 3.2 or later Transformer families.

The GPT-2 result is valuable precisely because it establishes a complete empirical record on a controlled, relatively simple Transformer substrate.

The subsequent Llama experiment provides an architectural contrast.

---

# 24. Hardware interpretation

The experiment was executed on an NVIDIA Tesla T4.

The hardware provided sufficient computational resources for the GPT-2 experiment.

Hardware execution is not part of the mathematical definition of ETTR or CTL.

Any numerical limitations associated with the T4 are therefore treated as properties of the computational realization rather than as modifications to the mathematical framework.

---

# 25. Reproducibility artifacts

Primary GPT-2 artifacts included:

`/content/ettr_ctl2/results/ctl_kernel_contract.json`

`/content/ettr_ctl2/results/gpt2_phase1c1_state_bank.npz`

`/content/ettr_ctl2/checkpoints/gpt2_phase1c3_selected_configs.json`

`/content/ettr_ctl2/checkpoints/gpt2_phase1c3_selected_transport_maps.pkl`

`/content/ettr_ctl2/checkpoints/gpt2_phase1c3_selected_pca_bases.pkl`

`/content/ettr_ctl2/checkpoints/gpt2_phase1d5e_contextual_realization_candidates.pkl`

Additional phase-specific diagnostics and statistical artifacts were retained in the experiment result directories.

---

# 26. Final scientific statement

ETTR-CTL-2 successfully established an operational experimental framework for examining selected ETTR/CTL structures on GPT-2 Small.

The experiment demonstrated:

- a measurable contextual behavioral effect;
- operationally identifiable Transformer sectors;
- controlled intervention instrumentation;
- finite sector-specific transport;
- a candidate contextual carrier;
- formal CTL kernel execution.

However, the stronger contextual realization did not generalize successfully to held-out data.

The negative result was robust across multiple statistical summaries and grouping strategies.

The experiment therefore does not provide empirical confirmation of a complete contextual realization or triadic irreducibility.

The appropriate scientific conclusion is:

> Selected ETTR/CTL structures can be operationalized and audited on GPT-2 Small, but the evaluated frozen contextual realization failed to generalize robustly to held-out data, and the experiment did not establish CTL triadic irreducibility or complete geometric realization.

This negative result is retained as an integral component of the ETTR/CTL empirical research record.
