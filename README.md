Applied Data Mining – Final Team Project
This repository showcases a complete, end-to-end data science project completed as part of a graduate-level Applied Data Mining course. The project demonstrates practical experience transforming raw clinical trial data into predictive insights using R.

The work emphasizes rigorous data pre-processing, statistical validation, and model tuning, not just building algorithms.

Project Objective
Triamex Biotech provided clinical trial data for a new mRNA-2206 drug protocol and asked for insights into which patients are likely to respond to treatment.

The goal of the assignment was to:

Clean and prepare a complex clinical dataset of 1,000 patient records

Identify biological and physiological markers linked to successful treatment outcomes

Apply advanced machine-learning techniques to handle class imbalance and non-linear data

Translate technical model performance into clinical insights to inform FDA submissions

What This Repository Contains
A fully documented R Markdown report containing:

Data importing, median imputation, and outlier capping

Feature engineering, including one-hot encoding and SMOTE resampling

Exploratory data analysis with ggplot2 visualizations

Comparative modeling using GLMnet, Random Forest, SVM, and XGBoost

Model evaluation through 3-fold cross-validation and ROC-AUC analysis

The report is designed to be readable by a technical audience, providing clear justifications for every step of the analytical pipeline.

Dataset Overview
The dataset captures clinical and demographic features for patients participating in a Phase I lung cancer drug trial. Each row represents a single patient session and includes:

Patient demographics (age and weight)

Specific clinical markers (Biomarker A and Biomarker B)

Physiological engagement scores (Immune response and tumor volume change)

A binary outcome indicating whether the patient was a "Responder" or "NonResponder"

Key Takeaways
Immune response is the strongest signal: Patients with higher immune_response_score metrics were significantly more likely to be classified as Responders (p=0.034).

Non-linear models outperform linear ones: The SVM with a Radial Basis Function kernel achieved the best balance of AUC (0.676) and Accuracy, effectively capturing complex decision boundaries.

Handling imbalance is critical: Applying SMOTE resampling was essential to prevent model bias, as the dataset was naturally weighted toward NonResponders.

Biomarkers provide secondary support: While not as strong as immune scores, biomarker_B showed a secondary correlation that helped refine model sensitivity.

Phase I data has inherent limits: The modest overall predictive power highlights that while key signals exist, clinical outcomes are influenced by factors beyond the current feature set.
