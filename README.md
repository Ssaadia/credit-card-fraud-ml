# notebooks
https://github.com/Ssaadia/credit-card-fraud-ml/blob/main/notebooks/01-fraud-data-cleaning-and-validation.ipynb

https://github.com/Ssaadia/credit-card-fraud-ml/blob/main/notebooks/02-credit-card-fraud-ml-pipeline.ipynb

# dataset

https://www.kaggle.com/datasets/asqsaadia/cleaned-credit-card-fraud-dataset-for-ml

# credit-card-fraud-ml
# Credit Card Fraud Detection (Imbalanced Classification + Threshold Tuning)

This project builds a fraud detection model on the popular Credit Card Fraud dataset and focuses on correct evaluation under extreme class imbalance. Instead of relying on accuracy, the notebook emphasizes ROC–AUC, Precision–Recall (PR) analysis, and decision-threshold tuning to reduce missed fraud cases.

## Project Highlights
- End-to-end ML workflow (Define → Fit → Predict → Evaluate)
- Stratified train/test split to preserve class ratio
- Baseline Logistic Regression with proper scaling (Time, Amount)
- Evaluation using:
  - Confusion Matrix (TP/FP/FN/TN)
  - Precision, Recall, F1-score
  - ROC–AUC and PR–AUC (Average Precision)
- Threshold tuning (including fine-grained low thresholds) to improve fraud recall
- Business-aware trade-off discussion: missed fraud vs false alerts

## Dataset
- Source: Kaggle Credit Card Fraud Detection dataset (original)
- This project uses a cleaned version published on Kaggle by the author:
  - `/kaggle/input/cleaned-credit-card-fraud-dataset-for-ml/credit_card_cleaned.csv`

> Note: The dataset is highly imbalanced (fraud is a tiny fraction of transactions), so PR-based metrics are critical.

## Results Summary (Baseline + Threshold Tuning)
Baseline (threshold = 0.5) shows high overall accuracy but misses many fraud cases due to imbalance.

Key improvements were obtained by tuning the decision threshold:
- Lower thresholds increased recall (caught more fraud)
- Very low thresholds produced operationally high false positives
- A practical threshold was chosen to balance recall with manageable false alarms


## Repository Structure

credit-card-fraud-ml/
│
├── notebooks/
  └── 	01_fraud_data_cleaning_and_validation	
│ └── 02_credit_card_fraud_ml_pipeline.ipynb

├── reports/
│ 
├── README.md
└── requirements.txt



## How to Run
### Option A: Kaggle (recommended)
Open the notebook on Kaggle and run all cells.

### Option B: Local (Jupyter)
1. Clone the repo
2. Install dependencies
3. Run notebook

```bash
pip install -r requirements.txt
jupyter notebook
