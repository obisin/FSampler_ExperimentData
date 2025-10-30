# FSampler Experiment Analysis Report

**Generated:** 2025-10-22 15:00:30

**Total Experiments:** 32

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

This report analyzes **32 experiments** comparing baseline sampling with FSampler acceleration.

- **Baseline runs:** 1
- **FSampler runs:** 31
- **Average time saved:** 15.5% (33.04s)
- **Average NFE reduction:** 14.1%

- **Average SSIM:** 0.9290
- **Min SSIM:** 0.8396
- **Max SSIM:** 0.9710

---

## Baseline Performance

**Reference measurements without FSampler optimization**

- **Average Runtime:** 213.59s
- **Average NFE (Model Calls):** 26.0

### Baseline Experiments Detail

| Sampler   | Scheduler         |   Steps |   NFE |   Time (s) |   SSIM |   RMSE |   MAE |
|:----------|:------------------|--------:|------:|-----------:|-------:|-------:|------:|
| res_2s    | beta+bong_tangent |      26 |    26 |   213.5873 |    nan |    nan |   nan |


---

## FSampler Performance

- **Average Runtime:** 180.55s
- **Average NFE:** 22.3
- **Average NFE Reduction:** 14.14%
- **Average Time Saved:** 15.47%
- **Average Time Saved (seconds):** 33.04s

**Quality Metrics (vs Baseline):**
- **Average SSIM:** 0.9290
- **Min SSIM:** 0.8396
- **Max SSIM:** 0.9710
- **Average RMSE:** 0.0482
- **Average MAE:** 0.0220


---

## All Experiments Table

Complete data for all experiments:

