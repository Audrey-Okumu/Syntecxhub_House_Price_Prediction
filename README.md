# House Price Prediction

---

## Project Overview

**This project aims to predict house prices using a regression model trained on a housing dataset. The workflow includes data cleaning, feature selection, model training, evaluation, and generating predictions on test data.**

---

## Dataset

**The dataset contains various features related to residential properties such as lot size, year built, garage details, basement details, etc.**

**Missing values were handled with appropriate strategies:**

- Numerical columns: filled with median values.

- Categorical columns: filled with 'None' or mode.

- Basement and garage features: filled with 0 where missing.

---

## Preprocessing Steps

- Handled missing values for numerical and categorical columns.
- One-hot encoded categorical variables.
- Aligned test dataset features with training dataset columns.

---

## Model
- **Type:** Linear Regression
- **Training:** Used 80% of the dataset for training and 20% for validation.
- **Evaluation Metrics:**
      - **RMSE:** Root Mean Squared Error
      - **R² Score:** Coefficient of Determination

---

## Interpretation:

Feature coefficients indicate which features increase or decrease house prices.

**Example:** OverallQual (overall material and finish quality) has a strong positive coefficient.

---

## How to Run

### Train the model:
```
jupyter notebook notebooks/model_training.ipynb
```

This will train the model and save it to the models folder.

### Make predictions on new data:
```
jupyter notebook notebooks/making_predictions.ipynb
```

Outputs predictions to predictions.csv.

### Optional: Interpret coefficients or visualize predictions in model_training.ipynb.


## Folder Structure
```
House_Price_Prediction/
│
├─ notebooks/
│    ├─ data/
│   │  ├─ X.csv
│   │  ├─ y.csv
│   │  └─ test.csv
│   ├─ model_training.ipynb
│   └─ making_predictions.ipynb
│
│
│
├─ models/
│   ├─ linear_regression_model.pkl
│   └─ training_columns.pkl
│
├─  README.md
│
└─requirements.txt
```
