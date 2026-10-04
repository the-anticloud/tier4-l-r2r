# Developer Cookbook — L_R2R
**Stack:** Python 3.11, r2r 0.x, FAISS, BM25, cross-encoder reranker, PAX 27B, AIOSS_FORMAT
**Domain:** R2R: production RAG-to-riches pipeline with hybrid search and reranking for Anticloud

## Production RAG query
```python
from l_r2r import R2RPipeline

r2r = R2RPipeline(
    dense_index="./kamelot_index/",
    pax_model="./pax-27b-q4.gguf",
    reranker_model="cross-encoder/ms-marco-MiniLM-L-6-v2",
    aioss_chain="./r2r.aioss"
)

result = r2r.query(
    "What are the GPU requirements for PAX 27B inference on T4?",
    top_k_dense=20, top_k_sparse=20, top_k_final=5
)
print(result.answer)
for chunk in result.top_chunks:
    print(f"  [{chunk.score:.3f}] {chunk.source}: {chunk.text[:60]}...")
print(f"Chain: {result.chain_hash}")
```

## Ingest new documents
```python
r2r.ingest("E:/fenta/Downloads/The Anticloud/TIER_4_INFERENCE_AGENTS/K_NANOVLLM/README.md")
```

## Benchmark retrieval precision
```python
bench = r2r.benchmark(test_set="./anticloud_rag_bench.jsonl")
print(f"Precision@5: {bench.precision_at_5:.3f}")
print(f"MRR: {bench.mrr:.3f}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
