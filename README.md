# CREDIGuard: Targeted Credit Card Fraud Detection

## Overview
CREDIGuard is a sophisticated machine learning-based fraud detection system designed to identify fraudulent activities in credit card transactions. The project was developed as part of the American Express Campus Challenge and focuses on identifying specific fraudsters responsible for a surge in default rates with minimal impact on legitimate customers.

## Project Features
- **Dataset**: The dataset used in this project contains over 62,000 rows and 60+ columns, including variables related to customer onboarding, spending behavior, and default indicators.
- **Data Preprocessing**:
  - **Missing Data Handling**: Applied KNN Imputer to handle missing values in numerical columns, ensuring data completeness.
  - **Skewed Data Transformation**: Performed Power and Square Root transformations to correct skewed distributions in key features.
  - **Categorical Data Encoding**: Employed OneHotEncoder to convert categorical features into a numerical format suitable for model training.
  - **SMOTE**: Addressed class imbalance in the training data using Synthetic Minority Over-sampling Technique (SMOTE).
- **Modeling**:
  - **Ensemble Stacking Classifier**: Built an ensemble model comprising XGBoost, CatBoost, and a meta-classifier (Logistic Regression) for robust prediction.
  - **Calibration & Threshold Tuning**: Calibrated the model using isotonic regression and fine-tuned the decision threshold to optimize performance.
- **Performance**:
  - **Optimal Threshold**: Achieved an optimal threshold of `0.21`, leading to a balanced F1-score of `0.60` for fraud detection.
  - **Accuracy**: The model demonstrated high accuracy, maintaining a precision of `0.70` and recall of `0.53` for the minority class (fraud cases).

## Installation
To replicate this project, follow the steps below:

1. Clone the repository:
   ```bash
   git clone https://github.com/a-m-a-nkumar/CreditGuard.git
    ```
2. Install the required dependencies:

```bash

    pip install -r requirements.txt
```
 3. Download and place the dataset (real_data_r3.xlsx) in the root directory.

## Usage

To run the model training and evaluation:

```bash

python Amex_CrediGuard.ipynb
```
## Results

The final model was tested on a hold-out dataset and evaluated on the following metrics:
```
    Accuracy: 99.61%
    F1-Score: 0.60
    Precision: 0.70
    Recall: 0.53
```
## Conclusion

CREDIGuard successfully identifies fraudulent credit card transactions with high precision and minimal impact on legitimate customers. The model is optimized for detecting fraudsters responsible for significant losses, contributing to enhanced risk management.

