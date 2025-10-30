# FSampler Experiment Analysis Report

**Generated:** 2025-10-22 15:00:16

**Total Experiments:** 31

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

This report analyzes **31 experiments** comparing baseline sampling with FSampler acceleration.

- **Baseline runs:** 1
- **FSampler runs:** 30
- **Average time saved:** 14.4% (20.87s)
- **Average NFE reduction:** 9.8%

- **Average SSIM:** 0.9323
- **Min SSIM:** 0.7164
- **Max SSIM:** 0.9952

---

## Baseline Performance

**Reference measurements without FSampler optimization**

- **Average Runtime:** 145.39s
- **Average NFE (Model Calls):** 25.0

### Baseline Experiments Detail

| Sampler   | Scheduler   |   Steps |   NFE |   Time (s) |   SSIM |   RMSE |   MAE |
|:----------|:------------|--------:|------:|-----------:|-------:|-------:|------:|
| euler     | simple      |      50 |    25 |   145.3910 |    nan |    nan |   nan |


---

## FSampler Performance

- **Average Runtime:** 124.52s
- **Average NFE:** 20.1
- **Average NFE Reduction:** 9.80%
- **Average Time Saved:** 14.35%
- **Average Time Saved (seconds):** 20.87s

**Quality Metrics (vs Baseline):**
- **Average SSIM:** 0.9323
- **Min SSIM:** 0.7164
- **Max SSIM:** 0.9952
- **Average RMSE:** 0.0467
- **Average MAE:** 0.0243


---

## All Experiments Table

Complete data for all experiments:

