# Results: 114 hipMemcpy Bandwidth Test (H2D, D2H, D2D)

**Main goal:** Measure HIP H2D/D2H/D2D transfer bandwidth  
**Tools:** Build via scripts/build.sh if needed; run bin/hip_memcpy_bw

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_138 · recorded 2026-11-12). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-147-generic · driver 7.1.9.31600000
- **Run:** 2026-11-12T23:02:01Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:13 · benchmark 00:02 · whole run 00:27
- **Source:** run 114_20261112_230201
- **Command:** `bash run_benchmark.sh --smoke --device-id 0 --direction all --pinned-memory true --min-bytes 1024 --max-bytes 268435456 --step-factor 2 --warmup-iters 1 --num-iterations 10`

| # | Metric | Result |
|---|---|---|
| 1 | H2D bandwidth at max transfer size, GB/s (bandwidth_h2d_gb_s) | 55.302 |
| 2 | D2H bandwidth at max transfer size, GB/s (bandwidth_d2h_gb_s) | 56.542 |
| 3 | D2D bandwidth at max transfer size, GB/s (bandwidth_d2d_gb_s) | 919.433 |
| 4 | H2D latency at min transfer size, us (latency_h2d_us) | 12.742 |
| 5 | D2H latency at min transfer size, us (latency_d2h_us) | 11.794 |
| 6 | D2D latency at min transfer size, us (latency_d2d_us) | 4.453 |
<!-- /profile:smoke -->
