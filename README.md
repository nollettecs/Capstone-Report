# 🏠 Housing Affordability Forecasting — Capstone Project

This capstone project uses machine learning techniques to analyze and forecast trends in U.S. housing affordability. By combining datasets related to home prices and household income, the project explores how the affordability gap has evolved — and where it's headed through 2033.

## 📊 Project Overview

- **Objective:** To model the historical relationship between household income and home prices, and forecast how that relationship may change in the coming decade.
- **Key Metric:** Price-to-Income Ratio (PIR), used as a benchmark for housing affordability.
- **Tools & Libraries:**
  - Python, Jupyter Notebook
  - Pandas, NumPy, Matplotlib
  - Scikit-learn (Linear & Polynomial Regression)

---

## 🧠 Machine Learning Pipeline

1. **Data Collection:** Datasets from FHFA, FRED, Zillow, and Kaggle.
2. **Data Cleaning:** Removed unnecessary columns, handled missing values, reshaped ZHVI dataset.
3. **Feature Engineering:** Extracted `Year` from dates to use as model input.
4. **Modeling:**
   - Polynomial Regression (degree = 2) for Average Sales Price
   - Linear Regression for Income, FHFA HPI, and ZHVI
5. **Evaluation:** Used MAE and R² Score for model validation.
6. **Forecasting:** Generated 10-year predictions (2024–2033).
7. **Visualization:** Multi-line plots, PIR ratios, and bar charts to communicate findings.

---

## 📁 Repository Structure

```
capstone-project/
├── data/                   # Excel/CSV datasets
├── notebooks/              # Jupyter Notebooks
├── charts/                 # Exported visualizations
├── README.md               # This file
├── requirements.txt        # Python dependencies
└── ML_Pipeline_Evaluation.md  # Machine Learning summary answers
```

---

## 📈 Results Summary

| Dataset                 | Model Type         | MAE      | R² Score | Insight                      |
| ----------------------- | ------------------ | -------- | -------- | ---------------------------- |
| Avg. Sales Price        | Polynomial (deg=2) | \$28,751 | 0.55     | Nonlinear rise in prices     |
| Median Household Income | Linear Regression  | \$4,784  | 0.48     | Slower, consistent growth    |
| FHFA House Price Index  | Linear Regression  | \$39.86  | 0.31     | Moderate fit, upward trend   |
| ZHVI                    | Linear Regression  | N/A      | N/A      | Trend supports primary model |

- **Price-to-Income Ratio** is projected to exceed 5.5 by 2033 — well above the affordable threshold of 3.0–4.0.

---

## 🔍 Data Sources

- [FHFA House Price Index (HPI)](https://www.fhfa.gov/DataTools/Downloads/Pages/House-Price-Index.aspx)
- [FRED Median Household Income](https://fred.stlouisfed.org/series/MEHOINUSA672N)
- [FRED Average Sales Price of Houses](https://fred.stlouisfed.org/series/ASPUS)
- [Zillow Home Value Index (ZHVI)](https://www.zillow.com/research/data/)
- [Kaggle Housing Data](https://www.kaggle.com)

---

## 📌 How to Run

1. Clone this repo:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   ```
2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   pip install -r requirements.txt
   ```
3. Launch the Jupyter Notebook and run the analysis.