| Sampler   | Scheduler   | Skip Mode   | Adaptive       |   Anchor Interval |   Max Consec Skips |   Steps |   NFE |   Skipped |   NFE Red % |   Time (s) |   Time Saved % |     SSIM |     RMSE |      MAE |
|:----------|:------------|:------------|:---------------|------------------:|-------------------:|--------:|------:|----------:|------------:|-----------:|---------------:|---------:|---------:|---------:|
| euler     | simple      | none        | none           |          nan      |           nan      |      50 |    25 |         0 |      0.0000 |   145.3910 |         0.0000 | nan      | nan      | nan      |
| euler     | simple      | h2/s2       | learning       |            4.0000 |             2.0000 |      50 |    18 |         7 |     14.0000 |   105.9800 |        27.1069 |   0.9550 |   0.0505 |   0.0197 |
| euler     | simple      | h2/s3       | learning       |            4.0000 |             2.0000 |      50 |    20 |         5 |     10.0000 |   116.3949 |        19.9435 |   0.9733 |   0.0247 |   0.0122 |
| euler     | simple      | h2/s4       | learning       |            4.0000 |             2.0000 |      50 |    21 |         4 |      8.0000 |   125.3823 |        13.7620 |   0.9696 |   0.0283 |   0.0124 |
| euler     | simple      | h2/s5       | learning       |            4.0000 |             2.0000 |      50 |    22 |         3 |      6.0000 |   133.5946 |         8.1136 |   0.9952 |   0.0105 |   0.0053 |
| euler     | simple      | h3/s3       | learning       |            4.0000 |             2.0000 |      50 |    20 |         5 |     10.0000 |   123.1772 |        15.2787 |   0.9645 |   0.0316 |   0.0146 |
| euler     | simple      | h3/s4       | learning       |            4.0000 |             2.0000 |      50 |    21 |         4 |      8.0000 |   128.4854 |        11.6277 |   0.9780 |   0.0369 |   0.0116 |
| euler     | simple      | h3/s5       | learning       |            4.0000 |             2.0000 |      50 |    22 |         3 |      6.0000 |   134.7786 |         7.2992 |   0.9732 |   0.0270 |   0.0113 |
| euler     | simple      | h4/s4       | learning       |            4.0000 |             2.0000 |      50 |    21 |         4 |      8.0000 |   131.2444 |         9.7300 |   0.9512 |   0.0374 |   0.0179 |
| euler     | simple      | h4/s5       | learning       |            4.0000 |             2.0000 |      50 |    22 |         3 |      6.0000 |   138.0739 |         5.0327 |   0.9784 |   0.0254 |   0.0115 |
| euler     | simple      | adaptive    | learning       |            4.0000 |             2.0000 |      50 |    14 |        11 |     22.0000 |    87.8411 |        39.5829 |   0.8317 |   0.0839 |   0.0534 |
| euler     | simple      | h2/s2       | grad_est       |            4.0000 |             2.0000 |      50 |    18 |         7 |     14.0000 |   113.2465 |        22.1090 |   0.9161 |   0.0618 |   0.0332 |
| euler     | simple      | h2/s3       | grad_est       |            4.0000 |             2.0000 |      50 |    20 |         5 |     10.0000 |   126.0276 |        13.3182 |   0.9146 |   0.0492 |   0.0255 |
| euler     | simple      | h2/s4       | grad_est       |            4.0000 |             2.0000 |      50 |    21 |         4 |      8.0000 |   131.7034 |         9.4143 |   0.9599 |   0.0348 |   0.0158 |
| euler     | simple      | h2/s5       | grad_est       |            4.0000 |             2.0000 |      50 |    22 |         3 |      6.0000 |   138.5974 |         4.6727 |   0.9822 |   0.0333 |   0.0103 |
| euler     | simple      | h3/s3       | grad_est       |            4.0000 |             2.0000 |      50 |    20 |         5 |     10.0000 |   124.7998 |        14.1626 |   0.9410 |   0.0492 |   0.0226 |
| euler     | simple      | h3/s4       | grad_est       |            4.0000 |             2.0000 |      50 |    21 |         4 |      8.0000 |   131.6283 |         9.4660 |   0.9634 |   0.0429 |   0.0176 |
| euler     | simple      | h3/s5       | grad_est       |            4.0000 |             2.0000 |      50 |    22 |         3 |      6.0000 |   136.7635 |         5.9340 |   0.9566 |   0.0368 |   0.0167 |
| euler     | simple      | h4/s4       | grad_est       |            4.0000 |             2.0000 |      50 |    21 |         4 |      8.0000 |   131.9232 |         9.2632 |   0.8934 |   0.0607 |   0.0321 |
| euler     | simple      | h4/s5       | grad_est       |            4.0000 |             2.0000 |      50 |    22 |         3 |      6.0000 |   136.7137 |         5.9682 |   0.9550 |   0.0391 |   0.0199 |
| euler     | simple      | adaptive    | grad_est       |            4.0000 |             2.0000 |      50 |    14 |        11 |     22.0000 |    86.3358 |        40.6182 |   0.7185 |   0.1147 |   0.0856 |
| euler     | simple      | h2/s2       | learn+grad_est |            4.0000 |             2.0000 |      50 |    18 |         7 |     14.0000 |   112.8889 |        22.3549 |   0.9159 |   0.0619 |   0.0335 |
| euler     | simple      | h2/s3       | learn+grad_est |            4.0000 |             2.0000 |      50 |    20 |         5 |     10.0000 |   124.7292 |        14.2112 |   0.9154 |   0.0490 |   0.0257 |
| euler     | simple      | h2/s4       | learn+grad_est |            4.0000 |             2.0000 |      50 |    21 |         4 |      8.0000 |   131.4979 |         9.5557 |   0.9598 |   0.0348 |   0.0160 |
| euler     | simple      | h2/s5       | learn+grad_est |            4.0000 |             2.0000 |      50 |    22 |         3 |      6.0000 |   139.7305 |         3.8933 |   0.9822 |   0.0334 |   0.0104 |
| euler     | simple      | h3/s3       | learn+grad_est |            4.0000 |             2.0000 |      50 |    20 |         5 |     10.0000 |   126.0125 |        13.3285 |   0.9415 |   0.0492 |   0.0227 |
| euler     | simple      | h3/s4       | learn+grad_est |            4.0000 |             2.0000 |      50 |    21 |         4 |      8.0000 |   131.3783 |         9.6380 |   0.9631 |   0.0431 |   0.0177 |
| euler     | simple      | h3/s5       | learn+grad_est |            4.0000 |             2.0000 |      50 |    22 |         3 |      6.0000 |   135.1065 |         7.0737 |   0.9565 |   0.0368 |   0.0168 |
| euler     | simple      | h4/s4       | learn+grad_est |            4.0000 |             2.0000 |      50 |    21 |         4 |      8.0000 |   128.6026 |        11.5471 |   0.8934 |   0.0607 |   0.0322 |
| euler     | simple      | h4/s5       | learn+grad_est |            4.0000 |             2.0000 |      50 |    22 |         3 |      6.0000 |   136.1079 |         6.3850 |   0.9550 |   0.0392 |   0.0200 |
| euler     | simple      | adaptive    | learn+grad_est |            4.0000 |             2.0000 |      50 |    14 |        11 |     22.0000 |    86.9112 |        40.2225 |   0.7164 |   0.1156 |   0.0862 |

---

## Configuration Performance Comparison

Individual performance of each skip mode × adaptive mode configuration.

Each row represents a separate experimental run compared to baseline.


### All FSampler Configurations

