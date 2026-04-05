# Explaining the COMPAS Replacement Model

A reproducible analysis of a COMPAS-based risk prediction model using SHAP, LIME, and counterfactual explanations to evaluate transparency, fairness, and governance implications.

**Name:** Natchapa Aunkay (Gift)  
**Course:** DNSC 6330 – Responsible Machine Learning  
**Instructor:** Prof. Michael Akinwumi  
**Assignment:** Individual Homework 3 

---

## 1. Purpose of the Analysis

This project focuses on explaining the behavior of a machine learning model trained on the COMPAS dataset. Instead of only evaluating model performance, the goal is to understand how and why the model makes predictions.

The analysis applies three explanation techniques:

SHAP (global and local explanations)
LIME (local explanations)
Counterfactual explanations using DiCE
The objective is to compare these methods and assess their implications for fairness, transparency, and model governance.

---

# 2. Python Libraries Used

The following libraries are used:

pandas
numpy
matplotlib
scikit-learn
shap
lime
dice-ml

---

## 3. Instructions for Reproducing the Results

Step 1: Clone the repository

git clone https://github.com/gifyncp/assignment2-rML-Natchapa.git cd assignment2-rML-Natchapa

Step 2: Run the notebook

jupyter notebook

Open Assignment02_rML.ipynb and run all cells sequentially.

---

## 4. Workflow Overview

### Step 1: SHAP Analysis

Compute SHAP values on the test dataset
Generate a beeswarm summary plot
Create waterfall plots for:
Highest-risk defendant (per racial group)
Lowest-risk defendant (per racial group)

### Step 2: LIME Explanations

Apply LIME to the same selected individuals
Compare feature attributions between SHAP and LIME
Identify agreements and divergences in explanations

### Step 3: Counterfactual Explanations

Generate counterfactuals using DiCE
Identify minimal feature changes required to flip predictions
Highlight any changes involving immutable features (e.g., race, sex)

### Step 4: Governance Interpretation

Analyze what explanation results reveal about model behavior
Discuss risks such as proxy variables and fairness concerns
Provide recommendations for monitoring and governance

---

## 5. Reproducibility and Documentation

The notebook is fully reproducible
Each step includes comments explaining the methodology
The workflow follows the structure required in the assignment

---

## 6. Notes

SHAP, LIME, and counterfactual methods may produce different explanations
Differences arise from methodological assumptions and approximations
No single explanation method is sufficient on its own

---

## AI Acknowledgment

Generative AI (ChatGPT by OpenAI) was used to assist with:
- Clarifying assignment requirements  
- Debugging Python code  
- Improving code structure and documentation  

All analysis, interpretation, and conclusions were independently completed and verified by me.
