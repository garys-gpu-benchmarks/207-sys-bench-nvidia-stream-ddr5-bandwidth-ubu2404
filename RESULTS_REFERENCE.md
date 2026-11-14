# Results: 207 STREAM - CPU (Copy/Scale/Add/Triad)

**Main goal:** Measure sustained CPU STREAM bandwidth  
**Tools:** Compile src/stream.c with gcc -O3 -fopenmp and run build/stream

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_140 · recorded 2026-11-13). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 PCIe (81559 MiB) · Intel(R) Xeon(R) Platinum 8352Y CPU @ 2.20GHz · Ubuntu 24.04.5 LTS · kernel 6.8.0-138-generic · driver 595.91.07
- **Run:** 2026-11-13T20:28:13Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:53 · benchmark 00:02 · whole run 01:05
- **Source:** run 207_20261113_202813
- **Command:** `bash run_benchmark.sh --smoke --numa-node 0 --num-threads 4 --thread-affinity core --array-size 10000000 --num-iterations 2`

| # | Metric | Result |
|---|---|---|
| 1 | Best Copy bandwidth, GB/s (copy_bandwidth_gb_s) | 28.9508 |
| 2 | Best Scale bandwidth, GB/s (scale_bandwidth_gb_s) | 30.5463 |
| 3 | Best Add bandwidth, GB/s (add_bandwidth_gb_s) | 32.6164 |
| 4 | Best Triad bandwidth, GB/s (triad_bandwidth_gb_s) | 32.9066 |
<!-- /profile:smoke -->
