# 🏦 Banking Risk Analysis – Customer Risk & Loan Exposure  

Analyzing customer credit risk and loan exposure to identify high-risk customer segments and provide actionable insights using **SQL, Python, and Power BI**.  

---

## 📑 Table of Contents
- [📌 Overview](#-overview)  
- [❓ Business Problem](#-business-problem)  
- [🗄️ Dataset](#%EF%B8%8F-dataset)  
- [🛠️ Tools & Technologies](#%EF%B8%8F-tools--technologies)  
- [📂 Project Structure](#-project-structure)  
- [🧹 Data Cleaning & Preparation](#-data-cleaning--preparation)  
- [🔎 Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)  
- [📊 Research Questions & Key Findings](#-research-questions--key-findings)  
- [📈 Dashboard](#-dashboard)  
- [⚙️ How to Run This Project](#%EF%B8%8F-how-to-run-this-project)  
- [✅ Final Recommendations](#-final-recommendations)  
- [👤 Author & Contact](#-author--contact)  

---

## 📌 Overview  
This project evaluates customer risk exposure and loan dynamics to help banks understand **which customer segments are most likely to default**. It follows a full analytics workflow: **data extraction (SQL) → EDA & hypothesis testing (Python) → dashboarding (Power BI).**  

---

## ❓ Business Problem  
Banks face challenges in managing **credit risk** across different customer segments. This project aims to:  
- Identify which **occupations, age groups, and income bands** are most risky  
- Compare **loans and credit card balances** across risk categories  
- Assess risk differences across **loyalty tiers (Platinum, Gold, Silver, Jade)**  
- Identify the **Top 10 riskiest customers** driving exposure  
- Provide **data-driven insights for monitoring & decision-making**  

---

## 🗄️ Dataset    

Data was pulled from a **MySQL database** into Python for analysis.  
It includes customer demographics, loans, credit balances, and risk scores, with derived fields such as:  
- **High Risk flag** (Risk Weighting ≥ 4)  
- **Risk Exposure Score** = (Bank Loans + Credit Balance) × Risk Weighting  

---

## 🛠️ Tools & Technologies  
- **SQL (MySQL)** → Data extraction  
- **Python (Pandas, Matplotlib, Seaborn, SciPy, Statsmodels)** → EDA & hypothesis testing  
- **Power BI** → Interactive dashboards (KPIs, slicers, heatmaps, charts)  
- **GitHub** → Version control & project documentation  

---

## 📂 Project Structure  
```
banking-risk-analysis/
│
├─ notebooks/
│ └─ banking_risk_analysis.ipynb           # Python analysis & EDA
│
├─ dashboard/
│ └─ Risk_Analysis_Dashboard.pbix          # Power BI dashboard file
│
├─ data/
│ └─ Banking_sample.csv                    # Sample dataset 
│
├─ images/
│ ├─ risk_overview.png                     # Page 1 dashboard
│ ├─ customer_segments.png                 # Page 2 dashboard
│
├─ requirements.txt                        # Python dependencies
└─ README.md
```

---

## 🧹 Data Cleaning & Preparation 

- Removed duplicates, invalid values (e.g., negative loans)  
- Created **age groups** and **income bands**  
- Encoded categorical features (occupation, nationality, loyalty tier)  
- Generated derived metrics: `High Risk`, `Risk Exposure Score`  

---

## 🔎 Exploratory Data Analysis (EDA)  

**Sample Visuals:**  

📊 Average Loan vs Credit Card Balance by Risk Category  
![Risk vs Exposure](images/avg_loan_vs_risk.png)  
![Risk vs Exposure](images/avg_credit_vs_risk.png)  

📊 Top 5 Occupations with Highest Average Risk  
![Occupation Risk](images/occupation_vs_risk.png)  

---

## 📊 Research Questions & Key Findings  

1. **Which occupations and age groups tend to fall in higher risk brackets?**  
   → Certain job roles and middle-aged groups had higher average risk.  

2. **Is there a difference in risk between male and female customers?**  
   → Minimal differences; gender is not a strong predictor.  

3. **Do high-risk customers hold more loans compared to low-risk customers?**  
   → Yes, loan size increases significantly with risk weighting.  

4. **Does higher loyalty classification (Platinum, Gold) align with lower risk?**  
   → Yes, Jade tier is associated with higher-risk loans.  

5. **Who are the Top 10 riskiest customers by exposure?**  
   → A small group of customers contribute **~2.5% of total exposure**.  

---

## 📈 Dashboard  

### 🔹 Page 1: Risk Overview  
![Risk Overview](images/Risk Overview.png)  
- KPIs: Total Customers, % High Risk, Avg Loan (High vs Low Risk), Avg Credit Balance  
- Risk distribution by **weighting, age group, occupation**  
- Loan vs Credit balance by risk  

### 🔹 Page 2: Customer Segments  
![Customer Segments](images/Customer Segments.png)  
- Risk & loan breakdown by **loyalty tier**  
- Heatmap: Loans by **Risk × Loyalty**  
- % High-Risk Customers by **Income Band** and **Nationality**  
- Top 10 Riskiest Customers table  

---

## ⚙️ How to Run This Project  

1. **Clone the repository:**  
   ```
   git clone https://github.com/yourusername/banking-risk-analysis.git
   cd banking-risk-analysis
 ```
2. **Install dependencies:**  
 ```
pip install -r requirements.txt
 ```
3. **Run Jupyter Notebook:**
 ```
notebooks/banking_risk_analysis.ipynb
 ```
4. **Open Power BI dashboard:**
```
dashboard/Risk_Analysis_Dashboard.pbix
```

---

✅ Final Recommendations

- Monitor high-income and Jade tier customers closely  
- Use risk-weighting + loan exposure for early-warning systems  
- Diversify loan portfolios to reduce concentration risk  
- Combine demographics + financial behavior for better scoring models

---

👤 Author & Contact  

**Rajat Rawat**  
Data Analyst  
📧 Email: [rajatrawatofficial98@gmail.com]
🔗 [LinkedIn](https://www.linkedin.com/in/rajat-rawat-3791a422a/)   