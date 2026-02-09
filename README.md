## HR Employee Prediction System (2025)
A data-driven HR system that integrates relational database management with machine learning models to support employee hiring decisions through both manual operations and predictive analytics.

**Context:** Data Science Tools course project (2025)

---

## Overview

This project implements an HR Employee Prediction System designed to combine structured data storage with supervised machine learning models for employment outcome prediction.

The system supports traditional HR database operations alongside AI-powered predictions, allowing structured employee data to be stored, analyzed, and used for classification-based hiring decisions. The focus of the project is on **end-to-end data handling**, from database design and preprocessing to model training, evaluation, and deployment-ready prediction workflows.

---

## System Architecture

The system is composed of three tightly integrated components:

- A **normalized SQLite database** for employee data storage
- A **data analysis and preprocessing pipeline** for feature preparation
- A **machine learning layer** for employee status prediction

This architecture reflects a practical data science workflow where persistent storage, analytics, and modeling coexist within a single system.

---

## Core Functionality

The system operates in two primary modes.

**Manual HR Mode** enables full control over employee records, including insertion, retrieval, update, and deletion of data stored in the relational database.

**AI-Powered HR Mode** allows trained machine learning models to be applied to candidate data in order to predict hiring outcomes without retraining, enabling repeated inference runs from saved models.

---

## Data Management

Employee data is stored in a structured SQLite database using a normalized schema. The design separates categorical attributes into lookup tables and models many-to-many relationships explicitly, ensuring scalability and data integrity.

The database supports large-scale imports from CSV files and is designed to handle tens of thousands of records efficiently.

---

## Data Processing Pipeline

Raw employee data undergoes a structured preprocessing workflow that includes:

- Missing value handling and duplicate removal  
- Outlier detection using the interquartile range (IQR) method  
- Encoding of categorical variables  
- Feature selection and transformation  
- Train–test splitting for model evaluation  

This pipeline ensures that the data used for modeling is clean, consistent, and suitable for supervised learning.

---

## Machine Learning Models

Three classification models are implemented and evaluated:

- Logistic Regression  
- Decision Tree Classifier  
- Random Forest Classifier  

Each model is trained using hyperparameter tuning via grid search and evaluated using standard classification metrics including accuracy, precision, recall, F1-score, ROC curves, and AUC values.

Trained models are persisted using joblib to enable reuse without retraining.

---

## Key Insights

Model evaluation indicates that technical skill indicators, professional background, previous salary, and age are among the strongest predictors of employment outcomes.

Tree-based models demonstrate improved performance and interpretability compared to linear approaches, particularly in capturing non-linear relationships between candidate attributes and hiring decisions.

---

## Visualization and Analysis

The system includes extensive exploratory data analysis and visualization, covering:

- Demographic distributions  
- Employment status by age, education, and geography  
- Skill distribution analysis  
- Correlation heatmaps for feature relationships  
- Regional comparisons by continent  

These visualizations support both model interpretation and data-driven HR insights.

---

## Tech Stack

Python, SQLite, pandas, NumPy, scikit-learn, matplotlib, seaborn, joblib, tabulate

---

## How to Run

```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib tabulate
