
# Optimizing Loan Approvals: A Decision Tree Approach to Minimizing Delinquency Risk

---

## Introduction & Background

DRS Bank faces a growing challenge with Non-Performing Assets (NPAs) from individual borrowers. To address this, the Chief Risk Officer launched a project to enhance loan approval processes. The goal is to pinpoint factors driving loan delinquency and establish a data-driven method to reduce defaults.

For a comprehensive look at the code and detailed analysis behind this case study, please refer to the **`Loan Delinquent.Rmd`** file in this repository.

## Problem Statement

Non-performing loans severely impact a lending institution's financial health. Proactive identification of at-risk borrowers is crucial for profitability and effective credit risk management. This study aims to:

* Analyze the key drivers of loan delinquency.
* Develop a robust predictive model to classify borrowers based on their likelihood of default.

---

## Scope of this Study

This analysis focuses on:

* Exploring the relationships between various borrower attributes (e.g., FICO score, loan term, gender) and their impact on delinquency rates.
* Constructing a **decision tree model** to predict loan delinquency with high accuracy.
* Generating actionable insights to optimize loan approval strategies, ensuring they align with the bank's risk management objectives.

---

## Dataset Overview

The analysis utilizes the `Loan_Delinquent_Dataset.csv` dataset, comprising 11,548 records with the following attributes:

* **isDelinquent**: Loan delinquency status (1 = Delinquent, 0 = Not Delinquent). This is our target variable.
* **term**: The duration of the loan (e.g., 36 months, 60 months).
* **gender**: The borrower's gender.
* **purpose**: The stated reason for the loan (e.g., House, Car, Medical, Personal).
* **home_ownership**: The borrower's housing status (e.g., Rent, Mortgage, Own).
* **age**: The borrower's age group (e.g., >25, 20-25).
* **FICO**: The borrower's FICO credit score range (e.g., 300-500, >500).

---

## Key Findings

### Loan Delinquency Distribution

Approximately **67% of borrowers in the dataset are delinquent**. This high proportion indicates a significant risk prevalence within the loan portfolio, highlighting the urgent need for improved risk assessment.

### FICO Score Distribution by Loan Delinquency

Borrowers with **FICO scores in the 300-500 range are significantly more likely to be delinquent**. Conversely, those with FICO scores **above 500 exhibit a noticeably lower risk** of default. This makes FICO score a critical predictor of delinquency.

### Loan Term Distribution by Loan Delinquency

Delinquency rates are **notably higher for 36-month loans** compared to 60-month loans. This suggests that shorter loan terms, despite seeming less risky, are associated with a greater likelihood of default in this dataset.

### Gender Distribution by Loan Delinquency

While the difference is slight, **male borrowers show a marginally higher likelihood of delinquency** compared to female borrowers.

---

## Decision Tree Analysis

The **decision tree model** developed for this analysis provides clear, interpretable rules that highlight the key factors influencing loan delinquency.

The model identifies important variables such as:

* **FICO Score**: This is the **most significant predictor** of delinquency, effectively categorizing borrowers into high- and low-risk groups.
* **Loan Term**: The term of the loan, particularly 36-month loans, shows a strong correlation with higher delinquency rates.
* **Gender**: Gender plays a role, with male borrowers showing a slightly elevated risk.

The final decision tree model demonstrates strong performance:

* **Training Accuracy: 85.08%**
* **Test Accuracy: 85.14%**

This consistent high accuracy across both training and test datasets confirms the model's robustness and its ability to generalize well to new, unseen data, providing reliable predictions of borrower delinquency.

---

## Recommendations

Based on the insights from this study, I recommend the following strategies to optimize loan approval processes and minimize delinquency risk:

* **Target High FICO Scores**: Prioritize loan approvals for borrowers with **FICO scores above 500**, as they exhibit significantly lower delinquency rates. This will directly contribute to minimizing risk.
* **Stricter Screening for 36-Month Terms**: Borrowers applying for **36-month term loans** show a delinquency rate of 70%. Consider implementing stricter screening criteria or potentially adjusting interest rates for these terms to offset the higher risk.
* **Prioritize Female Borrowers**: Given their lower delinquency rates, **female borrowers** can be strategically prioritized for lending opportunities.
* **Implement Automated Pre-screening**: Integrate the decision tree model into the loan approval workflow for **automated pre-screening**. This will enhance approval efficiency by quickly identifying high-risk applications.

---

Feel free to explore the `Loan Delinquent.Rmd` file to see the detailed code and steps that led to these findings!
```
