# 💳 Financial Fraud Prediction Model (2026)

> Predicting which transactions are fraudulent using a dataset that contains financial, geographical and temporal information.

---

## 📑 Table of Contents
**Technical**
- [Introduction](#-introduction)
- [Objective](#-objective)
- [Dataset](#-dataset)
- [Technologies](#-technologies)
- [Methodology](#-methodology)
- [Results](#-results)
- [How to Run](#-how-to-run)

**Business**
- [Business Context](#-business-context)
- [Business Problem](#-business-problem)
- [Stakeholders](#-stakeholders)
- [Business Questions](#-business-questions)
- [Interpretation of Results](#-interpretation-of-results)
- [Key Insights](#-key-insights)
- [Recommendations](#-recommendations)
- [Expected Impact](#-expected-impact)

---

## 🧭 TECHNICAL SECTION

### 📌 Introduction
This project analyses a dataset with financial transactions information and focuses on building a machine learning model to detect fraudulent financial transactions. It combines statistical analysis and predictive modeling to address one of the main challenges in fraud detection: class imbalance.


### 🎯 Objective
Develop a classification model to predict fraudulent transactions with a recall rate with at least 98% to prevent losses.
Apply hypothesis testing and correlation analysis.
Handle imbalanced data effectively.

### 🗂️ Dataset
| Attribute | Detail |
|---|---|
| Source | Kaggel,  |
| Size | [rows x columns] |
| Time period | [e.g., Jan–Dec 2024] |
| Target variable | [e.g., `dropout` (binary)] |
| Key features | [list 5-8 most relevant columns] |
| Link | [dataset URL if public] |

### ⚙️ Technologies
- **Language:** Python
- **Data manipulation:** Pandas, NumPy, Scipy
- **Visualization:** Matplotlib, Seaborn
- **ML:** Scikit-learn
- **Environment:** Jupyter Notebook

### 🔬 Methodology
1. **Data Cleaning:** Look for duplicates, type fixes.
2. **EDA:** Distribution comparisson between fraudulent and not fraudulent transactions, correlations, class balance.
3. **Hypothesis Testing:** Transactions with KYC, OTP and at night 
4. **Train/Test Split:** 75/25
5. **Modeling:** Logistic Regression, Decision Tree Classifier, Random Forest Classifier, Gradient Boosting Classifier
6. **Evaluation Metrics:** Main metric Recall, because it measures how many real fraud cases existed.
7. **Model Selection:** Gradient Boosting Classifier because it was the best classifier of the unbalanced set.

### 🤖 Machine Learning Models
| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---|---|---|---|---|
| Logistic Regression | 0.8648 | 0.8104 | 0.9524 | 0.8757 | 0.8771 |
| Decision Tree       | 0.8829 | 0.8107 | 0.9990 | 0.8951 | 0.8834 |
| Random Forest       | 0.8801 | 0.8107 | 0.9919 | 0.8922 | 0.8839 |
| Gradient Boosting   | 0.8832 | 0.8107 | 0.9999 | 0.8954 | 0.8843 |

**Best model:** [name] — [1-2 sentences on why it was selected: performance, interpretability, business fit]

### 📊 Results
Gradient Boosting Classifier model achieved the best Recall metric 0.9999. Feature importance analysis showed that main feature to predict fraudulent transaction was the hour.

### 🚀 How to Run
```bash
# Clone the repository
git clone [https://github.com/jpcampos04/2604_predictive_model_financial_fraud.git]
cd [2604_predictive_model_financial_fraud]

# Run the notebook
jupyter notebook 2604_predictive_model_financial_fraud.ipynb
```

---

## 💼 BUSINESS SECTION

### 🏢 Business Context
The client is a retail chain with an online presence and locations in various cities. The chain is facing losses due to fraudulent transactions so is looking for a predictive model that can detect the financial fraud. 

### ❗ Business Problem
The retail chain faces fraudulent transactions amounting to around 9%, resulting in a loss of profits.

### 👥 Stakeholders
| Stakeholder | Interest / What they need from this analysis |
|---|---|
| Financial officer | Reduce losses from fraudulent transactions |
| Tellers and platform managers | Detecting suspicious transactions |

### ❓ Business Questions
- What is the probability of fraud occuring on an account with KYC?
- What is the probability of fraud in an OTP transaction?
- What is the probability of fraud occuring at night?
- Does the fraud occur on a specific day?

### 🔎 Interpretation of Results
The models that exceeded the expected 98% range were Gradient Boosting, Random Forest, and Decision Tree; all surpassed 99%, with Gradient Boosting performing the best—though it was the slowest—while Decision Tree was the fastest of the three.

### 💡 Key Insights
- **Insight 1:** Fraud is directly related to the time of day, occurring more frequently at night.
- **Insight 2:** Fraud occurs regularly during the week and decreases on Saturdays and Sundays.
- **Insight 3:** Transactions involving OTP and KYC were not significant factors in the fraud cases.

### ✅ Recommendations
1. Staff responsible for monitoring transactions should be alerted to the rise in nighttime transaction fraud.
2. Staff should be aware of the days when fraud is most common.
3. Although OTP and KYC are important, they do not play a significant role in fraudulent transactions.

### 📈 Expected Impact
By implementing the model that detects approximately 99% of fraudulent transactions—and considering that the average transaction is around $2,022—the reduction in losses amounts to $180,160,200.
