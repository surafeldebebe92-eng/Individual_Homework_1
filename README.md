# COMPAS Recidivism Risk Score Analysis

## Purpose of the Analysis

This project replicates and extends the racial bias analysis of the COMPAS (Correctional Offender Management Profiling for Alternative Sanctions) recidivism risk scoring system, originally published by ProPublica in 2016.

The COMPAS algorithm is used by courts across the United States to assess the likelihood that a defendant will re-offend. This analysis investigates whether the COMPAS scores exhibit racial bias by or not examining several things:

- Whether Black defendants are disproportionately assigned higher risk scores compared to white defendants with similar criminal histories
- How demographic factors (race, sex, age) influence predicted risk scores after controlling for relevant variables such as prior criminal record and charge severity
- The false positive and false negative rates of the COMPAS score across racial groups, revealing disparate error distributions

The dataset comes from Broward County, Florida and was obtained from ProPublica's public GitHub repository.

---

## Python Libraries Used

| Library | Version |
|---|---|
| `pandas` | Data loading, filtering, and manipulation |
| `numpy` | Numerical computations and array operations |
| `matplotlib` | Bar chart visualizations of decile score distributions |
| `statsmodels` | Logistic regression modeling to detect racial bias |
| `warnings` | Suppressing non-critical warnings |


## Instructions for Reproducing the Results

1. Open the notebook `Lecture_01_alignment.ipynb` in Google Colab
2. Run all cells from top to bottom using **Runtime → Run All**
3. The dataset will load automatically from the ProPublica GitHub repository — no file uploads needed

### Workflow

1. **Load the data** — The raw COMPAS dataset is read directly from a URL into a pandas DataFrame
2. **Filter and clean** — Rows are filtered based on data quality conditions (charge date window, valid recidivism flags, charge type, and score availability)
3. **Explore demographics** — Breakdown of race, sex, and age category distributions are printed and analyzed
4. **Visualize decile scores** — Bar charts compare COMPAS decile score distributions between Black and white defendants
5. **Run logistic regression** — A logistic regression model predicts whether a defendant receives a high COMPAS score, controlling for race, sex, age, prior convictions, charge severity, and actual recidivism
6. **Calculate odds ratios** — Odds ratios are computed to quantify how much more likely certain groups are to receive a higher score
7. **Evaluate with confusion matrices** — Model predictions are compared against actual outcomes, both overall and broken down by race
8. **Assess disparity** — False positive and false negative rates are compared across racial groups to identify bias in the scoring system

### Notes

- Cells must be run in order — each cell depends on variables defined in the cells above
- Results may differ slightly from the original R output due to differences in how Python and R handle statistical modeling internally
