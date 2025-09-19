# Bank Marketing Prediction using Logistic Regression

This project implements a **Logistic Regression model** to predict whether a bank customer will **subscribe to a term deposit** based on their demographic and campaign-related features. It also allows **user input prediction** interactively.

---

## Table of Contents

- [Dataset](#dataset)  
- [Features](#features)  
- [Requirements](#requirements)  
- [Setup](#setup)  
- [Usage](#usage)  
- [Sample Input](#sample-input)  
- [Output](#output)  
- [Notes](#notes)  

---

## Dataset

The dataset used in this project is the **Bank Marketing Dataset** from Kaggle:  
[Bank Marketing Dataset](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset)

- **File name:** `bank.csv`  
- **Target variable:** `deposit` (`yes` = 1, `no` = 0)  
- **Number of rows:** 45,211  
- **Number of features:** 16 explanatory variables

---

## Features

| Feature | Description |
|---------|-------------|
| age | Age of the client |
| job | Type of job |
| marital | Marital status |
| education | Education level |
| default | Has credit in default? (yes/no) |
| balance | Average yearly balance (numeric) |
| housing | Has housing loan? (yes/no) |
| loan | Has personal loan? (yes/no) |
| contact | Contact communication type |
| month | Last contact month of year |
| day_of_week | Last contact day of the week |
| campaign | Number of contacts performed during this campaign |
| pdays | Days since client was last contacted (-1 if never) |
| previous | Number of contacts performed before this campaign |
| poutcome | Outcome of the previous campaign |

---

## Requirements

- Python 3.x  
- Packages: `pandas`, `scikit-learn`

Install packages using:

```bash
pip install pandas scikit-learn
```

---

## Setup

1. Download the **`bank.csv`** dataset from Kaggle and place it in the same folder as the script.  
2. Run the Python script:

```bash
python bank_logistic_user_input.py
```

---

## Usage

1. The script trains a **Logistic Regression model** on the dataset.  
2. After training, it prompts you to **enter customer details**.  
3. It predicts whether the customer is likely to subscribe to a term deposit and displays the **probability**.

---

## Sample Input

```
Age: 35
Job: management
Marital: married
Education: tertiary
Default Credit? (yes/no): no
Balance: 1500
Housing Loan? (yes/no): yes
Personal Loan? (yes/no): no
Contact Type (cellular, telephone, unknown): cellular
Month (jan, feb, mar, ... , dec): may
Day of Week (mon, tue, wed, thu, fri): wed
Number of Contacts in this Campaign: 2
Days since client was last contacted (-1 if never): -1
Number of contacts before this campaign: 0
Outcome of Previous Campaign (success, failure, other, unknown): unknown
```

---

## Output

Example prediction result:

```
--- Prediction Result ---
❌ The customer is NOT likely to subscribe. (Probability: 37.85%)
```

> ✅ The probability will vary depending on the logistic regression model training.

---

## Notes

- The script automatically **one-hot encodes** categorical features to match training columns.  
- Input values must match the **dataset categories** for accurate predictions.  
- You can modify the script to **loop and predict multiple customers** in one run.  

---

## Author

Narender Kashyap