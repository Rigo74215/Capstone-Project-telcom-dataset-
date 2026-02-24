# Capstone-Project-telcom-dataset-
# Analyzing Customer Behavior and Revenue Trends in a Telecom Company 📊📞

## Project Overview
This project focuses on understanding telecom customer behavior and revenue trends using descriptive statistics, statistical hypothesis testing, and machine learning (linear regression). By analyzing customer demographics, account information, and service usage patterns, this project aims to identify the primary factors influencing customer spending and to provide data-driven business recommendations to improve retention and revenue.

## Table of Contents
1. [Project Objectives](#project-objectives)
2. [Dataset](#dataset)
3. [Technologies & Tools](#technologies--tools)
4. [Project Workflow](#project-workflow)
5. [Key Findings & Insights](#key-findings--insights)
6. [Repository Structure](#repository-structure)
7. [How to Run](#how-to-run)

## Project Objectives
* **Data Understanding & Cleaning:** Handle missing values, address data types (e.g., `TotalCharges`), and encode categorical variables.
* **Exploratory Data Analysis (EDA):** Visualize spending behavior across different customer segments (e.g., Contract types).
* **Hypothesis Testing:** Statistically validate business assumptions regarding gender, contract types, and spending behaviors.
* **Regression Analysis:** Build a Linear Regression model to predict `MonthlyCharges` based on variables like `Tenure`, `Contract`, and `PaymentMethod`.
* **Business Strategy:** Translate statistical findings into actionable recommendations for the telecom business.

## Dataset
The project utilizes the **Telco Customer Churn** dataset (originally from Kaggle/IBM). Key features include:
* **Demographics:** `gender`, `SeniorCitizen`, `Partner`, `Dependents`
* **Account Info:** `tenure` (months with company), `Contract` (Month-to-month, One-year, Two-year), `PaymentMethod`
* **Financial Metrics:** `MonthlyCharges` ($), `TotalCharges` ($)

## Technologies & Tools
* **Language:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Statistical Analysis:** `scipy.stats` (ANOVA, Independent T-Tests)
* **Machine Learning:** `scikit-learn` (Linear Regression, Label Encoding, Metrics)
* **Environment:** Jupyter Notebook

## Project Workflow
1. **Data Preparation:** Blank spaces in `TotalCharges` were converted to nulls and dropped. Categorical features were encoded using `LabelEncoder`.
2. **EDA:** Histograms, count plots, and boxplots were generated to map the distribution of revenue against contract terms.
3. **Hypothesis Testing:**
   * *Hypothesis 1 (ANOVA):* Do customers with long-term contracts have higher total spending?
   * *Hypothesis 2 (T-Test):* Is there a significant difference in spending between male and female customers?
4. **Predictive Modeling:** A Multiple Linear Regression model was trained to predict `MonthlyCharges`. Evaluated using Mean Squared Error (MSE) and R-squared (R²) metrics. 

## Key Findings & Insights
* **Contract Length Dictates Value:** One-Way ANOVA testing confirmed a statistically significant difference in lifetime value (`TotalCharges`) across contract types. Two-year contracts yield exponentially higher lifetime revenue compared to month-to-month contracts.
* **Gender Does Not Impact Spending:** An independent t-test revealed no statistically significant difference in monthly spending between male and female customers.
* **Predicting Revenue:** `Tenure` has a positive correlation with monthly charges, indicating that loyal customers tend to upgrade their services or add premium features over time.
* **Actionable Recommendations:** * Incentivize Month-to-Month customers to upgrade to 1-year or 2-year contracts.
  * Target high-tenure customers with premium service upsells.
  * Offer discounts for customers utilizing automatic billing (Credit Card/Bank Transfer) to stabilize revenue compared to Electronic Check users.

## Repository Structure
```text
├── Data/
│   ├── Telcom-data.csv             # Original dataset
│   └── Cleaned_Telcom_data.csv     # Processed dataset
├── Notebooks/
│   └── Telecom_Analysis.ipynb      # Main Jupyter Notebook with code and outputs
├── Presentations_and_Reports/
│   ├── Capstone_Report.pdf         # Final written business report
│   └── Capstone_Slides.pptx        # Presentation slides summarizing findings
└── README.md                       # Project documentation