| Sampler   | Scheduler         | Skip Mode   | Adaptive       |   Anchor Interval |   Max Consec Skips |   Steps |   NFE |   Skipped |   NFE Red % |   Time (s) |   Time Saved % |     SSIM |     RMSE |      MAE |
|:----------|:------------------|:------------|:---------------|------------------:|-------------------:|--------:|------:|----------:|------------:|-----------:|---------------:|---------:|---------:|---------:|
| res_2s    | beta+bong_tangent | none        | none           |          nan      |           nan      |      26 |    26 |         0 |      0.0000 |   213.5873 |         0.0000 | nan      | nan      | nan      |
| res_2s    | beta+bong_tangent | h2/s2       | learning       |            4.0000 |             2.0000 |      26 |    20 |         6 |     23.0769 |   151.3382 |        29.1446 |   0.9136 |   0.0599 |   0.0278 |
| res_2s    | beta+bong_tangent | h2/s3       | learning       |            4.0000 |             2.0000 |      26 |    21 |         5 |     19.2308 |   165.6342 |        22.4513 |   0.8957 |   0.0809 |   0.0370 |
| res_2s    | beta+bong_tangent | h2/s4       | learning       |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   183.6157 |        14.0325 |   0.9503 |   0.0374 |   0.0154 |
| res_2s    | beta+bong_tangent | h2/s5       | learning       |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   202.3176 |         5.2764 |   0.9632 |   0.0342 |   0.0136 |
| res_2s    | beta+bong_tangent | h3/s3       | learning       |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   185.2332 |        13.2752 |   0.9399 |   0.0419 |   0.0194 |
| res_2s    | beta+bong_tangent | h3/s4       | learning       |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   183.6755 |        14.0045 |   0.9500 |   0.0395 |   0.0164 |
| res_2s    | beta+bong_tangent | h3/s5       | learning       |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   193.0614 |         9.6101 |   0.9710 |   0.0262 |   0.0121 |
| res_2s    | beta+bong_tangent | h4/s4       | learning       |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   195.9338 |         8.2652 |   0.9276 |   0.0431 |   0.0202 |
| res_2s    | beta+bong_tangent | h4/s5       | learning       |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   197.5518 |         7.5077 |   0.9323 |   0.0380 |   0.0186 |
| res_2s    | beta+bong_tangent | adaptive    | learning       |            4.0000 |             2.0000 |      26 |    17 |         9 |     34.6154 |   136.8426 |        35.9313 |   0.8396 |   0.0850 |   0.0418 |
| res_2s    | beta+bong_tangent | h2/s4       | learning       |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   194.9568 |         8.7227 |   0.9503 |   0.0374 |   0.0154 |
| res_2s    | beta+bong_tangent | h2/s2       | grad_est       |            4.0000 |             2.0000 |      26 |    20 |         6 |     23.0769 |   156.3947 |        26.7772 |   0.9136 |   0.0599 |   0.0278 |
| res_2s    | beta+bong_tangent | h2/s3       | grad_est       |            4.0000 |             2.0000 |      26 |    21 |         5 |     19.2308 |   170.5959 |        20.1282 |   0.8957 |   0.0809 |   0.0370 |
| res_2s    | beta+bong_tangent | h2/s4       | grad_est       |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   183.3042 |        14.1783 |   0.9503 |   0.0374 |   0.0154 |
| res_2s    | beta+bong_tangent | h2/s5       | grad_est       |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   190.9561 |        10.5957 |   0.9632 |   0.0342 |   0.0136 |
| res_2s    | beta+bong_tangent | h3/s3       | grad_est       |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   195.3758 |         8.5265 |   0.9399 |   0.0419 |   0.0194 |
| res_2s    | beta+bong_tangent | h3/s4       | grad_est       |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   186.5859 |        12.6419 |   0.9500 |   0.0395 |   0.0164 |
| res_2s    | beta+bong_tangent | h3/s5       | grad_est       |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   194.3353 |         9.0136 |   0.9710 |   0.0262 |   0.0121 |
| res_2s    | beta+bong_tangent | h4/s4       | grad_est       |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   199.5385 |         6.5775 |   0.9276 |   0.0431 |   0.0202 |
| res_2s    | beta+bong_tangent | h4/s5       | grad_est       |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   203.2261 |         4.8510 |   0.9323 |   0.0380 |   0.0186 |
| res_2s    | beta+bong_tangent | adaptive    | grad_est       |            4.0000 |             2.0000 |      26 |    17 |         9 |     34.6154 |   135.8502 |        36.3959 |   0.8396 |   0.0850 |   0.0418 |
| res_2s    | beta+bong_tangent | h2/s2       | learn+grad_est |            4.0000 |             2.0000 |      26 |    20 |         6 |     23.0769 |   154.6240 |        27.6062 |   0.9136 |   0.0599 |   0.0278 |
| res_2s    | beta+bong_tangent | h2/s3       | learn+grad_est |            4.0000 |             2.0000 |      26 |    21 |         5 |     19.2308 |   163.3016 |        23.5434 |   0.8957 |   0.0809 |   0.0370 |
| res_2s    | beta+bong_tangent | h2/s4       | learn+grad_est |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   188.3802 |        11.8018 |   0.9503 |   0.0374 |   0.0154 |
| res_2s    | beta+bong_tangent | h2/s5       | learn+grad_est |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   193.7185 |         9.3024 |   0.9632 |   0.0342 |   0.0136 |
| res_2s    | beta+bong_tangent | h3/s3       | learn+grad_est |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   180.0327 |        15.7100 |   0.9399 |   0.0419 |   0.0194 |
| res_2s    | beta+bong_tangent | h3/s4       | learn+grad_est |            4.0000 |             2.0000 |      26 |    23 |         3 |     11.5385 |   188.0624 |        11.9506 |   0.9500 |   0.0395 |   0.0164 |
| res_2s    | beta+bong_tangent | h3/s5       | learn+grad_est |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   197.3092 |         7.6213 |   0.9710 |   0.0262 |   0.0121 |
| res_2s    | beta+bong_tangent | h4/s4       | learn+grad_est |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   196.4558 |         8.0208 |   0.9276 |   0.0431 |   0.0202 |
| res_2s    | beta+bong_tangent | h4/s5       | learn+grad_est |            4.0000 |             2.0000 |      26 |    24 |         2 |      7.6923 |   193.1892 |         9.5502 |   0.9323 |   0.0380 |   0.0186 |
| res_2s    | beta+bong_tangent | adaptive    | learn+grad_est |            4.0000 |             2.0000 |      26 |    17 |         9 |     34.6154 |   135.6778 |        36.4766 |   0.8396 |   0.0850 |   0.0418 |

---

## Configuration Performance Comparison

Individual performance of each skip mode × adaptive mode configuration.

Each row represents a separate experimental run compared to baseline.


### All FSampler Configurations

