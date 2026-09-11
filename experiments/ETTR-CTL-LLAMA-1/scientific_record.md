# ETTR-CTL-LLAMA-1 Scientific Record

**Experiment ID:** ETTR-CTL-LLAMA-1  
**Model:** Meta Llama 3.2 3B base model  
**Primary model identifier:** `meta-llama/Llama-3.2-3B`  
**Random seed:** 42  
**Selected Transformer layer:** 14  
**Experimental status:** CLOSED  
**Scientific computation status:** CLOSED  

---

# 1. Objective

ETTR-CTL-LLAMA-1 was conducted as the second major empirical reconstruction experiment in the ETTR/Contextual Transport Logic (CTL) research program, following the completed GPT-2 Small experiment ETTR-CTL-2.

The purpose was not to demonstrate that a Transformer literally instantiates the mathematical structures of Contextual Calculus or Contextual Transport Logic. Instead, the experiment investigated whether selected mathematical and logical structures could be translated into explicit, auditable operational objects on a contemporary open Transformer architecture, and whether those operational objects exhibited empirically measurable behavior consistent with the intended transport framework.

The experiment therefore maintained a strict distinction between:

1. the mathematical structure defined by Contextual Calculus and CTL;
2. the operationalization of selected components of that structure on Transformer representations; and
3. the numerical execution of those operationalizations on GPU hardware.

The experiment was designed so that numerical or architectural limitations would be recorded as empirical limitations or decoherence rather than used to modify the mathematical definitions.

The principal empirical areas were:

- Transformer representation extraction;
- identification of three operational sectors;
- finite transport between paired clean and corrupted contextual states;
- formal instantiation of CTL structural interfaces;
- semantic realization of context-indexed observations;
- logical transport interface construction;
- triadic coherence and `Phi_C` interface construction;
- numerical investigation of triadic predictive sufficiency;
- held-out generalization of learned sector transports.

The experiment was explicitly closed without extending the study to curvature, holonomy, global descent, Cech cohomology, connection reconstruction, or other higher geometric constructions.

---

# 2. Research questions

The experiment addressed the following empirical questions.

## RQ1 — Can the selected Transformer representation pathways be operationalized as measurable transport sectors?

Three operational sectors were defined:

- **S1:** contextual interaction / attention output;
- **S2:** state propagation across depth / residual state entering the block;
- **S3:** feature transformation / MLP output.

These were treated as operational sectors rather than as a claim that the Transformer possesses three ontologically fundamental components.

---

## RQ2 — Can finite transport maps be learned between paired contextual states?

For each sector, a restricted linear transport map was learned from corrupted-state representations toward clean-state representations.

The empirical object was of the form:

\[
z_{\mathrm{corrupt}}^{(k)}
\overset{\widehat{T}^{(k)}}{\longrightarrow}
z_{\mathrm{clean}}^{(k)}.
\]

Transport maps were trained using calibration data and subsequently evaluated on held-out test data.

---

## RQ3 — Can the formal structural components of CTL be explicitly represented?

The experiment investigated whether the following formal objects could be represented without conflating them with ordinary binary labels or hidden-state thresholds:

\[
C,\quad
\mathcal{L}_C^{(k)},\quad
Adm_C,\quad
Adm_C^{(3)},\quad
\widehat{T}_{\gamma}^{(k)},\quad
K_C,\quad
\Phi_C.
\]

The experiment distinguished the existence of typed structural interfaces from empirical identification of their semantic or logical content.

---

## RQ4 — Does the numerical three-sector representation provide a predictive advantage over lower-order representations?

A controlled numerical comparison was performed between dyadic and triadic predictor sets.

This was explicitly treated as a test of **numerical triadic predictive sufficiency**, not as a direct test of CTL triadic irreducibility.

A positive or negative numerical result therefore could not, by itself, establish or refute the mathematical irreducibility claim of CTL.

---

## RQ5 — Do the learned sector transport maps generalize to held-out data?

The principal transport question was whether calibration-trained frozen transport maps generalized to held-out test conditions.

The result was evaluated separately for S1, S2, and S3.

---

# 3. Mathematical basis

The experiment was grounded in the Contextual Calculus and Contextual Transport Logic framework.

The mathematical framework treats context-indexed structures and transport as primary objects rather than assuming a pre-existing geometric manifold, metric, or connection.

The foundational triadic transport structure is represented schematically as:

\[
\tau =
(\tau^{(1)},\tau^{(2)},\tau^{(3)}).
\]

A coherent realization is represented abstractly as:

\[
C=\Phi(\tau^{(1)},\tau^{(2)},\tau^{(3)}).
\]

The mathematical hierarchy is:

\[
\text{triadic transport}
\rightarrow
\text{coherence}
\rightarrow
\text{dynamic equivalence}
\rightarrow
\text{smooth realization}
\rightarrow
\text{connection}
\rightarrow
\text{curvature/holonomy}
\rightarrow
\text{global descent}.
\]

Only the finite empirical transport and selected logical/interface levels of this hierarchy were investigated experimentally.

In particular, this experiment did NOT attempt to claim empirical reconstruction of:

- a smooth manifold;
- a connection;
- curvature;
- holonomy;
- global descent;
- Cech cohomology;
- or a complete geometric realization.

The CTL formal structure treats context-indexed syntax and admissibility as distinct from ordinary Boolean truth assignment. In particular:

\[
\text{undefined}\neq\text{false}.
\]

Likewise:

