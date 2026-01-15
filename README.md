# Client Asset Allocation Modeling with Machine Learning

## Overview
This project explores how client demographic, financial, and behavioral data can be used to model portfolio asset allocation decisions.
The goal is to simulate a data-driven wealth management workflow, where client profiles are mapped to diversified portfolio allocations across 5 asset classes: US Equity, International Equity, Bonds, Cash, REIT.

The problem is framed as a multi-output regression task, predicting allocation weights that sum to one for each client.

## Business Motivation
In wealth and asset management, portfolio construction is influenced by multiple client factors such as financial capacity, risk tolerance, life stage, and behavioral characteristics.

This project demonstrates how machine learning models can support portfolio decision-making by learning allocation patterns from structured client data.

## Evaluation Approach ???
Model performance is assessed using Root Mean Squared Error (RMSE) on allocation weights.

Predicted allocations are post-processed to enforce portfolio constraints, ensuring valid and interpretable results.
