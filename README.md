# Disparate Impact Audit – COMPAS Dataset

**Name:** Natchapa Aunkay (Gift)  
**Course:** DNSC 6330 – Responsible Machine Learning  
**Instructor:** Prof. Michael Akinwumi  
**Assignment:** Individual Homework 3 

---

## 1. Purpose of the Analysis

In this assignment, I evaluate fairness in a predictive model using the COMPAS dataset. The goal is to check whether the model shows any bias across different demographic groups, especially race and sex.

---
## 2. Python Libraries Used

The following libraries are used:

- pandas — for data manipulation and grouping
- numpy — for numerical calculations
- matplotlib — for visualization (bar charts)
- scipy — for basic statistical functions
- statsmodels — for statistical testing (two-proportion z-test)

---
## 3. Instructions for Reproducing the Results

Step 1: Clone the repository

git clone https://github.com/gifyncp/assignment3-rML-Natchapa.git cd assignment3-rML-Natchapa

Step 2: Run the notebook

jupyter notebook

Open Assignment03_rML.ipynb and run all cells sequentially.

Step 3: Run all cells in order:
- 1: Compute AIR, ME, SMD
- 2: Perform intersectional analysis
- 3: Compute FPR, FNR and run z-test
- 4: Generate visualization
- 5: Review compliance memo

Step 4: The output will include:
- Tables of fairness metrics
- Intersectional results
- Error rate comparison
- Visualization chart
- Final memo

---

## 4. Workflow Overview

### 1. Disparity Metrics (AIR, ME, SMD)

I computed:
- AIR (Adverse Impact Ratio)
- ME (Mean Error)
- SMD (Standardized Mean Difference)
for both race and sex using Caucasian and Male as reference groups.

These metrics help me understand differences in selection rates and score distributions across groups.

### 2. Intersectional Analysis (race × sex)

I created subgroups by combining race and sex (e.g., Hispanic / Female).
I filtered out small groups (n < 30) to keep results reliable.

From this analysis, I found that:

- Hispanic females had the lowest AIR (~0.154)
This means this group has the lowest chance of receiving a favorable outcome compared to the reference group (Caucasian / Male).

### 3. Error Rate Analysis (FPR, FNR)

I calculated:
- False Positive Rate (FPR)
- False Negative Rate (FNR)
by race.
I found that:
- African-American individuals have higher FPR than Caucasians
This suggests they are more likely to be incorrectly classified as high risk.

### 4. Statistical Test (z-test)

I used a two-proportion z-test to compare African-American and Caucasian groups.

The result shows the difference is statistically significant (p < 0.05), meaning the disparity is not due to random chance.

### 5. Visualization

I created a bar chart showing FPR and FNR by race, with a baseline line for the Caucasian group.
This makes it easier to compare disparities visually.

---

## Key Takeaways

Some groups have AIR below 0.80, indicating potential bias
Hispanic females are the most disadvantaged subgroup
African-American individuals have higher false positive rates
Disparities are statistically significant
Limitations
The COMPAS dataset may contain historical bias
Different fairness metrics may give different conclusions
Small groups may affect stability of results

---

## AI Acknowledgment

Generative AI (ChatGPT by OpenAI) was used to assist with:
- Clarifying assignment requirements  
- Debugging Python code  
- Improving code structure and documentation  

All analysis, interpretation, and conclusions were independently completed and verified by me.
