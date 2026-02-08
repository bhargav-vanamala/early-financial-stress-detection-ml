Early Financial Stress Detection using Machine Learning
📌 Project Overview

This project focuses on early detection of financial stress in customers using real-world banking transaction data.
Instead of reacting after a loan default occurs, the model identifies risk signals before loan issuance by analyzing historical customer behavior.

This project is designed as a flagship portfolio project for Data Analyst / Data Scientist / Machine Learning roles.

🎯 Business Problem

Financial stress usually builds up gradually and is reflected in:

Increasing transaction volatility

Declining account balances

Irregular spending patterns

Most traditional systems detect risk after default.
This project predicts early warning signs, enabling proactive actions such as:

Risk-based credit limits

Early customer alerts

Preventive intervention strategies

📊 Dataset (REAL DATA)

This project uses the PKDD’99 Czech Banking Dataset, a real anonymized financial dataset widely used in academic research and industry case studies.

Data tables used:

loan.csv – loan details and repayment status

account.csv – customer account information

trans.csv – historical transaction data

✔️ This is real-world banking data, not synthetic or sample data.

🧠 Target Definition

Loan status categories:

A → Good loan

B → Bad loan

Target variable:

target_bad = 1 → Financial stress / risky customer

target_bad = 0 → Healthy customer

Only completed loans are used to avoid ambiguous labeling.

⚙️ Methodology & Key Techniques
1️⃣ Data Cleaning & Validation

Robust parsing of mixed date formats (yymmdd, yyyymmdd)

Handling missing and mixed-type values

Column validation to prevent silent failures

2️⃣ Time-Aware Feature Engineering (Core Strength)

To prevent data leakage, the model strictly uses only transaction data available before the loan date.

Engineered features include:

Monthly transaction counts

Cumulative transaction volume

Balance volatility and trends

Behavioral stability indicators

A time-aware merge (merge_asof) is used to attach the last known customer behavior prior to loan issuance.

3️⃣ Exploratory Data Analysis & Visualization

The notebook includes rich visual analysis:

Loan distribution over time

Transaction frequency trends

Balance fluctuation patterns

Stress vs non-stress behavior comparisons

Feature importance visualizations

All plots are business-interpretable, not just technical.

🤖 Machine Learning Models

Multiple models are trained and evaluated:

Logistic Regression (baseline)

Random Forest

Gradient Boosting

Evaluation metrics:

ROC–AUC

Precision & Recall

Confusion Matrix

Special emphasis is placed on recall for financially stressed customers, which is critical in real-world financial risk detection.

📈 Key Insights

Customers with high transaction volatility and declining balances show significantly higher risk

Temporal behavioral features outperform static customer attributes

Time-aware modeling avoids overly optimistic and biased results

⭐ Why This Project Stands Out

✔ Uses real banking data
✔ Prevents data leakage through temporal constraints
✔ Advanced feature engineering rarely seen on GitHub
✔ Strong business framing and interpretability
✔ End-to-end ML pipeline

This is not a Kaggle-style or copied project.

🛠 Tools & Technologies

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

▶️ How to Run

Place loan.csv, account.csv, and trans.csv in the project directory

Open early_financial_stress_detection_ml.ipynb

Run cells sequentially from top to bottom
