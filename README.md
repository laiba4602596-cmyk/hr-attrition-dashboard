# HR Employee Attrition Dashboard

A data analyst portfolio project using Google Looker Studio to analyze employee attrition drivers.

## Business Question

A company wants to understand which departments, roles, or factors (overtime, tenure, satisfaction) are most associated with employees leaving, so it can focus retention efforts where they matter most. This dashboard analyzes 1,470 employee records to answer:

1. What is the company's overall attrition rate?
2. Which departments have the highest attrition?
3. Which job roles have the highest attrition?
4. Does working overtime correlate with higher attrition?
5. What do individual at-risk employee records look like?

## Data Source

The IBM HR Analytics Employee Attrition & Performance dataset, a well-known public dataset with 1,470 employee records covering demographics, compensation, satisfaction scores, and attrition status. Available on Kaggle: search "IBM HR Analytics Employee Attrition & Performance."

## Tools Used

- **Google Looker Studio** — dashboard building and calculated fields
- **Google Sheets** — data cleaning and preparation

## Dashboard

![HR Attrition Dashboard](dashboard-screenshot.png)

**Live interactive dashboard:** [View live dashboard](https://datastudio.google.com/reporting/b2581c42-f3f8-494f-a34a-835a18139d91)

## How to Reproduce

1. Download the dataset from Kaggle (https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset).
2. Import the CSV into Google Sheets.
3. Clean the data: remove duplicates, ensure numeric columns (Age, MonthlyIncome, YearsAtCompany, etc.) are formatted as Number and not Text.
4. Connect the sheet to Google Looker Studio.
5. Create a calculated field for Attrition Rate:
   ```
   COUNT(CASE WHEN Attrition = "Yes" THEN 1 END) / COUNT(Attrition)
   ```
6. Build scorecards, bar charts by department/role, and a filterable employee table using the steps above.

## Project Structure

```
hr-attrition-dashboard/
├── dashboard-screenshot.png   # Screenshot of the finished dashboard
└── README.md
```
