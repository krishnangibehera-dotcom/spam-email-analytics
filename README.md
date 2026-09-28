# Spam Email Analytics & Classification

An end-to-end portfolio project combining exploratory data analysis, NLP-based text classification, model evaluation, and a Power BI-ready output.

## Objective
Analyze a labeled email/SMS message dataset to identify patterns associated with spam messages and build machine-learning models that classify messages as spam or legitimate.

## Tools
Python · Pandas · NumPy · Matplotlib · Scikit-learn · TF-IDF · Power BI (dashboard extension)

## Workflow
1. Data loading and validation
2. Duplicate and missing-value handling
3. Exploratory data analysis
4. Text and message-level feature engineering
5. TF-IDF vectorization
6. Logistic Regression, Multinomial Naive Bayes and Linear SVM
7. Accuracy, precision, recall and F1-score comparison
8. Confusion matrix analysis
9. Export of a Power BI-ready analysis dataset

## Dataset
The supplied `mail_data.csv` contains 5,572 raw messages with `Category` and `Message`. Exact duplicate rows are removed during cleaning before modeling.

## Model results
Using an 80/20 stratified train-test split with `random_state=42`:

| Model | Accuracy | Precision | Recall | F1 |
|---|---:|---:|---:|---:|
| Logistic Regression | 0.958 | 0.989 | 0.672 | 0.800 |\n| Multinomial Naive Bayes | 0.955 | 1.000 | 0.641 | 0.781 |\n| Linear SVM | 0.981 | 0.958 | 0.883 | 0.919 |\n
The model selected by F1 score in this run is **Linear SVM**.

## Power BI extension
The notebook exports `outputs/spam_email_powerbi_data.csv`. Import this file into Power BI to build KPI cards, class-distribution visuals, message-length analysis, word-count comparisons and prediction breakdowns. See `dashboard/POWER_BI_GUIDE.md`.

## Structure
```text
spam-email-analytics/
├── data/mail_data.csv
├── notebooks/Spam_Email_Analytics_Classification.ipynb
├── outputs/
├── dashboard/POWER_BI_GUIDE.md
├── README.md
└── requirements.txt
```

## Run locally
```bash
pip install -r requirements.txt
jupyter notebook
```

Open `notebooks/Spam_Email_Analytics_Classification.ipynb`.

## Portfolio note
This repository contains a fresh notebook implementation using the supplied dataset. The analysis, feature engineering, model comparison, evaluation and visualizations are generated within this project.
