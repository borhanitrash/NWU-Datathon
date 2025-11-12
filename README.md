# NWU CSE Fest 2025 Datathon — 1st Place Solution

**Private Score:** 0.93310 • **Public Score:** 0.94464

## Overview

This repository contains the 1st-place solution for the **North Western University (Khulna) Datathon (CSE Fest 2025)**. The goal was to predict fraudulent transactions (`fraud` column) using large-scale transactional data. The solution achieved top performance on both public and private leaderboards.

## File

* **nwu-datathon.ipynb** — A complete, single Jupyter Notebook containing all steps: data loading, feature engineering, model training, threshold optimization, and final submission generation.

## Key Details

* **Competition Metric:** Cohen’s Kappa (binary classification)
* **Algorithm:** LightGBM (GBDT) with 5-fold Stratified K-Fold CV
* **Frameworks:** pandas, numpy, scikit-learn, lightgbm
* **Feature Strategy:** Extensive temporal, behavioral, and aggregated transaction features

## Highlights

* Comprehensive **feature engineering pipeline** for client, merchant, and transaction-level insights.
* **Memory optimization** for handling extremely large datasets.
* **Threshold tuning** for maximizing Cohen’s Kappa instead of relying on default 0.5.
* Balanced training using computed **scale_pos_weight** to manage class imbalance.

## Usage

1. Upload `nwu-datathon.ipynb` to your Kaggle Notebook environment.
2. Add the official dataset under `/kaggle/input/nwu-data/NWU_CSE_FEST_2025_DATATHON_COMPETITION/`.
3. Run all cells to reproduce the leaderboard submission.

Output file:

```
submission.csv
```

containing `transaction_id` and `fraud` predictions (`Yes` / `No`).

## Results

* **Public Leaderboard:** 0.94464
* **Private Leaderboard:** 0.93310

## Author

**Md. Abdur Rahman**
1st Place Winner — NWU Datathon 2025
