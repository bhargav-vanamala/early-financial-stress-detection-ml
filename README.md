# Early Financial Stress Detection using Machine Learning

## 📌 Project Overview
This project focuses on **early detection of financial stress** in customers using **real-world banking transaction data**.

Instead of reacting after a loan default occurs, the model identifies **risk signals before loan issuance** by analyzing historical customer behavior.

This project is designed as a **flagship portfolio project** for:
- Data Analyst  
- Data Scientist  
- Machine Learning Engineer roles  

---

## 🎯 Business Problem
Financial stress usually builds up gradually and is reflected in:

- 📈 Increasing transaction volatility  
- 📉 Declining account balances  
- 🔄 Irregular spending patterns  

Most traditional systems detect risk **after default**.

This project predicts **early warning signs**, enabling proactive actions such as:
- Risk-based credit limits  
- Early customer alerts  
- Preventive intervention strategies  

---

## 📊 Dataset (REAL DATA)
This project uses the **PKDD’99 Czech Banking Dataset**, a real-world anonymized financial dataset widely used in academic research and industry case studies.

### Data Tables Used
- **loan.csv** – Loan details and repayment status  
- **account.csv** – Customer account information  
- **trans.csv** – Historical transaction records  

✅ This is **real banking data**, not synthetic or mock data.

---

## 🧠 Target Definition
Loan status categories:
- **A** → Good loan  
- **B** → Bad loan  

Target variable:
- `target_bad = 1` → Financial stress  
- `target_bad = 0` → Healthy customer  

Only **completed loans** are used to ensure reliable labeling.

---

## ⚙️ Methodology & Approach

### 1️⃣ Data Cleaning & Validation
- Robust parsing of mixed date formats (`yymmdd`, `yyyymmdd`)
- Handling missing and mixed-type values
- Column validation to avoid silent errors

---

### 2️⃣ Time-Aware Feature Engineering (Key Strength)
To prevent **data leakage**, only **transactions occurring before the loan date** are used.

Engineered features include:
- Monthly transaction counts
- Cumulative transaction volume
- Balance volatility and trends
- Behavioral stability indicators

A **time-aware merge (`merge_asof`)** ensures realistic modeling.

---

### 3️⃣ Exploratory Data Analysis & Visualization
The notebook includes rich visualizations:
- Loan distribution over time
- Transaction frequency trends
- Balance fluctuation patterns
- Stress vs non-stress behavior comparisons
- Feature importance plots

All visuals are **business-focused and interpretable**.

---

## 🤖 Machine Learning Models
Multiple models are trained and evaluated:
- Logistic Regression (baseline)
- Random Forest
- Gradient Boosting

### Evaluation Metrics
- ROC–AUC
- Precision & Recall
- Confusion Matrix

Special focus is placed on **recall for financially stressed customers**, which is critical in risk detection.

---

## 📈 Key Insights
- Customers with **high transaction volatility** and **declining balances** show higher risk
- Temporal behavioral features outperform static attributes
- Time-aware modeling avoids overly optimistic results

---

## ⭐ Why This Project Stands Out
✔ Real banking dataset  
✔ Strong temporal modeling (no data leakage)  
✔ Advanced feature engineering  
✔ Business-driven insights  
✔ End-to-end ML pipeline  

This is **not a copied or Kaggle-style project**.

---

## 🛠 Tools & Technologies
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  

---

## ▶️ How to Run
1. Place `loan.csv`, `account.csv`, and `trans.csv` in the project folder  
2. Open `early_financial_stress_detection_ml.ipynb`  
3. Run all cells sequentially  

---

## 💬 Interview-Ready Explanation
**Where did the data come from?**

> “I used the PKDD’99 Czech Banking Dataset, a real-world financial dataset widely used in research and industry case studies.”

**What makes this project strong?**

> “It uses time-aware feature engineering to predict financial stress before loan issuance while strictly avoiding data leakage.”

---

## 👤 Author
**Bhargav Vanamala**  
GitHub: https://github.com/bhargav-vanamala
