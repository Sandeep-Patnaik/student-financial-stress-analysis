# Student Spending & Financial Stress Analysis

## Business context
This project explores how student income, financial aid, essential expenses, and discretionary spending relate to a rule-based financial-stress label. The goal is to identify patterns that could inform student budgeting and financial-aid product ideas.

## Dataset
- **Source:** Student Spending Habits dataset (Kaggle; add the exact dataset URL for reproducibility)
- **Approximate size:** 1,000 students
- **Fields:** monthly income, financial aid, expense categories, and student demographics such as age and year of study

## Methodology

### Financial-stress rule
A student is labelled **financially stressed** when essential expenses exceed 70% of effective income:

`effective income = monthly income + financial aid`

A sensitivity analysis compares 60%, 70%, and 80% thresholds.

### Expense groups
- **Essential:** housing, food, transportation, health and wellness, books and supplies
- **Non-essential:** entertainment, personal care, technology, miscellaneous spending

Income bands are formed using quantile-based segmentation. Students are also compared by academic year and stress label.

## Findings recorded in the analysis
- Approximately **79%** of students meet the selected 70% threshold.
- The share labelled stressed decreases as income rises, but more than half of the highest-income group is still labelled stressed.
- The stressed share rises from freshman to senior year in this dataset.
- Average non-essential spending is reported as similar between the two groups, while essential spending is higher among the stressed group.

These are descriptive findings from the analyzed dataset, not evidence that income or academic year causes financial stress.

## Methodological limitation to keep in mind
Because the stress label is *defined using essential expenses divided by effective income*, finding higher essential expenses among stressed students is partly built into the label itself. That comparison is not an independent validation of what causes stress. Stronger follow-up analysis could use a separate outcome measure, test alternative definitions, and examine how results change across the 60%, 70%, and 80% thresholds.

The dataset is observational; the results should not be generalized to all university students without checking how the sample was collected and whether it is representative.

## Product implications to explore
- Improve visibility into essential costs and available financial aid.
- Test early-warning alerts when essential costs take up a large share of effective income.
- Explore cost-support and budgeting features without assuming discretionary spending is the main problem.

These are hypotheses for product exploration, not proven interventions.

## Tools and techniques
- Python, Pandas, NumPy, Matplotlib
- Data cleaning and exploratory data analysis
- Feature engineering, quantile-based segmentation, sensitivity analysis

## Reproducibility
Open `Notebook/Analysis.ipynb` and run the analysis with the dataset stored in the repository's `Data/` directory. Add the exact upstream dataset URL and document any preprocessing needed to reproduce the notebook outputs.

## Author
Sandeep Patnaik
