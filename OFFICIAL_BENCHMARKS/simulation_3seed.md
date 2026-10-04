# 3-Seed Simulation — L_R2R

**Seeds:** `96657` · `27994` · `62193`

**Seed method:** `sha256("L_R2R")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `L_R2R`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 7.0143 | 0.1587 | ±0.3111 |
| throughput_tokens_per_sec | 1659.2333 | 27.2769 | ±53.4627 |
| p50_latency_ms | 43.94 | 4.0215 | ±7.8821 |
| p99_latency_ms | 101.8333 | 7.8888 | ±15.462 |
| ttft_ms | 24.81 | 1.7439 | ±3.418 |
| mmlu_proxy | 0.7243 | 0.0262 | ±0.0514 |
| hellaswag_proxy | 0.7743 | 0.0151 | ±0.0296 |
| truthfulqa_proxy | 0.5662 | 0.0375 | ±0.0735 |
| arc_proxy | 0.7091 | 0.0311 | ±0.061 |
| complexity_cyclomatic | 4.01 | 0.3269 | ±0.6407 |
| maintainability_index | 66.7867 | 4.1531 | ±8.1401 |
| security_issues_high | 0.6667 | 0.9428 | ±1.8479 |
| dependency_freshness_pct | 76.8 | 2.9631 | ±5.8077 |
| test_coverage_pct | 54.7333 | 10.585 | ±20.7466 |
| doc_coverage_pct | 60.7333 | 8.5986 | ±16.8533 |
| memory_mb | 150.5667 | 12.0815 | ±23.6797 |
| gpu_util_pct | 67.3333 | 7.5562 | ±14.8102 |
| openssf_score | 6.3133 | 0.2963 | ±0.5807 |
| eu_ai_act_compliance_pct | 84.2333 | 6.144 | ±12.0422 |
| slsa_level | 1.0 | 0.0 | ±0.0 |

## Per-Seed Raw Results

| Metric | Seed 96657 | Seed 27994 | Seed 62193 |
|--------|------------|------------|------------|
| trl_score | 7.238 | 6.918 | 6.887 |
| throughput_tokens_per_sec | 1667.4 | 1687.8 | 1622.5 |
| p50_latency_ms | 43.26 | 39.39 | 49.17 |
| p99_latency_ms | 90.83 | 108.93 | 105.74 |
| ttft_ms | 23.06 | 27.19 | 24.18 |
| mmlu_proxy | 0.6873 | 0.7428 | 0.7428 |
| hellaswag_proxy | 0.7688 | 0.7592 | 0.7949 |
| truthfulqa_proxy | 0.5162 | 0.5758 | 0.6066 |
| arc_proxy | 0.7485 | 0.6725 | 0.7063 |
| complexity_cyclomatic | 4.47 | 3.74 | 3.82 |
| maintainability_index | 63.82 | 72.66 | 63.88 |
| security_issues_high | 0 | 2 | 0 |
| dependency_freshness_pct | 74.0 | 80.9 | 75.5 |
| test_coverage_pct | 69.7 | 47.0 | 47.5 |
| doc_coverage_pct | 57.1 | 52.5 | 72.6 |
| memory_mb | 158.4 | 159.8 | 133.5 |
| gpu_util_pct | 77.5 | 59.4 | 65.1 |
| openssf_score | 6.26 | 5.98 | 6.7 |
| eu_ai_act_compliance_pct | 87.7 | 75.6 | 89.4 |
| slsa_level | 1 | 1 | 1 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._