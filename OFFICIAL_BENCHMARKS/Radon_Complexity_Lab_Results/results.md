# Radon_Complexity_Lab_Results
**Project:** `L_R2R` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'A', 'score': 3.025}`
- **complexity_grade:** `A`
- **complexity_score:** `3.025`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_R2R\UPSTREAM\py\core\_anticloud_egress.py - A (79.55)
E:\fent`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_R2R\UPSTREAM\py\core\_anticloud_egress.py
    F 38:0 _is_frontier - A (4)
    F 43:0 guarded_connect - A (4)
    F 61:0 install - A (3)
    F 33:0 is_offline - A (1)
    C 29:0 EgressDenied - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_R2R\UPSTREAM\py\migrations\env.py
    F 28:0 include_object - A (2)
    F 23:0 get_schema_name - A (1)
    F 36:0 run_migrations_offline - A (1)
    F 58:0 run_migrations_online - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_R2R\UPSTREAM\py\r2r\mcp.py
    F 9:0 format_search_results_for_llm - C (20)
    F 5:0 id_to_shorthand - A (1)
    F 107:0 search - A (1)
    F 128:0 rag - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_R2R\UPSTREAM\py\r2r\serve.py
    F 22:0 create_app - B (9)
    F 61:0 run_server - B (7)
    F 103:0 main - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_R2R\UPSTREAM\py\r2r\__init__.py
    F 18:0 get_version - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\L_R2R\UPSTREAM\py\sdk\async_client.py
    M 88:4 R2RAsyncClient._handle_response - B (6)
    M 47:4 R2RAsyncClient._make_request - A (5)
    M 72:4 R2RAsyncClient._make_streaming_request - A (4)
    C 25:0 R2RAsyncClient - A (3)
    M 28:4 R2RAsyncClient.__init__ - A (2)
    M 120:4 R2RAsyncClient.set_api_key - A (2)
    M 111:4 R2RAsyncClient.close - A (1)
    M 114:4 R2RAsyncClient.__aenter__ - A (1)
    M 117:4 R2RAsync
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_