| Skip Mode   | Adaptive Mode   |   Anchor Int |   Max Consec |   SSIM |   NFE Red % |     NFE |   Time (s) |   Skipped |   Time Saved % |   RMSE |    MAE |
|:------------|:----------------|-------------:|-------------:|-------:|------------:|--------:|-----------:|----------:|---------------:|-------:|-------:|
| adaptive    | grad_est        |       4.0000 |       2.0000 | 0.8396 |     34.6154 | 17.0000 |   135.8502 |    9.0000 |        36.3959 | 0.0850 | 0.0418 |
| adaptive    | learn+grad_est  |       4.0000 |       2.0000 | 0.8396 |     34.6154 | 17.0000 |   135.6778 |    9.0000 |        36.4766 | 0.0850 | 0.0418 |
| adaptive    | learning        |       4.0000 |       2.0000 | 0.8396 |     34.6154 | 17.0000 |   136.8426 |    9.0000 |        35.9313 | 0.0850 | 0.0418 |
| h2/s2       | grad_est        |       4.0000 |       2.0000 | 0.9136 |     23.0769 | 20.0000 |   156.3947 |    6.0000 |        26.7772 | 0.0599 | 0.0278 |
| h2/s2       | learn+grad_est  |       4.0000 |       2.0000 | 0.9136 |     23.0769 | 20.0000 |   154.6240 |    6.0000 |        27.6062 | 0.0599 | 0.0278 |
| h2/s2       | learning        |       4.0000 |       2.0000 | 0.9136 |     23.0769 | 20.0000 |   151.3382 |    6.0000 |        29.1446 | 0.0599 | 0.0278 |
| h2/s3       | grad_est        |       4.0000 |       2.0000 | 0.8957 |     19.2308 | 21.0000 |   170.5959 |    5.0000 |        20.1282 | 0.0809 | 0.0370 |
| h2/s3       | learn+grad_est  |       4.0000 |       2.0000 | 0.8957 |     19.2308 | 21.0000 |   163.3016 |    5.0000 |        23.5434 | 0.0809 | 0.0370 |
| h2/s3       | learning        |       4.0000 |       2.0000 | 0.8957 |     19.2308 | 21.0000 |   165.6342 |    5.0000 |        22.4513 | 0.0809 | 0.0370 |
| h2/s4       | grad_est        |       4.0000 |       2.0000 | 0.9503 |     11.5385 | 23.0000 |   183.3042 |    3.0000 |        14.1783 | 0.0374 | 0.0154 |
| h2/s4       | learn+grad_est  |       4.0000 |       2.0000 | 0.9503 |     11.5385 | 23.0000 |   188.3802 |    3.0000 |        11.8018 | 0.0374 | 0.0154 |
| h2/s4       | learning        |       4.0000 |       2.0000 | 0.9503 |     11.5385 | 23.0000 |   189.2862 |    3.0000 |        11.3776 | 0.0374 | 0.0154 |
| h2/s5       | grad_est        |       4.0000 |       2.0000 | 0.9632 |      7.6923 | 24.0000 |   190.9561 |    2.0000 |        10.5957 | 0.0342 | 0.0136 |
| h2/s5       | learn+grad_est  |       4.0000 |       2.0000 | 0.9632 |      7.6923 | 24.0000 |   193.7185 |    2.0000 |         9.3024 | 0.0342 | 0.0136 |
| h2/s5       | learning        |       4.0000 |       2.0000 | 0.9632 |      7.6923 | 24.0000 |   202.3176 |    2.0000 |         5.2764 | 0.0342 | 0.0136 |
| h3/s3       | grad_est        |       4.0000 |       2.0000 | 0.9399 |     11.5385 | 23.0000 |   195.3758 |    3.0000 |         8.5265 | 0.0419 | 0.0194 |
| h3/s3       | learn+grad_est  |       4.0000 |       2.0000 | 0.9399 |     11.5385 | 23.0000 |   180.0327 |    3.0000 |        15.7100 | 0.0419 | 0.0194 |
| h3/s3       | learning        |       4.0000 |       2.0000 | 0.9399 |     11.5385 | 23.0000 |   185.2332 |    3.0000 |        13.2752 | 0.0419 | 0.0194 |
| h3/s4       | grad_est        |       4.0000 |       2.0000 | 0.9500 |     11.5385 | 23.0000 |   186.5859 |    3.0000 |        12.6419 | 0.0395 | 0.0164 |
| h3/s4       | learn+grad_est  |       4.0000 |       2.0000 | 0.9500 |     11.5385 | 23.0000 |   188.0624 |    3.0000 |        11.9506 | 0.0395 | 0.0164 |
| h3/s4       | learning        |       4.0000 |       2.0000 | 0.9500 |     11.5385 | 23.0000 |   183.6755 |    3.0000 |        14.0045 | 0.0395 | 0.0164 |
| h3/s5       | grad_est        |       4.0000 |       2.0000 | 0.9710 |      7.6923 | 24.0000 |   194.3353 |    2.0000 |         9.0136 | 0.0262 | 0.0121 |
| h3/s5       | learn+grad_est  |       4.0000 |       2.0000 | 0.9710 |      7.6923 | 24.0000 |   197.3092 |    2.0000 |         7.6213 | 0.0262 | 0.0121 |
| h3/s5       | learning        |       4.0000 |       2.0000 | 0.9710 |      7.6923 | 24.0000 |   193.0614 |    2.0000 |         9.6101 | 0.0262 | 0.0121 |
| h4/s4       | grad_est        |       4.0000 |       2.0000 | 0.9276 |      7.6923 | 24.0000 |   199.5385 |    2.0000 |         6.5775 | 0.0431 | 0.0202 |
| h4/s4       | learn+grad_est  |       4.0000 |       2.0000 | 0.9276 |      7.6923 | 24.0000 |   196.4558 |    2.0000 |         8.0208 | 0.0431 | 0.0202 |
| h4/s4       | learning        |       4.0000 |       2.0000 | 0.9276 |      7.6923 | 24.0000 |   195.9338 |    2.0000 |         8.2652 | 0.0431 | 0.0202 |
| h4/s5       | grad_est        |       4.0000 |       2.0000 | 0.9323 |      7.6923 | 24.0000 |   203.2261 |    2.0000 |         4.8510 | 0.0380 | 0.0186 |
| h4/s5       | learn+grad_est  |       4.0000 |       2.0000 | 0.9323 |      7.6923 | 24.0000 |   193.1892 |    2.0000 |         9.5502 | 0.0380 | 0.0186 |
| h4/s5       | learning        |       4.0000 |       2.0000 | 0.9323 |      7.6923 | 24.0000 |   197.5518 |    2.0000 |         7.5077 | 0.0380 | 0.0186 |