\[
\text{Boolean valuation}
\neq
\text{context-indexed logical carrier}.
\]

This distinction became operationally important during the CTL phases.

---

# 4. Operationalization principles

The experiment followed several methodological constraints.

## 4.1 Mathematical authority

The mathematical framework was treated as authoritative.

Numerical implementation was not permitted to redefine mathematical objects merely because a particular CUDA, PyTorch, Transformer implementation, or hardware configuration made a direct realization difficult.

---

## 4.2 Operational sectors are not ontological claims

S1, S2, and S3 were chosen because they correspond to measurable Transformer computation pathways.

Their existence as measurable pathways does not establish that the underlying architecture has exactly three fundamental computational sectors.

---

## 4.3 Intervention success is not automatically scientific success

Successful hooks, finite tensors, successful GPU execution, and successful extraction do not establish transport, causal relevance, coherence, or triadic irreducibility.

Instrumentation success and scientific success were therefore evaluated separately.

---

## 4.4 Held-out evaluation

Learned maps and predictive comparisons were evaluated on held-out data.

Calibration data were used for selection where specified. Test data were not used for model selection.

---

## 4.5 No post hoc mathematical adjustment

The mathematical interpretation was not modified to make observed Transformer behavior conform to the desired result.

Negative, null, heterogeneous, and unresolved outcomes were retained as scientific results.

---

# 5. Model

The model was:

`meta-llama/Llama-3.2-3B`

The audited architecture contained:

- 28 Transformer layers;
- hidden dimension 3072;
- 24 attention heads;
- 8 key/value heads;
- feed-forward dimension 8192;
- vocabulary size 128256;
- maximum context length 131072;
- BF16 model configuration;
- Llama 3 RoPE configuration with theta 500000;
- grouped-query attention (GQA);
- gated MLP architecture;
- RMSNorm/pre-normalized Transformer organization.

Layer 14 was selected for the principal representation experiment.

The selected layer was kept fixed throughout the subsequent state-bank and transport analyses.

---

# 6. Dataset

The experiment used a recovered and explicitly authorized dataset containing:

- 192 experimental records;
- clean and corrupted prompt conditions;
- ordered contextual pairs;
- template identifiers;
- split assignments;
- target-token identifiers;
- target-position information.

The authorized dataset SHA-256 was:

`7b14ddebef594859cf284deb5037ac9bb7e67956edb640012eaa257325e8769d`

Target-token identifiers were derived independently for Llama.

GPT-2 target-token IDs were not reused because tokenizer vocabularies differ across models.

---

## 6.1 Tokenization audit

The 192 clean and corrupted prompts were tokenized under the Llama tokenizer.

Prompt lengths ranged from 13 to 14 tokens.

Clean and corrupted prompts had equal lengths within each paired condition.

Of the 32 target names:

- 19 were single-token under the Llama tokenizer;
- 13 were multi-token.

The target-position operationalization was therefore defined explicitly rather than assuming that the target token itself had already been processed by the model.

---

# 7. Target-position operationalization

For a prompt \(P\), the target continuation begins at:

\[
p_T=L(P),
\]

where \(L(P)\) is the prompt length.

The hidden state used for predicting the next token was therefore the final prompt position:

\[
i_T=L(P)-1.
\]

The target token itself was not fed into the model when the target prediction was evaluated.

The target-position audit verified:

- exact prefix validity: 192/192;
- one-token target continuation: 192/192;
- equal clean/corrupted prompt lengths;
- equality of first-target positions across paired conditions;
- contextual target IDs were distinct;
- no cross-condition target overlap;
- valid split assignments.

The target-position operationalization audit therefore passed.

Artifact:

`llama_phase1c3_target_position_operationalization_audit.json`

---

# 8. Computational environment

The experiment was executed using:

- Python 3.13.15;
- PyTorch 2.11.0+cu128;
- Transformers 5.16.1;
- CUDA 12.8;
- NVIDIA Tesla T4;
- GPU compute capability 7.5.

The model was executed using BF16 representation.

The T4 does not possess native BF16 Tensor Core support. Therefore, successful BF16 execution on the T4 must not be interpreted as evidence of native BF16 Tensor Core acceleration.

This distinction is part of the numerical execution record.

The hardware was treated as an execution substrate rather than as a component of the mathematical theory.

---

# 9. Phase 1A — Architecture audit

The first phase verified the model and architecture before scientific extraction.

The audit confirmed:

- the intended model was loaded;
- the model architecture matched the expected Llama 3.2 3B configuration;
- 28 layers were present;
- hidden size was 3072;
- the attention configuration contained 24 query heads and 8 key/value heads;
- the selected layer was layer 14;
- the expected model configuration was accessible.

**Status: PASS**

No scientific inference was made from the architecture audit alone.

---

# 10. Phase 1B — Model execution and intervention audit

The model was loaded using an exact CPU BF16 checkpoint followed by:

`model.to(cuda:0, dtype=BF16)`

The resulting model contained:

- 254 CUDA parameter tensors;
- 3,212,749,824 parameters;
- 2 buffers;
- approximately 5.993 GiB of parameter storage.

Synthetic baseline logits had shape:

\[
(1,16,128256)
\]

and were finite.

The audit also tested noninterference.

Maximum and relative output differences under the relevant sham/nonintervention conditions were zero.

Sector extraction tensors were finite and passed norm sanity checks.

Parameter immutability was verified.

**Status: PASS**

