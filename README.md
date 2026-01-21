\# Car Insurance Claims Prediction



\## Project Overview

This project aims to predict whether a policyholder will file a car insurance claim. Using historical data on policyholders, vehicles, and driving behavior, a machine learning model is trained to assess claim risk. This helps insurance companies with risk profiling, pricing strategies, and proactive claim management.



---



\## Dataset

The dataset contains information about policyholders, their vehicles, and claim history. Key columns include:



\- `AGE`, `INCOME`, `HOMEKIDS`, `YOJ` – Personal and financial info  

\- `CAR\_TYPE`, `CAR\_USE`, `BLUEBOOK`, `CAR\_AGE`, `RED\_CAR` – Vehicle information  

\- `MVR\_PTS`, `REVOKED`, `OLDCLAIM`, `CLM\_FREQ` – Driving and claim history  

\- `CLAIM\_FLAG` – Target variable (1 if a claim was filed, 0 otherwise)  

\- `URBANICITY`, `GENDER`, `EDUCATION`, `OCCUPATION`, `MSTATUS`, `PARENT1` – Demographic and social information  



---



\## Methodology



\### 1. Data Cleaning \& Preprocessing

\- Removed irrelevant columns (`ID`, `BIRTH`, `CLAIM\_AMT`)  

\- Handled missing values for both numeric and categorical columns  

\- Encoded categorical variables using Label Encoding and One-Hot Encoding  

\- Scaled numerical features using StandardScaler  



\### 2. Handling Class Imbalance

\- The dataset has significantly fewer claim cases (class imbalance)  

\- SMOTE (Synthetic Minority Over-sampling Technique) was applied to training data to generate synthetic minority class samples  



\### 3. Model Training

\- Logistic Regression was selected as the baseline model for its simplicity and interpretability  

\- Probability threshold tuning was performed to maximize the F1-score  



\### 4. Evaluation

\- Metrics used:

&nbsp; - Accuracy  

&nbsp; - Precision, Recall, F1-score  

&nbsp; - ROC-AUC  

&nbsp; - Confusion Matrix  

\- Results were evaluated on a held-out test set  



---



\## Results Summary

\- Logistic Regression achieved an optimized F1-score after threshold tuning  

\- SMOTE improved the model’s ability to identify claim cases  

\- ROC-AUC indicates good separation between claim and non-claim classes  

\- The model balances precision and recall for imbalanced data  



---



\## Business Interpretation

\- Policyholders with prior claims (`OLDCLAIM`, `CLM\_FREQ`) are more likely to file future claims  

\- Driving history variables (`MVR\_PTS`, `REVOKED`) significantly impact claim probability  

\- Urban drivers show a higher likelihood of filing claims  

\- This model can help insurers with risk-based pricing, underwriting decisions, and proactive claim prevention  



---



\## Tools \& Technologies

\- Python 3  

\- Jupyter Notebook  

\- Pandas, NumPy  

\- Scikit-learn  

\- imbalanced-learn (SMOTE)  

\- Seaborn, Matplotlib  



---



\## How to Run

1\. Clone the repository  

2\. Install required packages:

```bash

pip install -r requirements.txt





