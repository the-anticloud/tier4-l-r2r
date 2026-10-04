# Ledger Status

**Project:** `L_R2R`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `SciPhi-AI/R2R` @ `9c5a94d151f9` (MIT)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `SciPhi-AI/R2R` |
| Commit | `9c5a94d151f90876bd7eb860f300a8fd662dc481` |
| Upstream licence | MIT |
| Licence class | permissive |
| Clone size | 18.26 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
