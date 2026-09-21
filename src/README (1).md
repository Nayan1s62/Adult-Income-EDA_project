# Adult Income Data Cleaning and EDA

## About the Project

This project is based on the UCI Adult Income dataset. I used Python to clean the dataset and perform exploratory data analysis (EDA).

The main purpose of the project is to explore how factors such as education, age, occupation, employment type, working hours, and other characteristics are related to income.

The analysis mainly looks at people with income above $50K.

---

## Problem Statement

The dataset contains information about people from census records, including their education, job, age, working hours, and income.

The project tries to answer questions such as:

- Does education level have a relationship with income?
- How does income vary across different age groups?
- Is income different across occupations?
- How does employment type relate to income?
- Are working hours different between income groups?
- How do capital gains and losses vary with income?

---

## Dataset

The dataset used in this project is the **UCI Adult Income Dataset**.

It contains demographic and employment-related information along with an income category.

### Columns Used

- Age
- Employment Type
- Census Weight
- Education Level
- Education Level Number
- Marital Status
- Job Occupation
- Household Relationship
- Race Category
- Sex
- Capital Gain Amount
- Capital Loss Amount
- Weekly Work Hours
- Country of Origin
- Income Category

Additional columns were created during the cleaning and analysis process.

---

## Data Cleaning

Before starting the analysis, the raw dataset was cleaned.

The main steps were:

1. Loaded `adult.data` and `adult.test`.
2. Combined the two datasets.
3. Added a column to identify the original train/test source.
4. Removed extra spaces from text values.
5. Changed `?` values to missing values.
6. Replaced missing values in some categorical columns with `Unknown`.
7. Cleaned the income column.
8. Converted numeric columns to numeric data types.
9. Removed invalid age values.
10. Removed impossible weekly working-hour values.
11. Created a `high_income_flag` column.
12. Created age groups.
13. Created weekly working-hour groups.
14. Calculated net capital amount.
15. Renamed the columns to make them easier to understand.
16. Saved the cleaned dataset as a CSV file.

---

## EDA Performed

After cleaning the data, I performed different types of analysis.

### Basic Analysis

- Dataset size
- Data types
- Missing values
- Duplicate records
- Income distribution
- Age distribution
- Education distribution
- Weekly working hours

### Income Analysis

I compared the income groups based on:

- Education
- Age group
- Sex
- Employment type
- Occupation
- Weekly working hours
- Capital gain and loss

### Visualizations

The project contains different charts such as:

- Income distribution
- Income proportion
- Income rate by education
- Income rate by age group
- Income rate by sex
- Income rate by employment type
- Income rate by occupation
- Working hours by income
- Capital gain distribution
- Age vs working hours
- Education vs income
- Income rate by working-hour group
- Education and income by sex
- Correlation heatmap
- EDA dashboard

---

## Project Structure

```text
Adult_Income_EDA_Project/
│
├── data/
│   ├── adult.data
│   ├── adult.test
│   └── adult_income_cleaned.csv
│
├── reports/
│   ├── tables/
│   │   ├── income_summary.csv
│   │   └── education_income_summary.csv
│   │
│   ├── charts/
│   │   ├── 01_basic_overview.png
│   │   ├── 02_income_proportion.png
│   │   ├── 03_income_rate_by_education.png
│   │   └── ...

│   │
│   ├── cleaning_log.csv
│   │
│   └── reports/
│       ├── Adult_Income_EDA_Report.docx
│       └── Adult_Income_EDA_Report.pdf
│
├── src/
│   ├── Data Cleaning.ipynb
│   ├── Data Analysis.ipynb
│   └── build_pdf_report.py
│
├── README.md
└── requirements.txt