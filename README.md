# Bank Customer Churn Prediction

## Project Overview

Customer churn occurs when customers stop doing business with a company. For banks, identifying customers who are likely to leave is important for improving customer retention and maintaining long-term relationships.

This project uses machine learning classification techniques to predict whether a bank customer is likely to leave the bank based on their demographic and account information.

The goal is to build and evaluate predictive models that can help identify customers who may be at risk of churning.

## Project Objectives

- Explore and understand the bank customer dataset.
- Perform data inspection, cleaning, and exploratory data analysis.
- Prepare the dataset for machine learning.
- Train and evaluate multiple classification models.
- Compare model performance using appropriate evaluation metrics.
- Select and save the best-performing model.

## Dataset

The dataset contains 10,000 customer records and 18 columns.

The target variable is `Exited`:

- `0` – Customer stayed with the bank.
- `1` – Customer left the bank.

The dataset includes customer demographic, account, and activity information.

**Note:** The dataset is not currently included in this repository.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## Machine Learning Models

Four classification algorithms were trained and evaluated:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Gradient Boosting

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curve and AUC

### Performance Comparison

| Model | Accuracy | Precision | Recall | F1-Score | AUC |
|---|---:|---:|---:|---:|---:|
| Gradient Boosting | 0.87 | 0.79 | 0.51 | 0.62 | 0.877 |
| Random Forest | 0.87 | 0.80 | 0.48 | 0.60 | 0.865 |
| Decision Tree | 0.79 | 0.49 | 0.54 | 0.52 | 0.700 |
| Logistic Regression | 0.81 | 0.62 | 0.21 | 0.32 | 0.778 |

## Final Model Selection

Gradient Boosting was selected as the final model based on its overall performance.

It achieved:

- Accuracy: 87%
- Precision: 79%
- Recall: 51%
- F1-score: 0.62
- AUC: 0.877

Although Random Forest achieved slightly higher precision, Gradient Boosting performed better in recall, F1-score, and AUC.

This makes Gradient Boosting the strongest overall model among those evaluated.

## Project Structure

```text
bank-customer-churn/
│
├── Bank-Customer-Churn.ipynb
├── customer_churn_model.pkl
├── pyproject.toml
├── uv.lock
├── .gitignore
└── README.md
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Benjamin-Ajagun/bank-customer-churn-prediction.git
```

### 2. Navigate into the project

```bash
cd bank-customer-churn-prediction
```

### 3. Install dependencies

This project uses `uv` for Python environment and dependency management.

```bash
uv sync
```

### 4. Launch Jupyter Notebook

```bash
uv run jupyter notebook
```

Open `Bank-Customer-Churn.ipynb` and run the notebook cells sequentially.

**Dataset requirement:** Obtain the dataset separately and place it in the location expected by the notebook before running the analysis.

## Future Improvements

- Improve churn detection, particularly recall.
- Explore additional classification algorithms.
- Perform further feature engineering.
- Experiment with different decision thresholds.
- Develop a simple interface for making customer churn predictions.
- Explore model deployment.

## Author

**Benjamin Ajagun**

Machine Learning | Data Science