| Skip Mode   | Adaptive Mode   |   Anchor Int |   Max Consec |   SSIM |   NFE Red % |     NFE |   Time (s) |   Skipped |   Time Saved % |   RMSE |    MAE |
|:------------|:----------------|-------------:|-------------:|-------:|------------:|--------:|-----------:|----------:|---------------:|-------:|-------:|
| adaptive    | grad_est        |       4.0000 |       2.0000 | 0.7185 |     22.0000 | 14.0000 |    86.3358 |   11.0000 |        40.6182 | 0.1147 | 0.0856 |
| adaptive    | learn+grad_est  |       4.0000 |       2.0000 | 0.7164 |     22.0000 | 14.0000 |    86.9112 |   11.0000 |        40.2225 | 0.1156 | 0.0862 |
| adaptive    | learning        |       4.0000 |       2.0000 | 0.8317 |     22.0000 | 14.0000 |    87.8411 |   11.0000 |        39.5829 | 0.0839 | 0.0534 |
| h2/s2       | grad_est        |       4.0000 |       2.0000 | 0.9161 |     14.0000 | 18.0000 |   113.2465 |    7.0000 |        22.1090 | 0.0618 | 0.0332 |
| h2/s2       | learn+grad_est  |       4.0000 |       2.0000 | 0.9159 |     14.0000 | 18.0000 |   112.8889 |    7.0000 |        22.3549 | 0.0619 | 0.0335 |
| h2/s2       | learning        |       4.0000 |       2.0000 | 0.9550 |     14.0000 | 18.0000 |   105.9800 |    7.0000 |        27.1069 | 0.0505 | 0.0197 |
| h2/s3       | grad_est        |       4.0000 |       2.0000 | 0.9146 |     10.0000 | 20.0000 |   126.0276 |    5.0000 |        13.3182 | 0.0492 | 0.0255 |
| h2/s3       | learn+grad_est  |       4.0000 |       2.0000 | 0.9154 |     10.0000 | 20.0000 |   124.7292 |    5.0000 |        14.2112 | 0.0490 | 0.0257 |
| h2/s3       | learning        |       4.0000 |       2.0000 | 0.9733 |     10.0000 | 20.0000 |   116.3949 |    5.0000 |        19.9435 | 0.0247 | 0.0122 |
| h2/s4       | grad_est        |       4.0000 |       2.0000 | 0.9599 |      8.0000 | 21.0000 |   131.7034 |    4.0000 |         9.4143 | 0.0348 | 0.0158 |
| h2/s4       | learn+grad_est  |       4.0000 |       2.0000 | 0.9598 |      8.0000 | 21.0000 |   131.4979 |    4.0000 |         9.5557 | 0.0348 | 0.0160 |
| h2/s4       | learning        |       4.0000 |       2.0000 | 0.9696 |      8.0000 | 21.0000 |   125.3823 |    4.0000 |        13.7620 | 0.0283 | 0.0124 |
| h2/s5       | grad_est        |       4.0000 |       2.0000 | 0.9822 |      6.0000 | 22.0000 |   138.5974 |    3.0000 |         4.6727 | 0.0333 | 0.0103 |
| h2/s5       | learn+grad_est  |       4.0000 |       2.0000 | 0.9822 |      6.0000 | 22.0000 |   139.7305 |    3.0000 |         3.8933 | 0.0334 | 0.0104 |
| h2/s5       | learning        |       4.0000 |       2.0000 | 0.9952 |      6.0000 | 22.0000 |   133.5946 |    3.0000 |         8.1136 | 0.0105 | 0.0053 |
| h3/s3       | grad_est        |       4.0000 |       2.0000 | 0.9410 |     10.0000 | 20.0000 |   124.7998 |    5.0000 |        14.1626 | 0.0492 | 0.0226 |
| h3/s3       | learn+grad_est  |       4.0000 |       2.0000 | 0.9415 |     10.0000 | 20.0000 |   126.0125 |    5.0000 |        13.3285 | 0.0492 | 0.0227 |
| h3/s3       | learning        |       4.0000 |       2.0000 | 0.9645 |     10.0000 | 20.0000 |   123.1772 |    5.0000 |        15.2787 | 0.0316 | 0.0146 |
| h3/s4       | grad_est        |       4.0000 |       2.0000 | 0.9634 |      8.0000 | 21.0000 |   131.6283 |    4.0000 |         9.4660 | 0.0429 | 0.0176 |
| h3/s4       | learn+grad_est  |       4.0000 |       2.0000 | 0.9631 |      8.0000 | 21.0000 |   131.3783 |    4.0000 |         9.6380 | 0.0431 | 0.0177 |
| h3/s4       | learning        |       4.0000 |       2.0000 | 0.9780 |      8.0000 | 21.0000 |   128.4854 |    4.0000 |        11.6277 | 0.0369 | 0.0116 |
| h3/s5       | grad_est        |       4.0000 |       2.0000 | 0.9566 |      6.0000 | 22.0000 |   136.7635 |    3.0000 |         5.9340 | 0.0368 | 0.0167 |
| h3/s5       | learn+grad_est  |       4.0000 |       2.0000 | 0.9565 |      6.0000 | 22.0000 |   135.1065 |    3.0000 |         7.0737 | 0.0368 | 0.0168 |
| h3/s5       | learning        |       4.0000 |       2.0000 | 0.9732 |      6.0000 | 22.0000 |   134.7786 |    3.0000 |         7.2992 | 0.0270 | 0.0113 |
| h4/s4       | grad_est        |       4.0000 |       2.0000 | 0.8934 |      8.0000 | 21.0000 |   131.9232 |    4.0000 |         9.2632 | 0.0607 | 0.0321 |
| h4/s4       | learn+grad_est  |       4.0000 |       2.0000 | 0.8934 |      8.0000 | 21.0000 |   128.6026 |    4.0000 |        11.5471 | 0.0607 | 0.0322 |
| h4/s4       | learning        |       4.0000 |       2.0000 | 0.9512 |      8.0000 | 21.0000 |   131.2444 |    4.0000 |         9.7300 | 0.0374 | 0.0179 |
| h4/s5       | grad_est        |       4.0000 |       2.0000 | 0.9550 |      6.0000 | 22.0000 |   136.7137 |    3.0000 |         5.9682 | 0.0391 | 0.0199 |
| h4/s5       | learn+grad_est  |       4.0000 |       2.0000 | 0.9550 |      6.0000 | 22.0000 |   136.1079 |    3.0000 |         6.3850 | 0.0392 | 0.0200 |
| h4/s5       | learning        |       4.0000 |       2.0000 | 0.9784 |      6.0000 | 22.0000 |   138.0739 |    3.0000 |         5.0327 | 0.0254 | 0.0115 |



