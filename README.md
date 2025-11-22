# HR Employee Prediction System - 2025

## Academic Context
This project was developed as part of the "Data Science Tools" course (2025).

## Team Members

- Hamza Hussain Omran (22011501)
- Yasser Ashraf Mohammed (22010409)
- and more...

## Project Overview

This project implements an HR Employee Prediction System that combines database management with machine learning models to predict employee hiring outcomes. The system provides both manual HR operations and AI-powered prediction capabilities.

## Features

### Database Management
- SQLite database implementation for storing employee records
- Normalized database schema with multiple related tables
- CRUD operations (Create, Read, Update, Delete) for employee records
- Import functionality from CSV files
- Support for up to 50,000 employee records

### Data Analysis and Visualization
- Comprehensive Exploratory Data Analysis (EDA)
- Statistical analysis of employee attributes
- Distribution visualizations using histograms, bar plots, and pie charts
- Correlation heatmaps
- Country segmentation by continent
- Employment status analysis across different demographics

### Machine Learning Models
The system implements three classification models:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier

Each model includes:
- Hyperparameter tuning using GridSearchCV
- Performance metrics (Accuracy, Precision, Recall, F1-Score)
- ROC curves and AUC scores
- Confusion matrices
- Model persistence using joblib

### Data Preprocessing
- Handling missing values
- Duplicate removal
- Outlier detection and removal using IQR method
- Label encoding for categorical variables
- Feature selection and engineering
- Train-test split for model validation

## Database Schema

### Main Tables
- EmployeesRecords: Initial data import table
- Employees: Normalized employee information
- EducationLevels: Education level lookup table
- Genders: Gender lookup table
- MainBranches: Main branch lookup table
- Countries: Country lookup table
- Skills: Skills lookup table
- EmployeeSkills: Many-to-many relationship between employees and skills

## Key Attributes

Employee records include:
- Age
- Accessibility
- Education Level
- Gender
- Work Experience
- Mental Health Status
- Main Branch (Professional Developer status)
- Years of Coding
- Years of Professional Coding
- Country/Continent
- Previous Salary
- Computer Skills Count
- Employment Status (Target Variable)

## System Modes

### Manual HR Mode
- Add new employee records
- Retrieve employee information
- Update existing records
- Delete employee records
- View database records with pretty-printed tables

### AI-Powered HR Mode
- Select from trained machine learning models
- Input candidate information
- Receive hiring predictions (Accepted/Rejected)
- Multiple prediction runs without retraining

## Technical Stack

### Libraries and Frameworks
- sqlite3: Database management
- pandas: Data manipulation and analysis
- numpy: Numerical operations
- scikit-learn: Machine learning models and preprocessing
- matplotlib: Data visualization
- seaborn: Statistical visualizations
- joblib: Model persistence
- tabulate: Pretty-printing tables
- csv: CSV file handling

## Model Performance

The system evaluates models using:
- Accuracy Score
- Classification Report (Precision, Recall, F1-Score)
- Confusion Matrix
- ROC Curve
- AUC Score

Best performing features identified:
- Computer Skills
- Main Branch (Professional Developer status)
- Previous Salary
- Age
- Accessibility

## Data Processing Pipeline

1. Database initialization and CSV import
2. Data loading to DataFrame
3. Exploratory Data Analysis
4. Data preprocessing and cleaning
5. Feature encoding and selection
6. Outlier removal
7. Train-test split
8. Model training and evaluation
9. Model persistence
10. Prediction interface

## Usage

The system provides an interactive menu-driven interface:

1. Manual HR Mode: Perform CRUD operations on employee records
2. AI-Powered HR Mode: Use trained models for hiring predictions
3. Model Training: Select and train specific models
4. Exit: Close the application

## Data Source

The system uses employee data from Stack Overflow developer surveys, containing information about:
- Demographics
- Education background
- Professional experience
- Technical skills
- Employment status

## Visualization Capabilities

- Age distribution analysis
- Education level distribution
- Employment status by age groups
- Geographic distribution by continent
- Average computer skills by continent
- Employment percentage by continent
- Correlation heatmaps
- Feature distributions

## Model Saving and Loading

Trained models are saved using joblib for:
- Quick reloading without retraining
- Deployment in production environments
- Consistent predictions across sessions

## Requirements

- Python 3.x
- SQLite3
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- joblib
- tabulate

## Project Structure

- Copy_of_notebook_v_3_final.ipynb: Main analysis and database implementation
- Interactive_NEGEhr.ipynb: Interactive HR system implementation
- HR.db: SQLite database file
- stackoverflow_full.csv: Source data file
- EmployeesDB.jpg: Database schema diagram
- Model files: Saved trained models (.joblib)

## Future Enhancements

Potential improvements include:
- Web-based interface
- Real-time data updates
- Additional machine learning algorithms
- Deep learning integration
- Advanced feature engineering
- API development for external integrations
- Dashboard for analytics and reporting

## Conclusion

This HR Employee Prediction System demonstrates the integration of database management, data analysis, and machine learning to create a practical tool for HR decision-making. The system provides both manual control and automated predictions, making it suitable for various organizational needs.
