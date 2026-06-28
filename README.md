# Healthcare Access & Systems Analysis

**A Python data analysis capstone project exploring hospital admission patterns, patient billing, medication outcomes, and test result prediction across 55,500 patient records.**

---

## Project Overview

This project analyses a healthcare dataset covering 6 medical conditions, 5 insurance providers, and multiple admission types. The goal was to answer 5 research questions about how patients move through hospital systems — and whether machine learning can predict their test outcomes.

**Analyst:** Ogo Chukwuemeka Okereke  
**Programme:** TDI Python Data Analysis  
**Dataset:** [Healthcare Dataset — Prasad Patil (Kaggle)](https://www.kaggle.com/datasets/prasad22/healthcare-dataset)  
**Records:** 55,500 patients · 15 variables

---

## Research Questions

| # | Question |
|---|----------|
| RQ1 | Which medical conditions drive the most admissions, and how does admission type vary? |
| RQ2 | What factors most influence a patient's length of hospital stay? |
| RQ3 | How does billing amount vary across insurance providers and medical conditions? |
| RQ4 | Is there a relationship between medication prescribed and test result outcomes? |
| RQ5 | Can we predict a patient's test result using demographic and admission data? |

---

## Key Findings

**RQ1 — Admission Patterns**
- All 6 conditions place near-equal burden on the hospital system (spread of just 123 patients top to bottom)
- Diabetes has the highest urgent admissions (3,197) — suggesting diabetic episodes more frequently need immediate attention

**RQ2 — Length of Stay**
- Average stay is consistent across all conditions (~15.5 days), pointing to standardised care protocols
- Elderly emergency patients (50+) represent the highest combined resource demand

**RQ3 — Billing & Insurance**
- Insurance providers charge nearly identically: $25,415 (UnitedHealthcare) to $25,630 (Medicare)
- Obesity ($25,807) and Diabetes ($25,662) are the costliest conditions; Cancer the cheapest ($25,155)

**RQ4 — Medication & Test Results**
- No single medication is associated with better or worse outcomes — all split ~33/33/33 across Abnormal, Inconclusive, Normal
- Arthritis has the highest Abnormal rate (34.2%); Asthma and Hypertension have the highest Normal rates

**RQ5 — ML Prediction**
- Random Forest Classifier achieved **41.69% accuracy** — above the 33.3% random baseline
- Demographic and admission data alone are weak predictors; richer clinical features would improve this significantly

---

## Project Structure

```
healthcare-analysis/
│
├── data/
│   └── healthcare_dataset.csv        # Source dataset (Kaggle)
│
├── notebooks/
│   └── healthcare_analysis.ipynb     # Full analysis notebook
│
├── visuals/
│   ├── rq1_admission_patterns.png
│   ├── rq2_length_of_stay.png
│   ├── rq3_billing_insurance.png
│   ├── rq4_medication_test_results.png
│   └── rq5_ml_model.png
│
├── healthcare_dashboard.py           # Interactive Plotly Dash dashboard
├── requirements.txt
└── README.md
```

---

## Interactive Dashboard

The project includes a fully interactive **Plotly Dash dashboard** with live filters across all 5 research questions.

**To run it locally:**

```bash
# Install dependencies
pip install dash plotly pandas numpy scikit-learn

# Launch the dashboard
python healthcare_dashboard.py
```

Then open your browser at `http://127.0.0.1:8050`

**Dashboard features:**
- Live KPI cards (avg billing, avg stay, top condition)
- Sidebar filters: condition, admission type, insurance, age range, gender
- All 5 RQ charts update in real time based on your selection
- Confusion matrix and feature importance for the ML model

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python 3 | Primary analysis environment |
| Pandas & NumPy | Data cleaning and transformation |
| Matplotlib & Seaborn | Static visualisations |
| Plotly & Dash | Interactive dashboard |
| Scikit-learn | Random Forest Classifier (RQ5) |
| Jupyter Notebook | Development environment (VS Code) |

---

## How to Run the Notebook

```bash
# Clone the repo
git clone https://github.com/Mikkymo/healthcare-analysis.git
cd healthcare-analysis

# Install dependencies
pip install -r requirements.txt

# Open the notebook
jupyter notebook notebooks/healthcare_analysis.ipynb
```

> **Note:** The dataset is not included in this repo due to size. Download it from [Kaggle](https://www.kaggle.com/datasets/prasad22/healthcare-dataset) and place it in the `data/` folder.

---

## Strategic Recommendations

1. **Balanced resource allocation** — all 6 conditions generate nearly equal admissions; avoid over-investing in single-condition wards
2. **Fast-track elderly emergency patients** — this group has the longest stays and highest resource demand
3. **Target chronic disease prevention** — Obesity and Diabetes drive the highest billing; preventive programmes offer the best cost reduction potential
4. **Audit Arthritis treatment protocols** — it carries the highest Abnormal test rate (34.2%)
5. **Invest in richer clinical data** — lab values, vitals, and symptom scores would substantially improve ML prediction accuracy

---

## Author

**Ogo Chukwuemeka Okereke**  
Data Analyst · Abuja, Nigeria  
[LinkedIn](https://linkedin.com/in/ogochukwuemeka/) · [Portfolio](https://mikkymo.github.io/portfolio/)
