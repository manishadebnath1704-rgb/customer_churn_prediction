# Customer Churn Prediction

A machine learning project that predicts which telecom customers are likely to leave (churn), and suggests how a company can retain them.

## Dataset
Telco Customer Churn dataset (IBM sample data, from Kaggle): 7,043 customers and 21 columns covering services, account details and demographics.

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, Google Colab

## What I Did
1. Cleaned the data (fixed `TotalCharges` and handled missing values)
2. Explored the data with charts to see why customers leave
3. Encoded categorical variables and split the data into train and test sets
4. Handled class imbalance (only about 1 in 4 customers churns)
5. Trained and compared Logistic Regression, Random Forest and XGBoost
6. Evaluated with accuracy, precision, recall, F1-score, ROC-AUC and confusion matrices
7. Identified the factors linked to churn
8. Grouped customers into Low, Medium and High risk for retention planning

## Results

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |

| Logistic Reg (no balance) | 0.807 | 0.658 | 0.567 | 0.609 | 0.842 |
| Random Forest (no balance) | 0.790 | 0.634 | 0.495 | 0.556 | 0.826 |
| Logistic Reg (balanced) | 0.739 | 0.505 | 0.781 | 0.613 | 0.841 |
| Random Forest (balanced) | 0.789 | 0.631 | 0.497 | 0.556 | 0.825 |
| XGBoost (balanced) | 0.754 | 0.525 | 0.781 | 0.628 | 0.836 |

- Balancing the classes raised Logistic Regression recall from 0.567 to 0.781, so it catches many more churners.
- Logistic Regression had the best ROC-AUC. XGBoost had the best F1-score among the balanced models.

## Key Findings
- Customers on **month-to-month contracts** churn far more than those on one- or two-year contracts.
- **Short tenure** and **Fiber optic internet** are linked to higher churn.
- Longer contracts and online security are linked to lower churn.

## Business Use
Customers marked **High risk** churned 73% of the time, compared with 13% for **Low risk**. A retention team can contact high-risk customers first with offers, and encourage month-to-month customers to move to longer contracts.

## Limitations and Future Work
Tune hyperparameters, try SMOTE, build a full pipeline, and deploy the model with Streamlit.

## How to Run
1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
2. Open `Customer_Churn_Prediction.ipynb` in Google Colab
3. Upload the CSV file and run all cells

## Author
Manisha Debnath
