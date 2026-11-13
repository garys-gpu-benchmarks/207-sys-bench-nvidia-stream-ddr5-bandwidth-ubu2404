# Results: 207 STREAM - CPU (Copy/Scale/Add/Triad)

**Main goal:** Measure sustained CPU STREAM bandwidth  
**Tools:** Compile src/stream.c with gcc -O3 -fopenmp and run build/stream

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_138 · recorded 2026-11-12). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 NVL (95830 MiB) · AMD EPYC 9374F 32-Core Processor · Ubuntu 24.04.5 LTS · kernel 6.8.0-138-generic · driver 595.91.07
- **Run:** 2026-11-12T22:43:57Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:27 · benchmark 00:01 · whole run 00:34
- **Source:** run 207_20261112_224357
- **Command:** `bash run_benchmark.sh --smoke --numa-node 0 --num-threads 4 --thread-affinity core --array-size 10000000 --num-iterations 2`

| # | Metric | Result |
|---|---|---|
| 1 | Best Copy bandwidth, GB/s (copy_bandwidth_gb_s) | 55.674099999999996 |
| 2 | Best Scale bandwidth, GB/s (scale_bandwidth_gb_s) | 56.3699 |
| 3 | Best Add bandwidth, GB/s (add_bandwidth_gb_s) | 55.8393 |
| 4 | Best Triad bandwidth, GB/s (triad_bandwidth_gb_s) | 56.019 |
<!-- /profile:smoke -->
