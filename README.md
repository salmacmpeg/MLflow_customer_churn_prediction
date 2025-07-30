# 🧠 Customer Churn Prediction with MLflow Tracking

## 🚀 Overview
This project showcases how to apply MLflow to monitor and version classical machine learning experiments. It predicts customer churn using multiple classifiers, tracks evaluation metrics, and registers datasets dynamically.

## 📦 Dataset
Cleaned and preprocessed version of the **Iranian Customer Churn Prediction** dataset.

- Located in `telecome_customer_churn/`
- Files:
  - `train.csv`
  - `valid.csv`
  - `test.csv`

## 🧪 Models Used
Three classifiers are trained and logged:
- **Random Forest** (with customizable `n_estimators`)
- **Support Vector Machine** (with kernel tuning)
- **XGBoost** (default parameters)

## 🧮 Evaluation Metrics
For each model, the following metrics are computed and logged via MLflow:
- Balanced Accuracy
- Geometric Mean Score
- Matthews Correlation Coefficient
- Precision
- Recall
- F1 Score
- Confusion Matrix components: TP, TN, FP, FN

## 🔍 MLflow Features
- 🎯 Dataset registration via `mlflow.data.from_pandas`
- 🧬 Model signature inferred using `mlflow.models.infer_signature`
- 📊 Metrics logged dynamically during evaluation
- 📁 Timestamp-based run naming (`datetime.now()`)
- 🧱 Model artifacts logged using `mlflow.sklearn.log_model`

## 🧰 Usage/ How to run the experiments:
- Clone the repository.
- Ensure dataset is placed in `telecome_customer_churn/` folder.
- Make your own virtual environemnt .
- Install `poetry` then initialize it using `poetry init -n` in the terminal.
- Install dependencies using `poetry install`in the terminal.
- Run the `initialization.py` file to set the mlflow uri enviorment variable using `mlflow.set_tracking_uri("http://localhost:5000")`.
- Run the mlflow UI server using `mlflow server` in the terminal.
- Run the `(mlfow_experiment.ipynb)` notebook.
- Then visit the mlflow UI server http://localhost:5000 to inspect all tracked runs.
- After you finish terminate the server by typing `ctrl+c` in the terminal.

---
📂 Feel free to fork, modify, or repurpose for your own ML tracking workflows
