# Experiments Directory

This directory contains experimental results and analysis for various diffusion models.

## Structure

Each model has its own subdirectory containing:
- Individual experiment runs (timestamped folders)
- `_analysis/` folder with comprehensive analysis in high resolution

## Available Models

### FLUX.1-dev (`fluxr1/`)
High-resolution analysis files including:
- Family sweep graphs (SSIM vs NFE, SSIM vs Time Saved)
- Ablation heatmaps (skip mode, adaptive mode)
- Baseline comparisons
- Adaptive mode analysis
- Configuration tables and reports

**Link to FLUX analysis**: [[link](https://github.com/obisin/FSampler_ExperimentData/tree/main/experiments/flux/)]

### Qwen-Image (`qwen1/`)
High-resolution analysis files including:
- Family sweep graphs
- Ablation heatmaps
- Baseline comparisons
- Performance metrics
- Configuration analysis

**Link to Qwen analysis**: [[link](https://github.com/obisin/FSampler_ExperimentData/tree/main/experiments/qwen/)]

### WAN2.2 (`wan221/`)
High-resolution analysis files including:
- Family sweep graphs
- Ablation heatmaps
- Baseline comparisons
- High-noise configuration results
- Performance metrics

**Link to WAN2.2 analysis**: [[link](https://github.com/obisin/FSampler_ExperimentData/tree/main/experiments/wan2.2/_analysis)]

## Analysis Files

Within each `_analysis/` folder, you'll find:

- **PDF files**: High-resolution vector graphics suitable for publication
- **PNG files**: High-resolution raster images for quick viewing
- **CSV files**: Raw experimental data
- **TEX files**: LaTeX tables for inclusion in papers
- **ANALYSIS_REPORT.md**: Comprehensive analysis report with all findings

All graphs and visualizations are available in both PDF (vector) and PNG (raster) formats for maximum compatibility with different use cases.
