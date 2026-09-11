# ETTR-CTL-LLAMA-1

## Experiment

ETTR-CTL-LLAMA-1 is an empirical investigation of the operationalization of Empirical Triadic Transport Reconstruction (ETTR) and Contextual Transport Logic (CTL) using Meta Llama 3.2 3B.

## Model

- Model: `meta-llama/Llama-3.2-3B`
- Layers: 28
- Selected layer: 14
- Hidden dimension: 3072
- Attention heads: 24
- Key/value heads: 8
- Random seed: 42

## Computational environment

- Backend: Hugging Face Transformers
- Hardware: NVIDIA Tesla T4
- CUDA device: `cuda:0`
- Representation dtype: BF16

## Operational sectors

The experiment used three operational sectors:

- S1 — contextual interaction / attention output
- S2 — state propagation across depth / residual state entering block
- S3 — feature transformation / MLP output

These are operational sectors and should not be interpreted as proof that the Transformer has three ontologically fundamental components.

## Dataset

The experiment used 192 paired records.

Dataset SHA-256:

`7b14ddebef594859cf284deb5037ac9bb7e67956edb640012eaa257325e8769d`

## Major findings

The formal CTL structural interfaces were operationally instantiated.

Frozen linear transport showed heterogeneous held-out behavior across the three operational sectors:

- S1: statistically supported deterioration relative to identity.
- S2: near-null / unresolved effect.
- S3: small but statistically supported improvement.

The primary held-out numerical triadic predictive comparison did not support a triadic predictive advantage.

CTL irreducibility was not established.

The secondary target-rank robustness comparison was unresolved.

## Scientific status

This experiment is a closed empirical record. The negative and unresolved findings are retained as part of the experimental history and are not interpreted as evidence that the underlying mathematical framework is invalid.

## Limitations

The experiment did not empirically identify contextual or triadic admissibility, reconstruct `K_C` or `Phi_C`, establish full logical covariance, or establish CTL irreducibility.

The experiment was executed on an NVIDIA Tesla T4. The T4 does not provide native BF16 Tensor Core support; therefore the computational environment should be regarded as part of the numerical execution record rather than as evidence about the mathematical structure itself.

## Files

- `experiment_config.json` — computational configuration
- `results_summary.json` — machine-readable scientific results
- `dataset_manifest.json` — dataset identity and operationalization
- `hashes.txt` — SHA-256 integrity record
- `scientific_record.md` — detailed scientific record
