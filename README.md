# Real Bank Fraud Detection

This project analyzes and detects fraudulent transactions using a real-world bank transaction dataset.

## Files

- [`fraud_data.csv`](fraud_data.csv): The dataset containing 500 transactions with features:
  - TransactionID
  - Amount
  - Time
  - Location
  - MerchantCategory
  - CardHolderAge
  - IsFraud (target variable)
- [`fraud_detection.ipynb`](fraud_detection.ipynb): Jupyter notebook with data analysis, preprocessing, model training, and evaluation.

## Workflow

1. **Data Loading & Exploration**
   - Load data from `fraud_data.csv`.
   - Explore missing values, duplicates, and class imbalance.

2. **Preprocessing**
   - Handle missing values (e.g., fill `CardHolderAge` with median).
   - Encode categorical features (`Location`, `MerchantCategory`).
   - Scale numerical features (`Amount`, `CardHolderAge`, `Time`).

3. **Modeling**
   - Train/test split with stratification on `IsFraud`.
   - Models used:
     - Logistic Regression (recommended)
     - Random Forest (for comparison)
   - Handle class imbalance using `class_weight='balanced'`.

4. **Evaluation**
   - Metrics: Precision, Recall, F1-score, ROC-AUC.
   - Visualize class distribution and results.

## Results

- **Logistic Regression**: Reliable, interpretable, and effective for imbalanced data.
- **Random Forest**: No significant improvement, risk of overfitting.

## Usage

Open [`fraud_detection.ipynb`](fraud_detection.ipynb) in Jupyter and run the cells to reproduce the analysis.

## Requirements

- Python 3.12+
- pandas, numpy, scikit-learn, matplotlib, seaborn

Install dependencies:
```sh
pip install pandas numpy scikit-learn matplotlib seaborn
```

## License

For educational use only.