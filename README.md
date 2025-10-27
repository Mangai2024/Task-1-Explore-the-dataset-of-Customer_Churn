**README.md (Task 1 – Telco Customer Churn)**
# Task 1: Basic Exploration of Telco Customer Churn Dataset

## 📌 Objective
The goal of this task was to **explore the Telco Customer Churn dataset** using Python and Pandas.  
We checked the dataset’s **structure, summary statistics, and missing values** to understand its quality and prepare for cleaning.

---

## 📂 Dataset
- **Dataset**: Telco Customer Churn  
- **Source**: [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- **Rows**: 7043  
- **Columns**: 21  
- **Target Column**: `Churn` (Yes / No)

---

## 🔎 Steps Performed
1. **Loaded dataset with Pandas**
   ```python
   import pandas as pd
   df = pd.read_csv("Telco_Customer_Churn.csv")


Checked structure

Dataset shape → df.shape → (7043, 21)

Column names → df.columns

Data types and non-null values → df.info()

Preview of first rows → df.head()

Summary statistics

Numerical stats → df.describe()

Categorical stats → df.describe(include='object')

Unique values count → df.nunique()

Checked missing values

Missing per column → df.isnull().sum()

Percentage missing → (df.isnull().sum()/len(df))*100

Blank spaces check → (df == ' ').sum()

Duplicates → df.duplicated().sum()

📊 Findings

Dataset shape: 7043 rows × 21 columns

Target distribution: ~26.5% customers churned, ~73.5% did not.

TotalCharges column stored as string, needed conversion to numeric.

Some rows had blank values in TotalCharges.

No major duplicate rows found.

✅ Outcome

Gained a clear understanding of Telco Churn dataset structure.

Identified missing/blank values for cleaning in the next task.

