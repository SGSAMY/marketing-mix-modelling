# Marketing Mix Modelling (MMM) - Budget Optimisation

# Marketing Mix Modelling (MMM) - Budget Optimisation

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=plotly&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Marketing Analytics](https://img.shields.io/badge/Marketing%20Analytics-0052CC?style=for-the-badge)
![MMM](https://img.shields.io/badge/Marketing%20Mix%20Modelling-008000?style=for-the-badge)

## Project Overview

This project demonstrates an end-to-end **Marketing Mix Modelling (MMM)** framework to evaluate the impact of marketing channels on revenue performance and support data-driven marketing investment decisions.

The project applies statistical modelling techniques to:

- Understand the relationship between marketing activity and revenue
- Estimate channel contribution
- Evaluate marketing efficiency through ROI analysis
- Simulate alternative budget allocation scenarios

The approach reflects how marketing analytics teams use MMM to support strategic planning and budget optimisation.

---

# Business Objective

Marketing teams invest across multiple channels including paid search, paid social, display advertising and email marketing.

The objective of this project is to answer:

- Which marketing channels are contributing most to revenue?
- How can marketing effectiveness be measured beyond last-click attribution?
- What is the estimated ROI of each channel?
- How can budget allocation scenarios be evaluated?

---

# Dataset

The dataset contains weekly marketing performance data covering **104 weeks**.

## Variables

| Variable | Description |
|---|---|
| Week | Weekly reporting period |
| Paid Search Spend | Investment in paid search advertising |
| Paid Social Spend | Investment in paid social advertising |
| Display Spend | Investment in display advertising |
| Email Sends | Email marketing activity volume |
| Promotion | Promotional campaign indicator |
| Seasonality Index | Seasonal demand factor |
| Revenue | Business outcome metric |

**Note:**  
The dataset is synthetic and created for portfolio demonstration purposes.

---

# Tools & Technologies

## Programming

- Python

## Data Analysis

- Pandas
- NumPy

## Visualisation

- Matplotlib

## Machine Learning

- Scikit-learn

## Development Environment

- Jupyter Notebook

---

# Project Methodology

## 1. Data Loading & Preparation

The project begins by loading weekly marketing performance data and validating the dataset structure.

Performed:

- Data ingestion
- Data type validation
- Missing value checks
- Duplicate record checks
- Dataset profiling

---

# 2. Exploratory Data Analysis (EDA)

Exploratory analysis was performed to understand:

- Revenue trends over time
- Marketing investment patterns
- Channel relationships
- Seasonal behaviour
- Correlation between marketing activity and revenue

Key visualisations include:

- Revenue trend analysis
- Marketing spend trends
- Revenue distribution
- Correlation analysis

---

# 3. Marketing Carryover Effect - Adstock Transformation

Marketing impact is not always immediate.

Customers may see advertising multiple times before converting.

To capture this behaviour, an adstock transformation was applied:

```
Adstock(t) = Spend(t) + Decay × Adstock(t-1)
```

This models the ongoing influence of previous marketing activity.

Example:

```
Current Week Spend
        +
Previous Marketing Effect
        ↓
Total Marketing Impact
```

---

# 4. Diminishing Returns - Saturation Transformation

Increasing marketing investment does not always create proportional revenue growth.

A saturation transformation was applied to represent diminishing returns.

This helps the model understand that:

- Initial investment may generate stronger returns
- Additional spend may produce lower incremental impact

This provides a more realistic representation of marketing response.

---

# 5. Marketing Mix Model (MMM)

A regression-based MMM model was developed to estimate the relationship between marketing drivers and revenue.

## Model Inputs

Marketing variables:

- Paid Search saturation effect
- Paid Social saturation effect
- Display saturation effect
- Email activity

Business variables:

- Promotion activity
- Seasonality index
- Month
- Quarter

## Target Variable

```
Revenue
```

The model estimates how different factors contribute to revenue performance.

---

# 6. Model Evaluation

The model performance was evaluated using:

## R² Score

Measures how much variation in revenue is explained by the model.

## MAE (Mean Absolute Error)

Measures average prediction error.

## RMSE (Root Mean Squared Error)

Measures prediction accuracy while giving more weight to larger errors.

Additional validation:

- Actual vs predicted revenue comparison

---

# 7. Channel Contribution Analysis

Model outputs were converted into estimated channel contribution values.

This provides a business interpretation of model results.

Example:

```
Marketing Channel
        ↓
Model Impact
        ↓
Estimated Revenue Contribution
```

This allows comparison of relative channel effectiveness.

---

# 8. Marketing ROI Analysis

Channel efficiency was calculated using:

```
ROI = Estimated Contribution / Marketing Spend
```

This provides insight into:

- Channel efficiency
- Investment effectiveness
- Potential optimisation opportunities

---

# 9. Budget Optimisation Scenario

A hypothetical budget allocation scenario was created using ROI-weighted channel allocation.

The scenario demonstrates how MMM insights can support:

- Marketing planning
- Investment scenario analysis
- Budget allocation discussions

Example workflow:

```
MMM Results
     ↓
Channel ROI
     ↓
Budget Scenario
     ↓
Investment Planning
```

---

# Project Outputs

The analysis generates the following output files:

```
output/

├── channel_contribution.csv
├── roi_analysis.csv
└── budget_optimisation.csv
```

---

# Key Insights

The project demonstrates how MMM can be used to:

- Evaluate marketing channel effectiveness
- Measure incremental marketing impact
- Incorporate advertising carryover effects
- Model diminishing returns
- Compare channel ROI
- Simulate budget allocation scenarios

---

# Limitations

This portfolio project has several limitations:

- Dataset is synthetic
- Limited number of external business variables
- Baseline regression-based MMM approach
- Fixed adstock and saturation parameters

A production MMM solution would typically include additional factors such as:

- Pricing changes
- Competitor activity
- Customer demand indicators
- Economic factors
- Product launches
- Advanced Bayesian MMM approaches

---

# Future Improvements

Potential enhancements:

- Automated adstock parameter optimisation
- Automated saturation curve tuning
- Bayesian Marketing Mix Modelling
- Marginal ROI optimisation
- Constrained budget optimisation
- Power BI executive dashboard
- Integration with cloud data platforms

---

# Repository Structure

```
marketing-mix-modelling

│
├── data
│   └── marketing_data.xlsx
│
├── notebooks
│   └── marketing_mix_modelling.ipynb
│
├── output
│   ├── channel_contribution.csv
│   ├── roi_analysis.csv
│   └── budget_optimisation.csv
│
├── README.md
└── .gitignore
```

---

# Author

**Satheesh Gurusamy**

Senior Data & Marketing Analytics Professional

Skills demonstrated:

- Marketing Analytics
- Customer Analytics
- SQL
- Python
- Power BI
- Data Modelling
- CRM Analytics
- Marketing Effectiveness Analysis
