# HF_Leaderboard_Lab_Results

**Project:** `L_R2R`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `SciPhi-AI/R2R`  
**Commit:** `9c5a94d151f9`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **51.81 ms** |
| Min latency | 47.55 ms |
| Max latency | 56.93 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **38** |
| Tokenization latency | 1.99 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5892 |
| Classification latency | 85.47 ms |
| Status | **PASS** |

**Input text tokenized:**
```
L_R2R (SciPhi-AI/R2R) — 529 files, 89036 source lines, licence MIT, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'l', '_', 'r', '##2', '##r', '(', 'sci', '##phi', '-', 'ai', '/', 'r', '##2', '##r', ')', '—', '52', '##9', 'files']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_