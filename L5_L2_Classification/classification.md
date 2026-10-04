# L5 Narrow / L2 General Classification — L_R2R
**Platform:** Anticloud | **Tier:** TIER_4_INFERENCE_AGENTS | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
L_R2R integrates the R2R (RAG to Riches) pipeline with Anticloud's KAMELOT_SEARCH and PAX 27B. Hybrid dense+sparse retrieval with cross-encoder reranking achieves higher precision than single-method retrieval. Narrow scope: Anticloud corpus only.

## L2 General
L2 General: L_R2R is the production-quality retrieval pipeline for any tier needing high-precision answers. TIER_7 clinical staff and TIER_4 inference engineers both access L_R2R through the same REST API.

## PAX 27B Integration
PAX 27B is the generation backend. L_R2R provides the highest-quality retrieval context: hybrid search finds more relevant chunks, cross-encoder reranking orders them correctly, PAX synthesizes the final answer.

## AIOSS Audit Chain
Every R2R query (query hash + dense hits hash + sparse hits hash + reranked order hash + synthesis hash) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
GDPR Art. 25 (local-only retrieval). NIST AI RMF 1.0 (grounded AI).
