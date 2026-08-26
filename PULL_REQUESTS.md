# Pull Requests

## Merged

| Date | PR | Repo | Description |
|---|---|---|---|
| 2026-08-20 | [#52572](https://github.com/vllm-project/vllm/pull/52572) | vllm-project/vllm | shellcheck-py pre-commit hook |
| 2026-08-03 | [#50766](https://github.com/vllm-project/vllm/pull/50766) | vllm-project/vllm | Fix perf benchmark silently running at `tensor_parallel_size=1` instead of 4 |
| 2026-07-15 | [#48688](https://github.com/vllm-project/vllm/pull/48688) | vllm-project/vllm | Enable fp32 `head_dtype` torch.mm fast path on ROCm |
| 2026-06-04 | [#43625](https://github.com/vllm-project/vllm/pull/43625) | vllm-project/vllm | Bump fastsafetensors to v0.3.2 (drop git-source build for ROCm) |
| 2026-05-22 | [#78](https://github.com/foundation-model-stack/fastsafetensors/pull/78) | foundation-model-stack/fastsafetensors | Universal CUDA/ROCm wheel via runtime `dlopen` detection |
| 2026-04-29 | [#67](https://github.com/foundation-model-stack/fastsafetensors/pull/67) | foundation-model-stack/fastsafetensors | Remove `hipify-perl` build dependency |
| 2026-03-02 | [#35672](https://github.com/vllm-project/vllm/pull/35672) | vllm-project/vllm | Remove dead weight-shuffling code *(first vLLM PR)* |

## Open

| Opened | PR | Repo | Description | Status |
|---|---|---|---|---|
| 2026-08-25 | [#53813](https://github.com/vllm-project/vllm/pull/53813) | vllm-project/vllm | Multi-GPU CI coverage lint tool | Draft, exploratory |
| 2026-08-24 | [#53643](https://github.com/vllm-project/vllm/pull/53643) | vllm-project/vllm | MoE dispatch + Triton qzeros reshape tests (26 tests) | Approved by bnellnm, awaiting second review |
| 2026-08-21 | [#53341](https://github.com/vllm-project/vllm/pull/53341) | vllm-project/vllm | Fix 5 TODO-tagged shellcheck warnings | Awaiting review |
| 2026-05-07 | [#41978](https://github.com/vllm-project/vllm/pull/41978) | vllm-project/vllm | Fix wvSplitKrc kernel guard: restore CDNA support (was gfx950-only) | Draft, exploratory |
| 2026-04-29 | [#41187](https://github.com/vllm-project/vllm/pull/41187) | vllm-project/vllm | Fix LDS bank conflicts in vecMatMul reduction_smem layout | Awaiting review |
| 2026-04-24 | [#40827](https://github.com/vllm-project/vllm/pull/40827) | vllm-project/vllm | Rename LLMM1 to vecMatMul, refactor, fix RDNA4 correctness bugs | Under discussion |
