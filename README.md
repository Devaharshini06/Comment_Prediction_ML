# Comment Category Prediction 📊

> An NLP-based multi-class classification system for automatically categorizing user comments using text, engagement signals, and metadata.

## Overview

This project explores automated comment categorization using a combination of **Natural Language Processing, feature engineering, and machine learning**.

The objective was to determine whether user comments could be classified into predefined categories using both the textual content of the comment and additional metadata such as votes, emoticons, and other available features.

The project was developed as a machine learning experimentation pipeline, with multiple models compared using standard classification metrics.

---

## Dataset

The dataset contains:

- **198,000 training samples**
- **102,000 test samples**
- User comment text
- Upvotes and downvotes
- Emoticon-related features
- Additional metadata
- Target category labels

The training dataset contains **15 columns**, while the test dataset contains **14 columns**. 

The target variable contains four classes:

| Label | Training Samples | Proportion |
|------:|-----------------:|-----------:|
| 0 | 114,173 | 57.7% |
| 2 | 62,440 | 31.5% |
| 1 | 15,918 | 8.0% |
| 3 | 5,469 | 2.8% |

The class distribution is therefore highly imbalanced, making evaluation beyond simple accuracy important.

---

# 🔄 Machine Learning Pipeline

```text
Raw Dataset
     │
     ▼
Data Loading
     │
     ▼
Exploratory Data Analysis
     │
     ▼
Missing Value Analysis
     │
     ▼
Feature Engineering
     │
     ├───────────────┐
     ▼               ▼
Comment Text      Metadata
     │               │
     ▼               ▼
TF-IDF          Numerical/
Vectorization   Categorical Features
     │               │
     └───────┬───────┘
             ▼
      Feature Combination
             │
             ▼
      Model Training
             │
             ├── Logistic Regression
             ├── SVM
             ├── Naive Bayes
             ├── Random Forest
             ├── Gradient Boosting
             ├── LightGBM
             └── XGBoost
             │
             ▼
       Model Evaluation
             │
             ▼
     Best Model Selection
