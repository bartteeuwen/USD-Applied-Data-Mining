# Applied Data Mining – Final Team Project

This repository showcases a **complete, end-to-end data science project** completed as part of a graduate-level Applied Data Science course. The project demonstrates practical experience transforming raw clinical trial data into actionable insights using R.

The work emphasizes **real-world data handling, analytical reasoning, and clear communication**, not just model building.

---

## Project Objective

A biotech company (Triamex Biotech) conducted a trial to evaluate their new lung cancer drug protocol, mRNA-2206. The primary goal was to determine what factors drive patient response to the treatment.

The goal of the assignment was to:
* Understand patient behavior and clinical outcomes from raw trial data
* Identify biological patterns linked to successful treatment "Responders"
* Apply appropriate statistical and machine learning techniques to assess drug efficacy
* Translate findings into strategic insights to inform FDA approval and Phase II trial planning

---

## What This Repository Contains

* **A fully documented R notebook** containing:
    * Data importing, cleaning, and preprocessing (median imputation and scaling).
    * Feature engineering and transformation (addressing class imbalance with SMOTE).
    * Exploratory data analysis and visualizations.
    * Statistical testing (ANOVA and Kruskal-Wallis) to identify significant predictors.
    * Predictive modeling (XGBoost, Random Forest, SVM, and GLMnet) and rigorous evaluation.

The notebook is designed to be readable by both technical and non-technical audiences, with explanations provided alongside code and outputs.


---

## Dataset Overview

The dataset captures **clinical trial behavior** for 1,000 lung cancer patients. Each row represents a unique participant and includes:

* **Patient profiles:** Demographic information such as age and gender.
* **Clinical markers:** Immune response scores and specific biological markers (Biomarker A and B).
* **Treatment details:** Trial arm assignments (Drug 1, 2, 3, or Placebo) and side effect tracking.
* **A binary outcome:** Indicating whether the patient was a "Responder" or "NonResponder" to the treatment.

---

## Key Takeaways

* **Biological signals matter:** Immune response scores and Biomarker B were identified as the most significant indicators of whether a patient would respond to treatment.
* **Drug 3 shows promise:** Initial analysis revealed that participants assigned to "Drug 3" had the highest proportion of successful responses compared to other trial arms.
* **Stability is critical for deployment:** While several models were tested, **XGBoost** was selected as the optimal choice due to its consistent, stable performance and lower variability, which is essential for predicting outcomes on new, unseen patients.
* **Data-driven roadmap for Phase II:** The analysis suggests that while a predictive signal exists, future trials should expand data collection to include genomic data to further increase accuracy before wider deployment.