This established that the numerical model execution and instrumentation were functioning.

It did not establish the scientific validity of transport or CTL claims.

---

# 11. Phase 1C — Dataset and target-position audit

The dataset was recovered and its authorized SHA-256 verified.

The target-position audit established the correct causal ordering:

\[
\text{prompt}
\rightarrow
\text{final prompt hidden state}
\rightarrow
\text{next-token prediction}.
\]

The target token was not supplied to the model before the target prediction was measured.

All 192 records passed the target-position checks.

**Status: PASS**

Artifact:

`/content/ettr_ctl_llama/results/llama_phase1c3_target_position_operationalization_audit.json`

---

# 12. Phase 1D.0 — State extraction audit

Layer 14 was instrumented to extract three operational sectors.

The operational sectors were:

### S1 — attention/contextual interaction

Attention output before the residual addition.

### S2 — state propagation

Decoder-layer input / residual state entering the selected block.

### S3 — feature transformation

MLP output before residual addition.

All extracted states had shape:

\[
[1,14,3072]
\]

before selection of the target position.

The final target-position vectors had dimension:

\[
3072.
\]

Representative state norms were:

- S1: 3.69046760
- S2: 10.57186508
- S3: 6.66964483

Representative cross-sector cosine values were:

- S1/S2: -0.00868703
- S1/S3: -0.29631329
- S2/S3: -0.04869696

All extracted tensors were finite.

**Status: PASS**

Artifact:

`/content/ettr_ctl_llama/results/llama_phase1d0_state_extraction_audit.json`

---

# 13. Phase 1D.2 — Full state-bank extraction

The full state bank contained 384 conditions:

\[
192\ \text{clean} + 192\ \text{corrupt}.
\]

Each operational sector was stored as a:

\[
384\times3072
\]

matrix in float32 on CPU after extraction.

The paired clean-corrupt displacement magnitudes were:

| Sector | Mean paired displacement |
|---|---:|
| S1 | 1.275078 |
| S2 | 2.597086 |
| S3 | 1.653374 |

State-bank hashes:

- S1: `9621683192d82c8874f198660015abe88aef356ef58cbb79cfef51cfa8103783`
- S2: `41679cd0a1b46103ae896edf0ff106718b17499eb12bdb3c68ccd3a3f1b898fb`
- S3: `173866d853a396050e252b227b2a1fb6769b32c75c98fa00e1b4929375c172b3`

Target-logit artifact hash:

`537fa43c8e278b8678de978c1dc2ec4ee5a1c77ca0a917dbf6a5823cf77ea58f`

Target-rank artifact hash:

`f4de73b588c465e0c1e41887a2eab7b1e0f2214d2d15dc0108b69e4063e2d472`

Artifact:

`/content/ettr_ctl_llama/results/llama_phase1d2_full_state_bank.npz`

---

# 14. Phase 1D.3 — Post-extraction audit

The state-bank structure was checked after extraction.

The bank contained:

- 192 clean conditions;
- 192 corrupted conditions;
- train/calibration/test split assignments.

The final split structure was:

- training: 192 rows;
- calibration: 96 rows;
- test: 96 rows.

**Status: PASS**

---

# 15. Phase 1E.0 — Transport preflight

Train-only PCA was performed for each sector.

Retention values were evaluated at several candidate dimensions.

## S1

| Dimension | Variance retention |
|---:|---:|
| 4 | 0.757898 |
| 8 | 0.899873 |
| 16 | 0.935448 |
| 32 | 0.964765 |
| 64 | 0.986598 |
| 128 | 0.997363 |

## S2

| Dimension | Variance retention |
|---:|---:|
| 4 | 0.818344 |
| 8 | 0.941898 |
| 16 | 0.962889 |
| 32 | 0.979103 |
| 64 | 0.990516 |
| 128 | 0.997810 |

## S3

| Dimension | Variance retention |
|---:|---:|
| 4 | 0.822104 |
| 8 | 0.933162 |
| 16 | 0.956174 |
| 32 | 0.974828 |
| 64 | 0.988609 |

## Joint state representation

| Dimension | Variance retention |
|---:|---:|
| 4 | 0.812318 |
| 8 | 0.933851 |
| 16 | 0.956118 |
| 32 | 0.974271 |
| 64 | 0.988308 |
| 128 | 0.997255 |

These values were used as a transport-preflight diagnostic.

Importantly, the selection of dimension \(d=4\) in the subsequent transport experiment was based on calibration performance, not on a claim that the representation was intrinsically four-dimensional.

---

# 16. Phase 1E.1 — Transport candidate selection

Candidate linear transport maps were evaluated over:

\[
d\in\{4,8,16,32,64\}
\]

and ridge regularization:

\[
\lambda\in
\{0.01,0.1,1,10,100,1000\}.
\]

PCA bases were fitted using training data only.

The transport maps used no intercept.

Candidate selection was performed using calibration data.

The selected configurations were:

### S1

- dimension: 4
- ridge: 0.01
- calibration NRMSE: 0.201006
- identity NRMSE: 0.202619
- cosine: 0.985794

### S2

- dimension: 4
- ridge: 1
- calibration NRMSE: 0.091608
- identity NRMSE: 0.090833
- cosine: 0.995769

### S3

- dimension: 4
- ridge: 0.01
- calibration NRMSE: 0.120509
- identity NRMSE: 0.119503
- cosine: 0.993117

Training-fit NRMSE values were:

