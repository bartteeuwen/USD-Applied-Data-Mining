# Applied Data Mining – Final Team Project

This repository showcases a **complete, end-to-end data science project** completed as part of a graduate-level course. The project demonstrates practical experience turning clinical-trial data into actionable insights with R.

The work emphasizes **real-world data handling, analytical reasoning, and clear communication**, not just model building.

---

## Project Objective

A biotech sponsor (Triamex) asked: **can we predict which patients will respond to a new mRNA-2206 lung-cancer protocol?**  
The assignment goals were to:

- Understand outcome drivers from trial data  
- Build and compare supervised models for **Responder vs NonResponder**  
- Evaluate fairly with cross-validation and a held-out test set  
- Translate results into next-step guidance for Phase II/III decisions

---

## What This Repository Contains

- A **fully documented R notebook** covering:  
  - Data cleaning & preprocessing (imputation, scaling, one-hot, SMOTE)  
  - Exploratory analysis & visualization  
  - Model training/tuning (GLMnet, Random Forest, SVM-RBF, XGBoost)  
  - Test-set evaluation (ROC-AUC primary; Accuracy, Kappa secondary) 

- Exported **figures & tables**: combined ROC, box/dot plots of AUC across folds, tuning summaries, variable importance. 

---

## Dataset Overview

Cleaned modeling table (~1,000 rows) with numeric and categorical predictors:

- Numeric: `age`, `immune_response_score`, `biomarker_A`, `biomarker_B`, `tumor_volume_change`  
- Categorical: `trial_arm` (Drug 1–3, Placebo), `side_effect`  
- Target: `treatment_outcome` recoded to two levels (≈ 56% NonResponder / 44% Responder)

EDA highlights:

- Drug 3 shows the highest responder proportion; Placebo the lowest  
- Mostly symmetric numeric distributions; weak pairwise correlations  
- Up to ~5% missing in a few features; outliers modest and capped during prep

---

## Key Takeaways

- **Signal exists but is modest.** Cross-validated AUCs cluster around **0.65–0.68**; Kappa ≈ **0.20**. 
- **Best single test AUC**: SVM-RBF (~0.676). **Top accuracy**: SVM/RF (~0.62).
- **Recommended baseline**: **XGBoost** for stability (tight ROC distribution, narrower CI) and tunability, despite a slightly lower mean AUC. Prioritize calibration and thresholding for decisions.
- **Next steps**: expand features (genomics/longitudinal), larger N, consider survival & causal analyses; pilot model in Phase II for calibration.

