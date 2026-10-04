# Deploy Guide — L_R2R
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, r2r 0.x, FAISS, BM25, cross-encoder reranker, PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, r2r 0.x, FAISS-cpu 1.7+, rank-bm25 0.2+, cross-encoder model (~400MB), PAX 27B.

## Environment
8GB RAM for retrieval pipeline. GPU for cross-encoder and PAX. KAMELOT_SEARCH index required.

## AIOSS Integration
```bash
aioss init --module L_R2R --output ./l_r2r.aioss
aioss append --chain ./l_r2r.aioss --payload ./output.bin --module L_R2R
aioss verify --chain ./l_r2r.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_R2R",
    aioss_chain="./L_R2R.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_R2R.aioss --verbose
python -m L_R2R.tests.smoke
```
