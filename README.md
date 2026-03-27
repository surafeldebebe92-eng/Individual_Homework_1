# Individual_Homework_1

# COMPAS Recidivism Risk Score Analysis

## Purpose of the Analysis

This project replicates and extends the racial bias analysis of the COMPAS (Correctional Offender Management Profiling for Alternative Sanctions) recidivism risk scoring system, originally published by ProPublica in 2016.

The COMPAS algorithm is used by courts across the United States to assess the likelihood that a defendant will re-offend. This analysis investigates whether the COMPAS scores exhibit racial bias by examining:

- Whether Black defendants are disproportionately assigned higher risk scores compared to white defendants with similar criminal histories
- How demographic factors (race, sex, age) influence predicted risk scores after controlling for relevant variables such as prior criminal record and charge severity
- The false positive and false negative rates of the COMPAS score across racial groups, revealing disparate error distributions

The dataset comes from Broward County, Florida and was obtained from ProPublica's public GitHub repository.

---

## Python Libraries Used

|
 Library 
|
 Version 
|
 Purpose 
|
|
---
|
---
|
---
|
|
`pandas`
|
 ≥ 1.5 
|
 Data loading, filtering, and manipulation 
|
|
`numpy`
|
 ≥ 1.23 
|
 Numerical computations and array operations 
|
|
`matplotlib`
|
 ≥ 3.6 
|
 Bar chart visualizations of decile score distributions 
|
|
`statsmodels`
|
 ≥ 0.13 
|
 Logistic regression modeling to detect racial bias 
|
|
`warnings`
|
 (stdlib) 
|
 Suppressing non-critical warnings 
|

Install all required libraries with:

```bash
pip install pandas numpy matplotlib statsmodels
