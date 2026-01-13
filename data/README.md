DESCRIPTION OF DATA FROM KAGGLE
# Dataset Description

This directory contains the datasets used for the **Client Asset Allocation Modeling** project.

The data consists of synthetic banking client records with demographic, financial, and behavioral attributes.
Although the original dataset was designed for term-deposit subscription prediction, it is repurposed in this
project to model client portfolio allocation behavior.

---

## Source

- Synthetic banking client dataset
- Total records: 100,000
- Original target variable: `TermDepositSubscribed` (binary)
- File format: CSV

---

## Feature Selection

Only features relevant to **client financial capacity, life stage, and behavioral patterns** are used.
Marketing-specific and post-decision variables are excluded to avoid information leakage.

### Included Feature Categories
- **Demographics:** age, employment status, education level
- **Financial capacity:** income, credit score, balance indicators
- **Relationship depth:** account tenure, number of products
- **Behavioral indicators:** transaction frequency, digital activity

### Excluded Features
- Marketing campaign identifiers
- Contact channel and call duration
- Original target variable (`TermDepositSubscribed`)
- Any features dependent on marketing outcomes

---

## Target Construction

Target variables are **synthetically constructed portfolio allocation weights** across five asset classes:

- US Equity  
- International Equity  
- Bonds  
- Cash  
- Alternatives  

Allocations are generated using financial heuristics based on client characteristics and normalized
to sum to 1. The modeling task is framed as a **multi-output regression problem**.

---

## Files

- `raw_clients.csv`  
  Original client profile dataset before filtering.

- `processed_clients.csv`  
  Cleaned dataset with selected features and constructed portfolio allocation targets.

---

## Notes

- All data is synthetic and used solely for educational and demonstration purposes.
- No personally identifiable information (PII) is included.

https://www.kaggle.com/datasets/nisargpatel344/bank-marketing-dataset-for-term-deposit-prediction