- S1: 0.075175 versus identity 0.078320;
- S2: 0.045758 versus identity 0.046615;
- S3: 0.050468 versus identity 0.051745.

The transport checkpoint was:

`/content/ettr_ctl_llama/checkpoints/llama_phase1e1_selected_transport_maps.pkl`

The candidate-selection manifest was:

`/content/ettr_ctl_llama/results/llama_phase1e1_transport_candidate_selection.json`

The fact that all three selected maps used \(d=4\) was a calibration-selection result and was NOT interpreted as evidence of intrinsic four-dimensional Transformer geometry.

---

# 17. Phase 1E.2 — Frozen held-out transport

The selected transport maps were frozen and evaluated on the held-out test set.

## S1

Transport NRMSE:

\[
0.974842090
\]

Identity NRMSE:

\[
0.973854329
\]

Relative improvement:

\[
-0.104854\%.
\]

Transport cosine:

\[
0.158531
\]

Identity cosine:

\[
0.162613.
\]

Bootstrap estimate of identity-minus-transport NRMSE difference:

\[
-0.000987761
\]

with 95% CI:

\[
[-0.001486016,\,-0.000478748].
\]

This constitutes a statistically supported deterioration relative to identity.

---

## S2

Transport NRMSE:

\[
1.068554146
\]

Identity NRMSE:

\[
1.068859612
\]

Relative improvement:

\[
+0.010263\%.
\]

Transport cosine:

\[
-0.004318
\]

Identity cosine:

\[
-0.004375.
\]

Bootstrap estimate:

\[
+0.000305466
\]

with 95% CI:

\[
[-0.000336442,\,+0.000916010].
\]

The effect is near-null and unresolved.

---

## S3

Transport NRMSE:

\[
1.009386142
\]

Identity NRMSE:

\[
1.010317125
\]

Relative improvement:

\[
+0.073115\%.
\]

Transport cosine:

\[
0.027504
\]

Identity cosine:

\[
0.026982.
\]

Bootstrap estimate:

\[
+0.000930983
\]

with 95% CI:

\[
[0.000425511,\,+0.001460057].
\]

This is a small but statistically supported improvement.

---

## Frozen transport conclusion

The frozen linear transport operationalization therefore exhibited heterogeneous held-out behavior:

- **S1:** statistically supported deterioration;
- **S2:** unresolved near-null effect;
- **S3:** small but statistically supported improvement.

Final transport classification:

`FROZEN_TRANSPORT_HAS_MIXED_OR_NULL_GENERALIZATION`

This was retained as a scientific result rather than averaged away across sectors.

Decoded transport versus decoded identity showed:

- S1: 0.682013799 versus 0.681535960 — transport worse;
- S2: 0.604606829 versus 0.604751237 — transport improves;
- S3: 0.702645672 versus 0.703139990 — transport improves.

---

# 18. CTL phases

The CTL portion of the experiment was deliberately separated from the numerical transport analysis.

The objective was to establish whether formal CTL structural objects could be operationally represented without incorrectly equating them with hidden-state thresholds or ordinary binary covariates.

The formal CTL tuple was represented schematically as:

\[
\mathfrak{CTL}
=
(C,
\{E_C\},
\{L_C^{(k)}\},
\{Adm_C,Adm_C^{(3)}\},
\{\widehat{T}_\gamma^{(k)}\},
\{K_C,\Phi_C\}).
\]

---

# 19. Phase 1F.0 — Formal CTL structural preflight

A formal CTL structure was assembled containing:

- context-indexed carriers;
- event domains;
- contextual admissibility placeholders;
- triadic admissibility placeholders;
- logical transport registry;
- composition scaffold;
- coherence registry;
- typed `Phi_C` interfaces.

No empirical truth rule was invented at this stage.

No hidden-state threshold was treated as a CTL axiom.

No binary feature was automatically interpreted as a CTL proposition.

**Status: PASS**

The phase established that the formal structural interfaces could be instantiated as software objects without making empirical claims about their values.

---

# 20. Phase 1F.1 — Initial methodological failure and correction

The first attempted empirical CTL realization contained a methodological error.

It used hidden-state MAD thresholds and represented triadic admissibility as a pairwise conjunction.

This created a situation in which zero mismatch could become tautological by construction.

That implementation was rejected as scientifically invalid.

The problem was not treated as evidence against CTL.

Instead, the implementation was corrected so that:

- empirical admissibility was not invented;
- triadic admissibility was not reduced to pairwise conjunction;
- hidden-state thresholding was not used to define logical truth;
- semantic valuation remained distinct from structural admissibility;
- no numerical object was falsely designated as `K_C` or `Phi_C`.

The corrected implementation formally instantiated the CTL structure without claiming empirical identification of its semantic or logical values.

This correction is retained in the scientific record because it documents a methodological failure and the subsequent removal of a potential tautology.

---

# 21. Corrected Phase 1F.1 — Formal CTL structure realization

The corrected implementation produced:

- 192 contexts;
- 3 event domains per context;
- 576 context-indexed logical carriers;
- 192 partial admissibility domains;
- 192 triadic admissibility objects;
- 192 CTL morphisms;
- 192 logical transport objects;
- 3 sector maps for each logical transport object;
- composition scaffolding;
- 192 `K_C` coherence carriers;
- 192 typed `Phi_C` interfaces.

The following were deliberately NOT empirically identified:

- contextual admissibility;
- triadic admissibility;
- logical transport preservation;
- logical operation preservation;
- `K_C`;
- `Phi_C`.

