# Financial Risk for Loan Approval

This repository contains a comprehensive workflow for financial risk analysis and loan approval prediction. Using a synthetic dataset of 20,000 records, this project demonstrates how to build predictive models to assess financial risk (`RiskScore`) and classify loan approval outcomes (`LoanApproved`). It incorporates data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and evaluation.

---

## Dataset Overview

The dataset includes diverse features, such as demographic information, credit history, employment status, income levels, and existing debts. It supports two primary tasks:

1. **Risk Score Regression**: Predict a continuous risk score indicating the likelihood of loan default or financial instability.
2. **Loan Approval Classification**: Determine whether a loan application will be approved (`1`) or denied (`0`).

### Key Features
- **Demographic Data**: Age, Marital Status, Number of Dependents, etc.
- **Financial Metrics**: Annual Income, Savings Balance, Debt-To-Income Ratio, Total Liabilities, etc.
- **Credit History**: Credit Score, Payment History, Bankruptcy Records.
- **Loan Details**: Loan Amount, Purpose, Duration, Interest Rates.

---

## Project Workflow

### 1. **Data Preprocessing**
   - Addressed missing values and duplicated rows.
   - Performed outlier handling using Winsorization and log transformations to normalize skewed distributions.
   - Standardized numerical features and encoded categorical variables using one-hot encoding.

### 2. **Exploratory Data Analysis (EDA)**
   - Visualized distributions, correlations, and key patterns across features.
   - Investigated relationships between features (e.g., `RiskScore` vs. `LoanApproved`) to derive meaningful insights.

### 3. **Feature Engineering**
   - Created derived features, such as `DebtToIncomeRatio` and `TotalDebtToIncomeRatio`.
   - Selected important predictors through feature importance analysis.

### 4. **Model Training**
   - Utilized **Gradient Boosting Classifier** for binary classification and fine-tuned hyperparameters to optimize performance.
   - Achieved near-perfect model metrics with an ROC-AUC score of **0.9999**.

### 5. **Evaluation**
   - Validated the model using precision-recall curves, confusion matrices, and cross-validation.
   - Assessed feature contributions through SHAP and feature importance plots.

---

## Key Results

- **Model Performance**:
  - ROC-AUC Score: **0.9999**
  - Cross-Validation Accuracy: **99.78%**
- **Top Features**:
  - `RiskScore`, `TotalDebtToIncomeRatio`, `DebtToIncomeRatio`, and `MonthlyIncome` were identified as the most impactful features.

---

## Usage

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/Financial-Risk-for-Loan-Approval.git
cd Financial-Risk-for-Loan-Approval
```

### 2. Install Dependencies
Create a virtual environment and install the required libraries:
```bash
pip install -r requirements.txt
```

### 3. Run the Notebook
Open the Jupyter Notebook to explore the workflow:
```bash
jupyter notebook Financial_Risk_for_Loan_Approval.ipynb
```

### 4. Deploy the Model
Save the trained model and deploy it using Flask or FastAPI. Example deployment scripts are included in the repository.

---

## Future Work

- Validate the model on real-world datasets to ensure scalability and robustness.
- Enhance the workflow by integrating additional algorithms like XGBoost or LightGBM for comparative analysis.
- Extend the solution to include explainability tools for transparency in decision-making.
- Implement a real-time API to automate predictions for loan applications.

---

## Acknowledgments

This project was built using a synthetic dataset from [Kaggle](https://www.kaggle.com/datasets/lorenzozoppelletto/financial-risk-for-loan-approval). It provides an excellent foundation for learning financial risk assessment techniques and applying machine learning models in finance.

---

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
