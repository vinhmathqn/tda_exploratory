# Representative Market-State Stock Selection

Replication package for the manuscript:

**Representative Market-State Stock Selection: An Exploratory Framework Using PCA-KMeans and Topology-Inspired Benchmarks**

This repository is prepared for public upload to GitHub. It contains the manuscript source, the compiled PDF, the notebooks used for Step 4 / Step 5 / Step 5B, the recovered main fixed-universe returns matrix used for supplementary diagnostics, diagnostic CSV files, and a reference requirements file.

## Important reproducibility note

The experiments use public/yfinance-derived adjusted prices. yfinance is a live data source and adjusted prices may be revised retroactively. For exact reproduction of the supplementary diagnostics, use the saved returns matrix and CSV artifacts included here rather than relying only on live re-downloads.

## Repository structure

```text
manuscript/
  draft_9.tex
  draft_9.pdf
  figures/
    nav_comparison_2023_regime_sensitivity.png
supplement/
  supplementary_diagnostics.tex
  supplementary_diagnostics.pdf
code/
  step_4_code.ipynb
  step_4_exp2_code.ipynb
  step_4_exp3_code.ipynb
  step_5_code.ipynb
  step_5B_code.ipynb
data/
  main_fixed_universe_returns_matrix.csv
diagnostics/
  k_ablation_exact.csv
  walk_forward_holdout_exact.csv
  hold_orig.csv
  hold_selected.csv
  k1.csv ... k5.csv
metadata/
  checksums.csv
requirements_reference.txt
```

## How to reproduce the supplementary diagnostics

1. Create a Python environment using `requirements_reference.txt`.
2. Use the saved return matrix in `data/main_fixed_universe_returns_matrix.csv` for exact supplementary diagnostic reproduction.
3. The diagnostic outputs are stored in `diagnostics/`.
4. The manuscript states which results are saved Step 4/5/5B artifacts and which are supplementary diagnostics based on the recovered return matrix.

## GitHub upload steps

```bash
git init
git add .
git commit -m "Initial replication package"
git branch -M main
git remote add origin https://github.com/<YOUR_ACCOUNT>/<YOUR_REPO>.git
git push -u origin main
```

After uploading, replace the manuscript Data and Code Availability text with the public repository URL.

## Citation

Please cite the accompanying manuscript if using this package.