Final status:

`FORMAL_CTL_STRUCTURE_IMPLEMENTATION_PASS`

---

# 22. Phase 1F.2A — State-bank row-order audit

Before semantic CTL realization, the ordering of the state bank was audited.

The actual state-bank ordering was interleaved:

\[
bank[2i]=clean_i,
\]

\[
bank[2i+1]=corrupt_i.
\]

This was explicitly checked rather than assumed.

The candidate interleaved clean/corrupt ordering passed:

- target-position consistency: 384/384;
- Llama target-ID consistency: 384/384.

Artifact:

`/content/ettr_ctl_llama/results/llama_phase1f2a_state_bank_row_order_audit.json`

---

# 23. Phase 1F.2 — Semantic realization

The semantic realization stage created:

- 384 context-condition semantic models;
- 1152 semantic valuations.

The primary semantic observations were target-logit and target-rank differences between clean and corrupted conditions.

The clean-minus-corrupt target-logit difference had:

- mean: 0.069010417;
- median: 0.

The target-rank improvement had:

- mean: 0.432291667;
- median: 0.

Split-level results were:

### Train

- N = 96;
- target-logit difference mean: 0.063802083;
- target-rank difference mean: -0.90625.

### Calibration

- N = 48;
- target-logit difference mean: -0.055989583;
- target-rank difference mean: -0.708333.

### Test

- N = 48;
- target-logit difference mean: 0.204427083;
- target-rank difference mean: 4.25.

The semantic layer was therefore operationally realized, but contextual and triadic admissibility remained unresolved.

No semantic threshold was imposed to manufacture a Boolean result.

No `Phi_C` was reconstructed.

No collapse of truth, coherence, and state similarity was permitted.

Final status:

`CTL_SEMANTIC_REALIZATION_OPERATIONAL_PASS`

---

# 24. Phase 1F.3 — Logical transport covariance structure audit

The logical transport structure was audited independently of semantic value invariance.

The audit contained:

- 576 context-indexed carriers;
- 576 event structures;
- 576 morphisms;
- 1152 semantic observations;
- endpoint typing: 576/576.

The audit explicitly recognized that semantic values need not be invariant under transport.

The following were NOT empirically established:

- admissibility preservation;
- logical operation preservation;
- full composition/functoriality;
- semantic covariance in the strong sense.

The triadic transport registry was retained as a three-sector formal object.

No pairwise reduction was substituted for the triadic registry.

Final status:

`LOGICAL_TRANSPORT_STRUCTURE_OPERATIONAL_PASS`

The strongest scientifically justified interpretation is that the formal CTL carrier/event/semantic/logical-transport interfaces were operationally realized with preserved context and sector typing.

Empirical admissibility preservation, logical operation preservation, and full logical covariance were not identified.

---

# 25. Phase 1F.4 — Triadic coherence and Phi_C interface audit

This phase audited the existence and typing of the formal triadic coherence interfaces.

The implementation contained:

- 192 formal `Adm_C^(3)` objects;
- 192 `K_C` coherence carriers;
- 192 typed `Phi_C` interfaces.

However, none of the following was empirically identified:

- contextual admissibility;
- triadic admissibility;
- an empirical `K_C`;
- an empirical `Phi_C`.

In particular, the following were explicitly NOT designated as `K_C` or `Phi_C`:

- hidden states;
- semantic observations;
- numerical transport outputs.

The phase therefore established interface-level operational support but not empirical reconstruction of the mathematical coherence map.

Final status:

`TRIADIC_COHERENCE_INTERFACE_OPERATIONAL_PASS_NOT_EMPIRICALLY_IDENTIFIED`

---

# 26. Phase 1F.5 — Triadic irreducibility identifiability audit

The formal CTL structure contained a triadic object.

However, this does not mean that empirical triadic irreducibility had been identified.

The audit established:

- a formal triadic CTL object was available;
- lower-order reducts could be formally defined;
- invalid reductions were rejected;
- held-out train/calibration/test capacity was available.

The capacity structure was:

- train: 96;
- calibration: 48;
- test: 48.

However, a sufficient complexity-control scheme had not been frozen for an empirical mathematical irreducibility claim.

Specifically, the experiment did not establish a final:

- parameter-matched dyadic/triadic comparison;
- effective-dimension-matched comparison;
- penalty-controlled nested comparison.

Therefore the mathematical CTL irreducibility question was not empirically identifiable in this experiment.

Final status:

`TRIADIC_IRREDUCIBILITY_NOT_CURRENTLY_IDENTIFIABLE`

A numerical triadic predictive-sufficiency experiment was therefore treated only as a lower-level empirical probe.

---

# 27. Phase 1F.6 — Numerical triadic predictive sufficiency

A numerical comparison was performed using the target logit clean-corrupt difference as the response variable.

Predictors were paired state differences.

The comparison used an equal six-predictor budget.

The dyadic representation used:

- 3 predictors from one selected sector;
- 3 predictors from another selected sector.

The triadic representation used:

- 2 predictors from S1;
- 2 predictors from S2;
- 2 predictors from S3.

Dyadic selection was performed using calibration data.

The final regression used ridge regularization:

\[
\lambda=1.
\]

No PCA refitting was performed after the checkpoint schema audit.

The primary held-out result supported a **triadic predictive disadvantage** rather than a triadic predictive advantage.

Final classification:

