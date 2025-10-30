# FSampler Experiment Analysis Report

**Generated:** 2025-10-22 15:00:02

**Total Experiments:** 42

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [Baseline Performance](#baseline-performance)
3. [FSampler Performance](#fsampler-performance)
4. [All Experiments Table](#all-experiments-table)
5. [Ablation Studies](#ablation-studies)
6. [Best Configurations](#best-configurations)
7. [Statistical Analysis](#statistical-analysis)
8. [Recommendations](#recommendations)

---

## Executive Summary

This report analyzes **42 experiments** comparing baseline sampling with FSampler acceleration.

- **Baseline runs:** 1
- **FSampler runs:** 41
- **Average time saved:** 19.0% (30.47s)
- **Average NFE reduction:** 19.6%

- **Average SSIM:** 0.9331
- **Min SSIM:** 0.7279
- **Max SSIM:** 0.9818

---

## Baseline Performance

**Reference measurements without FSampler optimization**

- **Average Runtime:** 160.26s
- **Average NFE (Model Calls):** 20.0

### Baseline Experiments Detail

| Sampler   | Scheduler   |   Steps |   NFE |   Time (s) |   SSIM |   RMSE |   MAE |
|:----------|:------------|--------:|------:|-----------:|-------:|-------:|------:|
| res_2s    | simple      |      20 |    20 |   160.2574 |    nan |    nan |   nan |


---

## FSampler Performance

- **Average Runtime:** 129.79s
- **Average NFE:** 16.1
- **Average NFE Reduction:** 19.63%
- **Average Time Saved:** 19.01%
- **Average Time Saved (seconds):** 30.47s

**Quality Metrics (vs Baseline):**
- **Average SSIM:** 0.9331
- **Min SSIM:** 0.7279
- **Max SSIM:** 0.9818
- **Average RMSE:** 0.0437
- **Average MAE:** 0.0205


---

## All Experiments Table

Complete data for all experiments:

| Sampler   | Scheduler   | Skip Mode   | Adaptive       |   Anchor Interval |   Max Consec Skips |   Steps |   NFE |   Skipped |   NFE Red % |   Time (s) |   Time Saved % |     SSIM |     RMSE |      MAE |
|:----------|:------------|:------------|:---------------|------------------:|-------------------:|--------:|------:|----------:|------------:|-----------:|---------------:|---------:|---------:|---------:|
| res_2s    | simple      | h2/s2       | learning       |            4.0000 |             2.0000 |      20 |    15 |         5 |     25.0000 |   119.5049 |        25.4294 |   0.9282 |   0.0532 |   0.0180 |
| res_2s    | simple      | h2/s3       | learning       |            4.0000 |             2.0000 |      20 |    16 |         4 |     20.0000 |   125.6168 |        21.6156 |   0.9533 |   0.0354 |   0.0135 |
| res_2s    | simple      | h2/s4       | learning       |            4.0000 |             2.0000 |      20 |    17 |         3 |     15.0000 |   134.7864 |        15.8938 |   0.9818 |   0.0173 |   0.0066 |
| res_2s    | simple      | h2/s5       | learning       |            4.0000 |             2.0000 |      20 |    18 |         2 |     10.0000 |   144.1199 |        10.0698 |   0.9782 |   0.0196 |   0.0074 |
| res_2s    | simple      | h3/s3       | learning       |            4.0000 |             2.0000 |      20 |    16 |         4 |     20.0000 |   127.2152 |        20.6182 |   0.9649 |   0.0339 |   0.0110 |
| res_2s    | simple      | h3/s4       | learning       |            4.0000 |             2.0000 |      20 |    17 |         3 |     15.0000 |   135.5275 |        15.4313 |   0.9645 |   0.0259 |   0.0102 |
| res_2s    | simple      | h3/s5       | learning       |            4.0000 |             2.0000 |      20 |    18 |         2 |     10.0000 |   143.6787 |        10.3450 |   0.9756 |   0.0211 |   0.0079 |
| res_2s    | simple      | h4/s4       | learning       |            4.0000 |             2.0000 |      20 |    17 |         3 |     15.0000 |   134.2366 |        16.2369 |   0.9601 |   0.0303 |   0.0111 |
| res_2s    | simple      | h4/s5       | learning       |            4.0000 |             2.0000 |      20 |    18 |         2 |     10.0000 |   142.7970 |        10.8952 |   0.9460 |   0.0335 |   0.0153 |
| res_2s    | simple      | adaptive    | learning       |            4.0000 |             2.0000 |      20 |    11 |         9 |     45.0000 |    86.5800 |        45.9744 |   0.7341 |   0.1634 |   0.1120 |
| res_2s    | simple      | adaptive    | learning       |            3.0000 |             2.0000 |      20 |    10 |        10 |     50.0000 |    77.4249 |        51.6872 |   0.7279 |   0.1365 |   0.0809 |
| res_2s    | simple      | none        | none           |          nan      |           nan      |      20 |    20 |         0 |      0.0000 |   160.2574 |         0.0000 | nan      | nan      | nan      |
| res_2s    | simple      | h2/s2       | grad_est       |            3.0000 |             2.0000 |      20 |    15 |         5 |     25.0000 |   117.8479 |        26.4634 |   0.9282 |   0.0532 |   0.0180 |
| res_2s    | simple      | h2/s3       | grad_est       |            3.0000 |             2.0000 |      20 |    16 |         4 |     20.0000 |   127.9758 |        20.1436 |   0.9533 |   0.0354 |   0.0135 |
| res_2s    | simple      | h2/s4       | grad_est       |            3.0000 |             2.0000 |      20 |    17 |         3 |     15.0000 |   135.1462 |        15.6693 |   0.9818 |   0.0173 |   0.0066 |
| res_2s    | simple      | h2/s5       | grad_est       |            3.0000 |             2.0000 |      20 |    18 |         2 |     10.0000 |   144.0706 |        10.1005 |   0.9782 |   0.0196 |   0.0074 |
| res_2s    | simple      | h3/s3       | grad_est       |            3.0000 |             2.0000 |      20 |    16 |         4 |     20.0000 |   132.2025 |        17.5062 |   0.9649 |   0.0339 |   0.0110 |
| res_2s    | simple      | h3/s4       | grad_est       |            3.0000 |             2.0000 |      20 |    17 |         3 |     15.0000 |   138.1894 |        13.7703 |   0.9645 |   0.0259 |   0.0102 |
| res_2s    | simple      | h3/s5       | grad_est       |            3.0000 |             2.0000 |      20 |    18 |         2 |     10.0000 |   148.6958 |         7.2144 |   0.9756 |   0.0211 |   0.0079 |
| res_2s    | simple      | h4/s4       | grad_est       |            3.0000 |             2.0000 |      20 |    17 |         3 |     15.0000 |   143.4588 |        10.4823 |   0.9601 |   0.0303 |   0.0111 |
| res_2s    | simple      | h4/s5       | grad_est       |            3.0000 |             2.0000 |      20 |    18 |         2 |     10.0000 |   151.8300 |         5.2587 |   0.9460 |   0.0335 |   0.0153 |
| res_2s    | simple      | adaptive    | grad_est       |            3.0000 |             2.0000 |      20 |    10 |        10 |     50.0000 |    81.8061 |        48.9533 |   0.7279 |   0.1365 |   0.0809 |
| res_2s    | simple      | h2/s2       | learn+grad_est |            3.0000 |             2.0000 |      20 |    15 |         5 |     25.0000 |   123.0512 |        23.2165 |   0.9282 |   0.0532 |   0.0180 |
| res_2s    | simple      | h2/s3       | learn+grad_est |            3.0000 |             2.0000 |      20 |    16 |         4 |     20.0000 |   126.0248 |        21.3610 |   0.9533 |   0.0354 |   0.0135 |
| res_2s    | simple      | h2/s4       | learn+grad_est |            3.0000 |             2.0000 |      20 |    17 |         3 |     15.0000 |   134.4398 |        16.1101 |   0.9818 |   0.0173 |   0.0066 |
| res_2s    | simple      | h2/s5       | learn+grad_est |            3.0000 |             2.0000 |      20 |    18 |         2 |     10.0000 |   145.3496 |         9.3024 |   0.9782 |   0.0196 |   0.0074 |
| res_2s    | simple      | h3/s3       | learn+grad_est |            3.0000 |             2.0000 |      20 |    16 |         4 |     20.0000 |   129.8191 |        18.9934 |   0.9649 |   0.0339 |   0.0110 |
| res_2s    | simple      | h3/s4       | learn+grad_est |            3.0000 |             2.0000 |      20 |    17 |         3 |     15.0000 |   139.8102 |        12.7590 |   0.9645 |   0.0259 |   0.0102 |
| res_2s    | simple      | h3/s5       | learn+grad_est |            3.0000 |             2.0000 |      20 |    18 |         2 |     10.0000 |   146.9049 |         8.3319 |   0.9756 |   0.0211 |   0.0079 |
| res_2s    | simple      | h4/s4       | learn+grad_est |            3.0000 |             2.0000 |      20 |    17 |         3 |     15.0000 |   143.0197 |        10.7562 |   0.9601 |   0.0303 |   0.0111 |
| res_2s    | simple      | h4/s5       | learn+grad_est |            3.0000 |             2.0000 |      20 |    18 |         2 |     10.0000 |   148.9903 |         7.0306 |   0.9460 |   0.0335 |   0.0153 |
| res_2s    | simple      | adaptive    | learn+grad_est |            3.0000 |             2.0000 |      20 |    10 |        10 |     50.0000 |    78.0991 |        51.2665 |   0.7279 |   0.1365 |   0.0809 |
| res_2s    | simple      | h2/s2       | none           |          nan      |           nan      |      20 |    15 |         5 |     25.0000 |   119.7724 |        25.2625 |   0.9282 |   0.0532 |   0.0180 |
| res_2s    | simple      | h2/s3       | none           |          nan      |           nan      |      20 |    16 |         4 |     20.0000 |   127.6063 |        20.3742 |   0.9533 |   0.0354 |   0.0135 |
| res_2s    | simple      | h2/s4       | none           |          nan      |           nan      |      20 |    17 |         3 |     15.0000 |   137.9882 |        13.8959 |   0.9818 |   0.0173 |   0.0066 |
| res_2s    | simple      | h2/s5       | none           |          nan      |           nan      |      20 |    18 |         2 |     10.0000 |   145.5012 |         9.2078 |   0.9782 |   0.0196 |   0.0074 |
| res_2s    | simple      | h3/s3       | none           |          nan      |           nan      |      20 |    16 |         4 |     20.0000 |   128.7951 |        19.6324 |   0.9649 |   0.0339 |   0.0110 |
| res_2s    | simple      | h3/s4       | none           |          nan      |           nan      |      20 |    17 |         3 |     15.0000 |   138.3945 |        13.6424 |   0.9645 |   0.0259 |   0.0102 |
| res_2s    | simple      | h3/s5       | none           |          nan      |           nan      |      20 |    18 |         2 |     10.0000 |   147.8264 |         7.7569 |   0.9756 |   0.0211 |   0.0079 |
| res_2s    | simple      | h4/s4       | none           |          nan      |           nan      |      20 |    17 |         3 |     15.0000 |   140.3732 |        12.4077 |   0.9601 |   0.0303 |   0.0111 |
| res_2s    | simple      | h4/s5       | none           |          nan      |           nan      |      20 |    18 |         2 |     10.0000 |   148.0242 |         7.6335 |   0.9460 |   0.0335 |   0.0153 |
| res_2s    | simple      | adaptive    | none           |          nan      |           nan      |      20 |    10 |        10 |     50.0000 |    78.6854 |        50.9006 |   0.7279 |   0.1365 |   0.0809 |

---

## Configuration Performance Comparison

Individual performance of each skip mode × adaptive mode configuration.

Each row represents a separate experimental run compared to baseline.


### All FSampler Configurations

| Skip Mode   | Adaptive Mode   |   Anchor Int |   Max Consec |   SSIM |   NFE Red % |     NFE |   Time (s) |   Skipped |   Time Saved % |   RMSE |    MAE |
|:------------|:----------------|-------------:|-------------:|-------:|------------:|--------:|-----------:|----------:|---------------:|-------:|-------:|
| adaptive    | grad_est        |       3.0000 |       2.0000 | 0.7279 |     50.0000 | 10.0000 |    81.8061 |   10.0000 |        48.9533 | 0.1365 | 0.0809 |
| adaptive    | learn+grad_est  |       3.0000 |       2.0000 | 0.7279 |     50.0000 | 10.0000 |    78.0991 |   10.0000 |        51.2665 | 0.1365 | 0.0809 |
| adaptive    | learning        |       3.0000 |       2.0000 | 0.7279 |     50.0000 | 10.0000 |    77.4249 |   10.0000 |        51.6872 | 0.1365 | 0.0809 |
| adaptive    | learning        |       4.0000 |       2.0000 | 0.7341 |     45.0000 | 11.0000 |    86.5800 |    9.0000 |        45.9744 | 0.1634 | 0.1120 |
| h2/s2       | grad_est        |       3.0000 |       2.0000 | 0.9282 |     25.0000 | 15.0000 |   117.8479 |    5.0000 |        26.4634 | 0.0532 | 0.0180 |
| h2/s2       | learn+grad_est  |       3.0000 |       2.0000 | 0.9282 |     25.0000 | 15.0000 |   123.0512 |    5.0000 |        23.2165 | 0.0532 | 0.0180 |
| h2/s2       | learning        |       4.0000 |       2.0000 | 0.9282 |     25.0000 | 15.0000 |   119.5049 |    5.0000 |        25.4294 | 0.0532 | 0.0180 |
| h2/s3       | grad_est        |       3.0000 |       2.0000 | 0.9533 |     20.0000 | 16.0000 |   127.9758 |    4.0000 |        20.1436 | 0.0354 | 0.0135 |
| h2/s3       | learn+grad_est  |       3.0000 |       2.0000 | 0.9533 |     20.0000 | 16.0000 |   126.0248 |    4.0000 |        21.3610 | 0.0354 | 0.0135 |
| h2/s3       | learning        |       4.0000 |       2.0000 | 0.9533 |     20.0000 | 16.0000 |   125.6168 |    4.0000 |        21.6156 | 0.0354 | 0.0135 |
| h2/s4       | grad_est        |       3.0000 |       2.0000 | 0.9818 |     15.0000 | 17.0000 |   135.1462 |    3.0000 |        15.6693 | 0.0173 | 0.0066 |
| h2/s4       | learn+grad_est  |       3.0000 |       2.0000 | 0.9818 |     15.0000 | 17.0000 |   134.4398 |    3.0000 |        16.1101 | 0.0173 | 0.0066 |
| h2/s4       | learning        |       4.0000 |       2.0000 | 0.9818 |     15.0000 | 17.0000 |   134.7864 |    3.0000 |        15.8938 | 0.0173 | 0.0066 |
| h2/s5       | grad_est        |       3.0000 |       2.0000 | 0.9782 |     10.0000 | 18.0000 |   144.0706 |    2.0000 |        10.1005 | 0.0196 | 0.0074 |
| h2/s5       | learn+grad_est  |       3.0000 |       2.0000 | 0.9782 |     10.0000 | 18.0000 |   145.3496 |    2.0000 |         9.3024 | 0.0196 | 0.0074 |
| h2/s5       | learning        |       4.0000 |       2.0000 | 0.9782 |     10.0000 | 18.0000 |   144.1199 |    2.0000 |        10.0698 | 0.0196 | 0.0074 |
| h3/s3       | grad_est        |       3.0000 |       2.0000 | 0.9649 |     20.0000 | 16.0000 |   132.2025 |    4.0000 |        17.5062 | 0.0339 | 0.0110 |
| h3/s3       | learn+grad_est  |       3.0000 |       2.0000 | 0.9649 |     20.0000 | 16.0000 |   129.8191 |    4.0000 |        18.9934 | 0.0339 | 0.0110 |
| h3/s3       | learning        |       4.0000 |       2.0000 | 0.9649 |     20.0000 | 16.0000 |   127.2152 |    4.0000 |        20.6182 | 0.0339 | 0.0110 |
| h3/s4       | grad_est        |       3.0000 |       2.0000 | 0.9645 |     15.0000 | 17.0000 |   138.1894 |    3.0000 |        13.7703 | 0.0259 | 0.0102 |
| h3/s4       | learn+grad_est  |       3.0000 |       2.0000 | 0.9645 |     15.0000 | 17.0000 |   139.8102 |    3.0000 |        12.7590 | 0.0259 | 0.0102 |
| h3/s4       | learning        |       4.0000 |       2.0000 | 0.9645 |     15.0000 | 17.0000 |   135.5275 |    3.0000 |        15.4313 | 0.0259 | 0.0102 |
| h3/s5       | grad_est        |       3.0000 |       2.0000 | 0.9756 |     10.0000 | 18.0000 |   148.6958 |    2.0000 |         7.2144 | 0.0211 | 0.0079 |
| h3/s5       | learn+grad_est  |       3.0000 |       2.0000 | 0.9756 |     10.0000 | 18.0000 |   146.9049 |    2.0000 |         8.3319 | 0.0211 | 0.0079 |
| h3/s5       | learning        |       4.0000 |       2.0000 | 0.9756 |     10.0000 | 18.0000 |   143.6787 |    2.0000 |        10.3450 | 0.0211 | 0.0079 |
| h4/s4       | grad_est        |       3.0000 |       2.0000 | 0.9601 |     15.0000 | 17.0000 |   143.4588 |    3.0000 |        10.4823 | 0.0303 | 0.0111 |
| h4/s4       | learn+grad_est  |       3.0000 |       2.0000 | 0.9601 |     15.0000 | 17.0000 |   143.0197 |    3.0000 |        10.7562 | 0.0303 | 0.0111 |
| h4/s4       | learning        |       4.0000 |       2.0000 | 0.9601 |     15.0000 | 17.0000 |   134.2366 |    3.0000 |        16.2369 | 0.0303 | 0.0111 |
| h4/s5       | grad_est        |       3.0000 |       2.0000 | 0.9460 |     10.0000 | 18.0000 |   151.8300 |    2.0000 |         5.2587 | 0.0335 | 0.0153 |
| h4/s5       | learn+grad_est  |       3.0000 |       2.0000 | 0.9460 |     10.0000 | 18.0000 |   148.9903 |    2.0000 |         7.0306 | 0.0335 | 0.0153 |
| h4/s5       | learning        |       4.0000 |       2.0000 | 0.9460 |     10.0000 | 18.0000 |   142.7970 |    2.0000 |        10.8952 | 0.0335 | 0.0153 |



**Baseline Reference:** SSIM = 1.0000 (by definition), 
NFE = 20.0, 
Time = 160.26s

---

## Best Configurations

### Best Quality (Highest SSIM)

- **Skip Mode:** h2/s4
- **Adaptive Mode:** learning
- **Sampler:** res_2s
- **SSIM:** 0.9818
- **Runtime:** 134.79s
- **Time Saved:** 15.9%
- **NFE:** 17
- **NFE Reduction:** 15.0%

### Best Time Savings (SSIM ≥ 0.95)

- **Skip Mode:** h2/s3
- **Adaptive Mode:** learning
- **Sampler:** res_2s
- **SSIM:** 0.9533
- **Runtime:** 125.62s
- **Time Saved:** 21.6%
- **NFE:** 16
- **NFE Reduction:** 20.0%

---

## Statistical Analysis

### Configuration Summary

- **Samplers tested:** res_2s
- **Schedulers tested:** simple
- **Skip modes tested:** adaptive, h2/s2, h2/s3, h2/s4, h2/s5, h3/s3, h3/s4, h3/s5, h4/s4, h4/s5, none
- **Adaptive modes tested:** grad_est, learn+grad_est, learning, none
- **Model types tested:** flux-dev

### Quality Distribution

- **Mean SSIM:** 0.9331
- **Median SSIM:** 0.9601
- **Std Dev SSIM:** 0.0784
- **Min SSIM:** 0.7279
- **Max SSIM:** 0.9818

### Efficiency Distribution

- **Mean NFE Reduction:** 19.17%
- **Median NFE Reduction:** 15.00%
- **Max NFE Reduction:** 50.00%

- **Mean Time Saved:** 18.56%
- **Median Time Saved:** 15.55%
- **Max Time Saved:** 51.69%

---

## Recommendations

### For High Quality (SSIM ≥ 0.98)

**Recommended:** `h2/s4` with `learn+grad_est` adaptive mode
- Achieves 0.9818 SSIM with 16.1% time savings

### For Balanced Quality/Speed (SSIM ≥ 0.95)

**Recommended:** `h2/s3` with `learning` adaptive mode
- Achieves 0.9533 SSIM with 21.6% time savings

### General Observations

- Skip modes with lower history (h2) tend to be more conservative but stable
- Higher history modes (h3, h4) can achieve better compression but may be less stable
- Adaptive modes with learning stabilizer generally improve quality
- Time savings correlate strongly with NFE reduction

---

*End of Report*
