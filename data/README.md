# Dataset Description

This directory contains the datasets used for the **Client Asset Allocation Modeling** project.

The data consists of synthetic banking client records with demographic, financial, and behavioral attributes.
Although the original dataset was designed for term-deposit subscription prediction, it is repurposed in this
project to model client portfolio allocation behavior.

---

## Data Source

The original dataset is sourced from Kaggle:  
- **Dataset:** Bank Marketing Dataset for Term Deposit Prediction  
- **Link:** https://www.kaggle.com/datasets/nisargpatel344/bank-marketing-dataset-for-term-deposit-prediction

The original dataset contains banking client records with demographic, financial, behavioral, and marketing
interaction features. It was originally designed for a **binary classification task**, where the target
variable indicates whether a client subscribed to a term deposit.

- Total Features: 45
- Total records: 100,000

---

## Feature Selection

To fit the asset allocation modeling setting, the original dataset was modified as follows:

- Selected only features relevant to client **financial capacity, life stage, and behavioral patterns**
- Removed marketing-specific variables and the original target variable to avoid information leakage
- Cleaned and encoded categorical variables for model training
- Constructed synthetic portfolio allocation targets across multiple asset classes
- Normalized allocation weights so that each client’s portfolio sums to 1
- Sampled 50% of the original records to reduce computational cost while maintaining sufficient
  data coverage for model training and evaluation

The resulting dataset is used to train **multi-output regression models** that predict client portfolio
allocations based on structured client profile data.

---

## Target Construction

Target variables are **synthetically constructed portfolio allocation weights** across five asset classes:

- US Equity  
- International Equity  
- Bonds  
- Cash  
- Alternatives  

Allocations are generated using financial features based on client characteristics and normalized
to sum to 1. 

---

## Files

- `raw_clients.csv`  
  Original client profile dataset before filtering.

- `processed_clients.csv`  
  Cleaned dataset with selected features and constructed portfolio allocation targets.

---