`NUMERICAL_TRIADIC_PREDICTIVE_SUFFICIENCY_NOT_SUPPORTED_CTL_IRREDUCIBILITY_NOT_ESTABLISHED`

Numerical status:

`HELD_OUT_TRIADIC_PREDICTIVE_DISADVANTAGE_SUPPORTED`

This result was not interpreted as a refutation of CTL irreducibility because the numerical predictor comparison is not mathematically equivalent to the CTL irreducibility proposition.

---

# 28. Phase 1F.8 — Secondary target-rank robustness analysis

A secondary analysis examined target-rank behavior.

The comparator was the S2+S3 dyadic representation.

The held-out results were:

Dyadic MSE:

\[
418.5135378562957
\]

Triadic MSE:

\[
416.46091629639744
\]

Difference:

\[
2.0526215598982844
\]

Relative improvement:

\[
0.49045523602705765\%.
\]

The bootstrap 95% confidence interval for the corresponding effect was:

\[
[-0.44518365371362373,\,
6.3634280161301415].
\]

Because the confidence interval crossed zero, the target-rank triadic effect was unresolved.

Final status:

`HELD_OUT_TRIADIC_PREDICTIVE_EFFECT_UNRESOLVED`

This result provided no basis for claiming a robust triadic advantage.

---

# 29. Transport interpretation

The frozen transport experiment produced heterogeneous behavior.

The scientifically justified statement is:

> The frozen linear transport operationalization exhibits heterogeneous held-out behavior across the three operational sectors: a small but statistically supported improvement for S3, an unresolved near-null effect for S2, and a statistically supported deterioration for S1.

This heterogeneity is compatible with several possible explanations, including architectural differences in the functional organization of the sectors.

However, this experiment did not establish a causal explanation for the heterogeneity.

In particular, it did not establish that:

- GQA caused the S1 deterioration;
- RMSNorm caused the S2 behavior;
- gated MLP structure caused the S3 improvement;
- or any individual architectural component caused the observed transport differences.

Architecture may affect the empirical transport behavior, but causal attribution requires a separately controlled architectural comparison.

---

# 30. CTL interpretation

The experiment provided evidence for the **operational representation of formal CTL structures**, but not for complete empirical realization of CTL semantics.

Supported operational elements included:

- context indexing;
- event-domain separation;
- logical-carrier typing;
- morphism typing;
- sector-specific transport registration;
- triadic transport registry;
- coherence-interface representation;
- typed `Phi_C` interface representation.

Not empirically established were:

- contextual admissibility;
- triadic admissibility;
- empirical `K_C`;
- empirical `Phi_C`;
- logical operation preservation;
- admissibility preservation;
- full logical covariance;
- CTL irreducibility.

Therefore, the correct conclusion is not:

> "The Transformer implements CTL."

The stronger and more accurate statement is:

> "Selected formal CTL structures were operationally instantiated as typed computational objects, while their empirical semantic, admissibility, coherence, and irreducibility properties remained incompletely identified."

---

# 31. Binary features and Boolean logic

The experiment explicitly distinguished ordinary binary computational features from CTL logical structure.

A binary variable with values:

\[
0,1
\]

is not automatically a CTL proposition.

Likewise:

\[
\text{binary feature}
\neq
\text{context-indexed logical carrier}.
\]

A genuine CTL logical realization requires explicit representation of:

\[
C,
\mathcal L_C^{(k)},
Adm_C,
Adm_C^{(3)},
\widehat{T}_\gamma^{(k)},
K_C,
\Phi_C.
\]

The earlier temptation to treat ordinary binary `transfer` or `presentation` features as if they constituted CTL logical computation was therefore rejected.

The current experiment correctly avoided making that identification.

This distinction is important for future work.

---

# 32. Relationship between numerical transport and formal CTL

The experiment kept two levels separate.

## Formal level

The CTL structure specifies context-indexed carriers, admissibility, morphisms, logical transport, and coherence-related objects.

## Numerical level

Transformer hidden-state differences and learned finite-dimensional linear maps provide numerical observables and transport approximations.

The numerical transport experiment therefore should not be read as a direct empirical measurement of every formal CTL object.

The strongest demonstrated bridge was:

\[
z_{\mathrm{corrupt}}^{(k)}
\rightarrow
\widehat{T}^{(k)}
\rightarrow
z_{\mathrm{clean}}^{(k)}
\]

combined with explicit context and sector typing.

The higher-level map:

\[
C=\Phi(\tau^{(1)},\tau^{(2)},\tau^{(3)})
\]

was represented as a formal interface but not empirically reconstructed.

---

# 33. Negative and unresolved findings

The following negative or unresolved findings are part of the scientific result.

## 33.1 Frozen transport

Frozen transport did not generalize uniformly.

- S1 deteriorated;
- S2 was near-null;
- S3 showed a small improvement.

Therefore no uniform cross-sector transport advantage was established.

---

## 33.2 Triadic predictive sufficiency

The primary numerical held-out triadic comparison did not support a triadic predictive advantage.

Instead, a held-out triadic predictive disadvantage was supported for the target-logit analysis.

---

## 33.3 Target-rank robustness

The secondary target-rank comparison was unresolved.

Its small apparent triadic improvement was not statistically decisive.

---

## 33.4 CTL irreducibility

CTL irreducibility was not established.

The numerical predictor experiment cannot substitute for the mathematical irreducibility claim.

---

## 33.5 `Phi_C`

An empirical contextual realization map `Phi_C` was not reconstructed.