**Baseline Reference:** SSIM = 1.0000 (by definition), 
NFE = 26.0, 
Time = 213.59s

---

## Best Configurations

### Best Quality (Highest SSIM)

- **Skip Mode:** h3/s5
- **Adaptive Mode:** learning
- **Sampler:** res_2s
- **SSIM:** 0.9710
- **Runtime:** 193.06s
- **Time Saved:** 9.6%
- **NFE:** 24
- **NFE Reduction:** 7.7%

### Best Time Savings (SSIM ≥ 0.95)

- **Skip Mode:** h2/s4
- **Adaptive Mode:** grad_est
- **Sampler:** res_2s
- **SSIM:** 0.9503
- **Runtime:** 183.30s
- **Time Saved:** 14.2%
- **NFE:** 23
- **NFE Reduction:** 11.5%

---

## Statistical Analysis

### Configuration Summary

- **Samplers tested:** res_2s
- **Schedulers tested:** beta+bong_tangent
- **Skip modes tested:** adaptive, h2/s2, h2/s3, h2/s4, h2/s5, h3/s3, h3/s4, h3/s5, h4/s4, h4/s5, none
- **Adaptive modes tested:** grad_est, learn+grad_est, learning, none
- **Model types tested:** wan22-high-noise+wan22-high-noise

### Quality Distribution

- **Mean SSIM:** 0.9290
- **Median SSIM:** 0.9399
- **Std Dev SSIM:** 0.0367
- **Min SSIM:** 0.8396
- **Max SSIM:** 0.9710

### Efficiency Distribution

- **Mean NFE Reduction:** 13.70%
- **Median NFE Reduction:** 11.54%
- **Max NFE Reduction:** 34.62%

- **Mean Time Saved:** 14.98%
- **Median Time Saved:** 11.88%
- **Max Time Saved:** 36.48%

---

## Recommendations

### For Balanced Quality/Speed (SSIM ≥ 0.95)

**Recommended:** `h2/s4` with `grad_est` adaptive mode
- Achieves 0.9503 SSIM with 14.2% time savings

### General Observations

- Skip modes with lower history (h2) tend to be more conservative but stable
- Higher history modes (h3, h4) can achieve better compression but may be less stable
- Adaptive modes with learning stabilizer generally improve quality
- Time savings correlate strongly with NFE reduction

---

*End of Report*
