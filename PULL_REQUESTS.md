# Pull Requests

## Open

| Opened | PR | Repo | Description | Impact | Status |
|---|---|---|---|---|---|
| 08/30/2026 | [#54474](https://github.com/vllm-project/vllm/pull/54474) | vllm-project/vllm | Add `AITERConfig` object for AITER op toggles | Replaces ~16 loose `VLLM_ROCM_USE_AITER*` env vars with one typed, cache-hashed sub-config; unset config preserves current behavior | Awaiting review (supersedes #41159) |
| 08/30/2026 | [#54466](https://github.com/vllm-project/vllm/pull/54466) | vllm-project/vllm | Wire `indexer_kv_dtype` through on the MiniMax-M3 AMD path | Fixes a KV-cache dtype mismatch on the MiniMax-M3 sparse-attention indexer for ROCm; Hot Aisle-validated for correctness | Awaiting review |
| 08/29/2026 | [#54388](https://github.com/vllm-project/vllm/pull/54388) | vllm-project/vllm | Remove `get_cached_compilation_config`, read compilation config directly | Drops an unjustified cache (~9ns/call, ~1k calls at startup, 0 on the forward path) that had caused a silent wrong-kernel-dispatch bug across config swaps | Awaiting review (pinged mgoin + skyloevil) |
| 08/26/2026 | [#53925](https://github.com/vllm-project/vllm/pull/53925) | vllm-project/vllm | Add multi-GPU test groups for nightly-log-confirmed skips (fixes #53840) | Restores real execution to 11 of 12 files with silently skipped multi-GPU tests | Awaiting review |
| 08/25/2026 | [#53813](https://github.com/vllm-project/vllm/pull/53813) | vllm-project/vllm | Multi-GPU CI coverage lint tool | Would catch future silent multi-GPU skips automatically instead of relying on manual log audits | Draft, exploratory |
| 08/24/2026 | [#53643](https://github.com/vllm-project/vllm/pull/53643) | vllm-project/vllm | MoE dispatch + Triton qzeros reshape tests (26 tests) | Adds regression coverage for MoE dispatch and quantization reshape paths that had none | Approved by bnellnm, awaiting second review |
| 08/21/2026 | [#53341](https://github.com/vllm-project/vllm/pull/53341) | vllm-project/vllm | Fix 5 TODO-tagged shellcheck warnings | Clears long-standing suppressed lint warnings flagged in #52572 | Awaiting review |
| 05/07/2026 | [#41978](https://github.com/vllm-project/vllm/pull/41978) | vllm-project/vllm | Fix wvSplitKrc kernel guard: restore CDNA support (was gfx950-only) | Restores a GEMM kernel path to all CDNA GPUs instead of just gfx950 | Draft, exploratory |
| 04/29/2026 | [#41187](https://github.com/vllm-project/vllm/pull/41187) | vllm-project/vllm | Fix LDS bank conflicts in vecMatMul reduction_smem layout | Removes a memory-access bottleneck in the vecMatMul reduction kernel | Awaiting review |
| 04/24/2026 | [#40827](https://github.com/vllm-project/vllm/pull/40827) | vllm-project/vllm | Rename LLMM1 to vecMatMul, refactor, fix RDNA4 correctness bugs | Fixes real correctness bugs on RDNA4 (consumer GPUs), not just a rename | Under discussion |

## Merged

| Date | PR | Repo | Description | Impact |
|---|---|---|---|---|
| 08/20/2026 | [#52572](https://github.com/vllm-project/vllm/pull/52572) | vllm-project/vllm | shellcheck-py pre-commit hook | Replaced a custom shellcheck script with a maintained hook, catching issues the old script missed |
| 08/03/2026 | [#50766](https://github.com/vllm-project/vllm/pull/50766) | vllm-project/vllm | Fix perf benchmark silently running at `tensor_parallel_size=1` instead of 4 | Benchmark had been silently measuring the wrong config; results now reflect real TP=4 performance |
| 07/15/2026 | [#48688](https://github.com/vllm-project/vllm/pull/48688) | vllm-project/vllm | Enable fp32 `head_dtype` torch.mm fast path on ROCm | Closed a CUDA-only gate on a fast path PyTorch already supports on ROCm |
| 06/04/2026 | [#43625](https://github.com/vllm-project/vllm/pull/43625) | vllm-project/vllm | Bump fastsafetensors to v0.3.2 (drop git-source build for ROCm) | Removed a slow from-source build step for ROCm users in favor of a prebuilt wheel |
| 05/22/2026 | [#78](https://github.com/foundation-model-stack/fastsafetensors/pull/78) | foundation-model-stack/fastsafetensors | Universal CUDA/ROCm wheel via runtime `dlopen` detection | One wheel replaces separate CUDA/ROCm builds, simplifying packaging for both platforms |
| 04/29/2026 | [#67](https://github.com/foundation-model-stack/fastsafetensors/pull/67) | foundation-model-stack/fastsafetensors | Remove `hipify-perl` build dependency | Unblocked manylinux wheel builds for ROCm, which hipify-perl had been preventing |
| 03/02/2026 | [#35672](https://github.com/vllm-project/vllm/pull/35672) | vllm-project/vllm | Remove dead weight-shuffling code *(first vLLM PR)* | First vLLM contribution — removed dead code left over from a prior refactor |
