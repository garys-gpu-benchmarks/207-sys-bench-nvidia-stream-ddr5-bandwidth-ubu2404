# Results: 207 STREAM - CPU (Copy/Scale/Add/Triad)

**Main goal:** Measure sustained CPU STREAM bandwidth  
**Tools:** Compile src/stream.c with gcc -O3 -fopenmp and run build/stream

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_139 · recorded 2026-11-13). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 PCIe (81559 MiB) · Intel(R) Xeon(R) Platinum 8352Y CPU @ 2.20GHz · Ubuntu 24.04.5 LTS · kernel 6.8.0-138-generic · driver 595.91.07
- **Run:** 2026-11-13T13:58:04Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:55 · benchmark 00:01 · whole run 01:06
- **Source:** run 207_20261113_135804
- **Command:** `bash run_benchmark.sh --smoke --numa-node 0 --num-threads 4 --thread-affinity core --array-size 10000000 --num-iterations 2`

| # | Metric | Result |
|---|---|---|
| 1 | Best Copy bandwidth, GB/s (copy_bandwidth_gb_s) | 27.4652 |
| 2 | Best Scale bandwidth, GB/s (scale_bandwidth_gb_s) | 29.0137 |
| 3 | Best Add bandwidth, GB/s (add_bandwidth_gb_s) | 30.848599999999998 |
| 4 | Best Triad bandwidth, GB/s (triad_bandwidth_gb_s) | 31.1725 |
<!-- /profile:smoke -->
