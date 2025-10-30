# Curated Summary (Visual-First)

SSIM values are often so high that changes from baseline can be hard to discern; readers should inspect the full-size images alongside the small panel. The per-configuration images are the primary evidence.

Shown configs: Baseline, h2/s2+learning, h2/s3+learning, h3/s3+learning, adaptive+learning (or nearest available if exact combination is missing).

Generality note: Community testers report FSampler also works on Chroma, SDXL, and other models. While not reproduced here, the method applies to any diffusion pipeline exposing latents x, noise scale σ, and epsilon predictions.

| Config | Adaptive | NFE | Time Saved % | SSIM | Image |
|---|---:|---:|---:|---:|---|
| Baseline | - | 26 | 0.0 |  | G:\ComfyUI\output\experiments\wan221\2025-10-19_07-17-20_1760854640_wan22-high-noise+wan22-high-noise_baseline\output_image.png |
| h2/s2 | learning | 20 | 29.1 | 0.9136 | G:\ComfyUI\output\experiments\wan221\2025-10-19_07-23-49_1760855029_wan22-high-noise+wan22-high-noise\output_image.png |
| h2/s3 | learning | 21 | 22.5 | 0.8957 | G:\ComfyUI\output\experiments\wan221\2025-10-19_07-27-04_1760855224_wan22-high-noise+wan22-high-noise\output_image.png |
| h3/s3 | learning | 23 | 13.3 | 0.9399 | G:\ComfyUI\output\experiments\wan221\2025-10-19_07-38-15_1760855895_wan22-high-noise+wan22-high-noise\output_image.png |
| adaptive | learning | 17 | 35.9 | 0.8396 | G:\ComfyUI\output\experiments\wan221\2025-10-19_07-55-47_1760856947_wan22-high-noise+wan22-high-noise\output_image.png |

Figures generated:
- image_grid_SMALL.png (paper-sized strip)
- image_grid_FULL.png (full-resolution strip)
- crops_grid.png (fixed ROIs per config)
- quality_vs_efficiency_curated.png (curated trade-off)