---

## 33.6 `K_C`

An empirical coherence carrier `K_C` was not identified.

---

## 33.7 Admissibility

Contextual and triadic admissibility were represented formally but were not empirically identified.

---

## 33.8 Full logical covariance

Full preservation of logical operations and admissibility under transport was not tested.

---

## 33.9 Geometric realization

No smooth geometric realization was established.

No connection, curvature, holonomy, or global descent result was obtained.

---

# 34. Why the negative results are retained

The purpose of the experiment was empirical reconstruction, not confirmation.

Consequently, a result such as:

\[
\text{triadic predictive advantage not supported}
\]

is retained as an experimental result rather than reinterpreted as a software problem solely because it does not support the theoretical expectation.

Likewise, a mixed transport result is retained rather than averaged into a single positive claim.

The experiment therefore functions as a falsification-sensitive empirical layer around the mathematical framework.

---

# 35. Architectural interpretation

Llama 3.2 3B differs substantially from GPT-2 Small.

Relevant architectural differences include:

- substantially greater depth;
- substantially larger hidden dimension;
- grouped-query attention;
- RMSNorm/pre-normalization;
- rotary positional encoding;
- gated MLP structure;
- different tokenizer and vocabulary;
- substantially different parameter scale and training regime.

Consequently, the empirical behavior of S1/S2/S3 cannot be assumed to be architecture-invariant.

The experiment therefore does not claim that the GPT-2 and Llama sector results should coincide.

The Llama results demonstrate that the ETTR operationalization can be executed on a substantially more contemporary Transformer organization, but they do not establish architecture-independent transport laws.

---

# 36. Hardware and numerical interpretation

The experiment ran successfully on an NVIDIA Tesla T4.

The T4 provided sufficient memory and compute for the present 3B-parameter model experiment.

However, the T4 belongs to an earlier accelerator generation than current transformer-oriented accelerators.

Most importantly, the T4 is compute capability 7.5 and does not have native BF16 Tensor Core support.

Therefore:

\[
\text{BF16 representation}
\neq
\text{native BF16 Tensor Core acceleration on T4}.
\]

This is a numerical execution constraint.

It does not alter the mathematical definition of CTL or ETTR.

Future experiments on newer accelerators may produce different numerical performance characteristics, particularly for BF16, FP8, memory bandwidth, attention kernels, and large-scale matrix operations.

Such differences should be treated as numerical/hardware factors rather than silently incorporated into the mathematical framework.

---

# 37. Scientific closure

The scientific computation for ETTR-CTL-LLAMA-1 was closed after the completion of the CTL and numerical triadic analyses.

The final closure was:

### Formal CTL structure

**SUPPORTED**

The formal CTL carrier, event, morphism, logical-transport, triadic, coherence-interface, and typed `Phi_C` structures were operationally represented.

### Contextual/triadic admissibility

**NOT EMPIRICALLY IDENTIFIED**

### `K_C`

**NOT IDENTIFIED**

### `Phi_C`

**NOT RECONSTRUCTED**

### Logical transport covariance

**NOT FULLY TESTED**

### Frozen sector transport

**MIXED OR NULL GENERALIZATION**

### Primary numerical triadic predictive advantage

**NOT SUPPORTED**

### Primary numerical triadic result

**HELD-OUT TRIADIC PREDICTIVE DISADVANTAGE SUPPORTED**

### Target-rank robustness

**UNRESOLVED**

### CTL irreducibility

**NOT ESTABLISHED**

### Geometric realization

**NOT TESTED**

The overall interpretation is therefore deliberately conservative.

---

# 38. Overall experiment classification

The experiment does NOT justify the statement:

> "Llama 3.2 3B empirically proves Contextual Transport Logic."

It also does NOT justify:

> "The failure of triadic prediction disproves the mathematical triadic structure."

The appropriate interpretation is:

> ETTR-CTL-LLAMA-1 successfully operationalized selected formal CTL structures and finite sector-specific transport procedures on Llama 3.2 3B. The resulting frozen transport maps exhibited heterogeneous held-out behavior, with a statistically supported improvement for S3, a near-null unresolved effect for S2, and a statistically supported deterioration for S1. The primary numerical triadic predictive comparison did not support a triadic predictive advantage, while a secondary target-rank comparison remained unresolved. Formal CTL irreducibility, empirical admissibility, empirical coherence realization, and `Phi_C` reconstruction were not established.

The experiment therefore constitutes a **mixed empirical result with strong operational support for the structural implementation layer but no empirical confirmation of the stronger CTL irreducibility or coherence claims**.

---

# 39. Phase-status summary

| Phase | Purpose | Status |
|---|---|---|
| 1A | Architecture audit | PASS |
| 1B | Model execution/intervention audit | PASS |
| 1C.3 | Target-position operationalization | PASS |
| 1D.0 | State extraction audit | PASS |
| 1D.2 | Full state-bank extraction | PASS |
| 1D.3 | Post-extraction audit | PASS |
| 1E.0 | Transport preflight | PASS |
| 1E.1 | Transport candidate selection | PASS |
| 1E.2 | Frozen held-out transport | MIXED/NULL GENERALIZATION |
| 1F.0 | Formal CTL structural preflight | PASS |
| 1F.1 | Initial CTL empirical realization | REJECTED — METHODOLOGICAL TAUTOLOGY |
| Corrected 1F.1 | Formal CTL structure realization | PASS |
| 1F.2A | State-bank row-order audit | PASS |
| 1F.2 | CTL semantic realization | OPERATIONAL PASS |
| 1F.3 | Logical transport covariance structure | OPERATIONAL PASS |
| 1F.4 | Triadic coherence / `Phi_C` interfaces | OPERATIONAL PASS; NOT EMPIRICALLY IDENTIFIED |
| 1F.5 | Triadic irreducibility identifiability | NOT IDENTIFIABLE |
| 1F.6 | Numerical triadic predictive sufficiency | NOT SUPPORTED |
| 1F.8 | Target-rank robustness | UNRESOLVED |
| 1F.9 | Scientific closure | CLOSED |

