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

### Option 1: Google Colab (Recommended)

1. Go to [https://colab.research.google.com](https://colab.research.google.com)
2. Click **File → New Notebook**
3. Copy and paste each cell from the provided `.ipynb` file into separate Colab cells in order
4. Click **Runtime → Run All**
5. No additional setup is required — all libraries are pre-installed in Colab and the dataset is loaded directly from the internet

### Option 2: Run Locally

1. **Clone this repository:**
   ```bash
   git clone <your-repo-url>
   cd <your-repo-folder>
