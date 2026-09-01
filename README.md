# CloudExify Project 3 — House Price Prediction

**CloudExify Data Science Internship 2026 — Month 2, Project 3 (1st)**

## Overview

This project predicts residential house prices using **Linear Regression** and **Random Forest Regression**, trained on area, number of bedrooms, age, and location, so buyers, sellers, and agents can get a quick, data-driven price estimate instead of relying purely on manual appraisal.

## Files in this repository

| File | Description |
|---|---|
| `house_price_prediction.ipynb` | Main Jupyter Notebook — data cleaning, model training, evaluation, and predictions |
| `sample_data.csv` | House listings dataset used for the analysis |
| `House_Price_Prediction_Report.docx` | Full project report with methodology, results, and visualizations |
| Screenshot PNGs | Screenshots of the notebook running with outputs and charts |

## What was done

- Loaded and explored the housing dataset (Area, Bedrooms, Age, Location, Price)
- Handled missing values in the `Age` column and removed statistical price outliers using the **1.5×IQR rule**
- Encoded the categorical `Location` feature using one-hot encoding
- Split the data into training (80%) and test (20%) sets
- Trained a **Linear Regression** model as a baseline
- Trained a **Random Forest Regressor** (100 trees) and compared it against the baseline using R², RMSE, and MAE
- Automatically selected the better-performing model as `best_model`
- Analyzed feature importance to identify which factors most influence price
- Visualized actual vs. predicted prices, price distribution, and price vs. area
- Built an editable prediction cell (plus an optional `ipywidgets` slider interface) for predicting the price of a new house

## Key Findings

- **Random Forest outperformed Linear Regression** — R² of 0.970 vs. 0.860, and a lower average error (RMSE ~Rs 235K vs. ~Rs 511K)
- **Area is the dominant price driver**, accounting for ~91% of the Random Forest's feature importance
- **Location and Age have a smaller but real effect** on price, while number of Bedrooms contributes the least once Area is accounted for
- Price data was right-skewed with a few high-value outlier listings, which were removed to prevent them from distorting the models

## Tools Used

Python 3 · Jupyter Notebook · pandas · NumPy · scikit-learn · Matplotlib · ipywidgets (optional)

## Author

Hafsa Bukhtiar Chishti — Software Engineering, COMSATS University Islamabad, Sahiwal Campus
