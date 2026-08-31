# 🏠 House Price Prediction

**CloudExify Summer Internship 2026 — Data Science Month 2, Project 3**

A machine learning project that predicts house prices using **Linear Regression** and **Random Forest**, based on area, number of bedrooms, age of the property, and location.

---

## 📌 Overview

This notebook walks through a complete, beginner-friendly ML workflow:

1. Load and explore housing data
2. Clean missing values and remove price outliers (IQR method)
3. Encode categorical features (`Location`) using one-hot encoding
4. Train a **Linear Regression** model
5. Train a **Random Forest Regressor** and compare performance
6. Visualize feature importance
7. Predict prices for new/custom house inputs
8. (Optional) Interactive slider-based prediction using `ipywidgets`

---

## 📂 Dataset

**File:** `sample_data.csv`

| Column     | Description                          |
|------------|---------------------------------------|
| `Area`     | Area of the house (in sqft)          |
| `Bedrooms` | Number of bedrooms                   |
| `Age`      | Age of the property (in years)       |
| `Location` | Categorical: North / South / East    |
| `Price`    | Target variable — house price (Rs)   |

> The dataset contains a few missing `Age` values and some price outliers, both of which are handled in the preprocessing steps.

---

## ⚙️ Requirements

```bash
pip install pandas numpy scikit-learn matplotlib
```

Optional (for the interactive slider widget at the end of the notebook):

```bash
pip install --upgrade ipywidgets widgetsnbextension
jupyter nbextension enable --py widgetsnbextension
```

---

## 🚀 How to Run

### Option 1 — Local Jupyter Notebook
1. Clone this repo / download the files.
2. Make sure `sample_data.csv` is in the **same folder** as the notebook.
3. Open `house_price_prediction.ipynb` in Jupyter and run all cells in order.

### Option 2 — Google Colab
1. Open the notebook in Colab.
2. Run the first cell — it will prompt you to upload `sample_data.csv` directly.
3. Run the remaining cells in order.

---

## 🧠 Models Used

| Model                | Purpose                                      |
|-----------------------|-----------------------------------------------|
| Linear Regression      | Baseline model                               |
| Random Forest Regressor | Usually performs better on non-linear data |

The notebook automatically compares both models on **R², RMSE, and MAE**, and selects the better-performing one as `best_model` for final predictions.

---

## 📊 Results & Visualizations

- **Feature Importance chart** — shows which features (Area, Bedrooms, Age, Location) most influence price predictions, based on the Random Forest model.
- **Actual vs Predicted scatter plot** — visualizes how close the model's predictions are to real prices, with a red dashed "perfect prediction" reference line.

---

## 🔮 Making Your Own Prediction

Edit the values in the **"Try Your Own Prediction"** cell:

```python
my_area = 300          # in sqft
my_bedrooms = 3
my_age = 5              # in years
my_location = 'North'   # 'North', 'South', or 'East'
```

Re-run the cell to instantly get a predicted price — no extra setup needed.

An optional interactive version with sliders and a "Predict Price" button is also included for those who want to enable `ipywidgets`.

---

## 📁 Project Structure

```
├── house_price_prediction.ipynb   # Main notebook
├── sample_data.csv                # Dataset
└── README.md                      # Project documentation
```

---

## 📝 Notes

- Outliers in `Price` are removed using the **1.5×IQR rule**, a standard statistical approach rather than manually picking rows to drop.
- Categorical `Location` values are one-hot encoded — make sure any new prediction input matches the exact same column structure as the training data.

---

## 👤 Author

CloudExify Summer Internship 2026 — Data Science Track