**Baseline Reference:** SSIM = 1.0000 (by definition), 
NFE = 25.0, 
Time = 145.39s

---

## Best Configurations

### Best Quality (Highest SSIM)

- **Skip Mode:** h2/s5
- **Adaptive Mode:** learning
- **Sampler:** euler
- **SSIM:** 0.9952
- **Runtime:** 133.59s
- **Time Saved:** 8.1%
- **NFE:** 22
- **NFE Reduction:** 6.0%

### Best Time Savings (SSIM ≥ 0.95)

- **Skip Mode:** h2/s2
- **Adaptive Mode:** learning
- **Sampler:** euler
- **SSIM:** 0.9550
- **Runtime:** 105.98s
- **Time Saved:** 27.1%
- **NFE:** 18
- **NFE Reduction:** 14.0%

---

## Statistical Analysis

### Configuration Summary

- **Samplers tested:** euler
- **Schedulers tested:** simple
- **Skip modes tested:** adaptive, h2/s2, h2/s3, h2/s4, h2/s5, h3/s3, h3/s4, h3/s5, h4/s4, h4/s5, none
- **Adaptive modes tested:** grad_est, learn+grad_est, learning, none
- **Model types tested:** qwen-image

### Quality Distribution

- **Mean SSIM:** 0.9323
- **Median SSIM:** 0.9558
- **Std Dev SSIM:** 0.0675
- **Min SSIM:** 0.7164
- **Max SSIM:** 0.9952

### Efficiency Distribution

- **Mean NFE Reduction:** 9.48%
- **Median NFE Reduction:** 8.00%
- **Max NFE Reduction:** 22.00%

- **Mean Time Saved:** 13.89%
- **Median Time Saved:** 9.73%
- **Max Time Saved:** 40.62%

---

## Recommendations

### For High Quality (SSIM ≥ 0.98)

**Recommended:** `h2/s5` with `learning` adaptive mode
- Achieves 0.9952 SSIM with 8.1% time savings

### For Balanced Quality/Speed (SSIM ≥ 0.95)

**Recommended:** `h2/s2` with `learning` adaptive mode
- Achieves 0.9550 SSIM with 27.1% time savings

### General Observations

- Skip modes with lower history (h2) tend to be more conservative but stable
- Higher history modes (h3, h4) can achieve better compression but may be less stable
- Adaptive modes with learning stabilizer generally improve quality
- Time savings correlate strongly with NFE reduction

---

*End of Report*