---

# 40. Principal numerical results

## Frozen transport

| Sector | Transport NRMSE | Identity NRMSE | Relative change | Interpretation |
|---|---:|---:|---:|---|
| S1 | 0.974842090 | 0.973854329 | -0.104854% | Supported deterioration |
| S2 | 1.068554146 | 1.068859612 | +0.010263% | Near-null / unresolved |
| S3 | 1.009386142 | 1.010317125 | +0.073115% | Small supported improvement |

---

## Target-rank secondary analysis

| Measure | Value |
|---|---:|
| Dyadic MSE | 418.5135378562957 |
| Triadic MSE | 416.46091629639744 |
| MSE difference | 2.0526215598982844 |
| Relative improvement | 0.49045523602705765% |
| Bootstrap 95% CI | [-0.44518365371362373, 6.3634280161301415] |
| Interpretation | Unresolved |

---

# 41. Reproducibility information

The experiment should be reproduced only from the archived experiment configuration, dataset identity, notebook/code version, and numerical artifacts.

Important reproducibility identifiers include:

**Dataset SHA-256**

`7b14ddebef594859cf284deb5037ac9bb7e67956edb640012eaa257325e8769d`

**S1 state-bank SHA-256**

`9621683192d82c8874f198660015abe88aef356ef58cbb79cfef51cfa8103783`

**S2 state-bank SHA-256**

`41679cd0a1b46103ae896edf0ff106718b17499eb12bdb3c68ccd3a3f1b898fb`

**S3 state-bank SHA-256**

`173866d853a396050e252b227b2a1fb6769b32c75c98fa00e1b4929375c172b3`

**Target-logit SHA-256**

`537fa43c8e278b8678de978c1dc2ec4ee5a1c77ca0a917dbf6a5823cf77ea58f`

**Target-rank SHA-256**

`f4de73b588c465e0c1e41887a2eab7b1e0f2214d2d15dc0108b69e4063e2d472`

---

# 42. Primary artifacts

The principal experiment artifacts included:

`/content/ettr_ctl_llama/results/llama_colab_authentication_verification_v2.json`

`/content/ettr_ctl_llama/results/llama_phase1c3_target_position_operationalization_audit.json`

`/content/ettr_ctl_llama/results/llama_phase1d0_state_extraction_audit.json`

`/content/ettr_ctl_llama/results/llama_phase1d2_full_state_bank.npz`

`/content/ettr_ctl_llama/results/llama_phase1f2a_state_bank_row_order_audit.json`

`/content/ettr_ctl_llama/checkpoints/llama_phase1e1_selected_transport_maps.pkl`

`/content/ettr_ctl_llama/results/llama_phase1e1_transport_candidate_selection.json`

Additional phase-specific CTL and numerical result artifacts were retained in the experiment result directory.

Large numerical artifacts should be archived separately from the GitHub scientific record where appropriate.

---

# 43. Recommended archival interpretation

This record should be treated as the historical scientific record of ETTR-CTL-LLAMA-1.

Subsequent experiments should not silently modify the conclusions recorded here.

If a methodological error is discovered later, the appropriate procedure is to create a new experiment or explicit revision record while preserving this historical record.

The experiment should therefore remain identifiable by:

`ETTR-CTL-LLAMA-1`

and future reruns should receive new experiment identifiers.

---

# 44. Final scientific statement

ETTR-CTL-LLAMA-1 demonstrates that a substantial contemporary Transformer architecture can serve as a numerical substrate for an explicit ETTR/CTL operational framework, including context indexing, sector-specific representation extraction, finite transport estimation, and formal CTL structural interfaces.

However, the experiment does not establish that the Transformer empirically realizes the complete mathematical CTL structure.

The frozen transport maps do not generalize uniformly across sectors. The primary numerical triadic predictive comparison does not support a triadic predictive advantage, while the secondary target-rank result remains unresolved. Formal CTL irreducibility, empirical admissibility, empirical coherence, and `Phi_C` reconstruction remain unestablished.

These negative and unresolved outcomes are retained as part of the experiment's scientific content.

The experiment is therefore closed with the following high-level classification:

**FORMAL CTL STRUCTURE: SUPPORTED OPERATIONALLY**

**FROZEN TRANSPORT: HETEROGENEOUS / MIXED-NULL HELD-OUT GENERALIZATION**

**NUMERICAL TRIADIC ADVANTAGE: NOT SUPPORTED**

**CTL TRIADIC IRREDUCIBILITY: NOT ESTABLISHED**

**EMPIRICAL `K_C`: NOT IDENTIFIED**

**EMPIRICAL `Phi_C`: NOT RECONSTRUCTED**

**GEOMETRIC REALIZATION: NOT TESTED**

**OVERALL: MIXED EMPIRICAL RESULT; SCIENTIFICALLY CLOSED**
