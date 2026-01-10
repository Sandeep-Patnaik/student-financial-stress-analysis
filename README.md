# Student Spending & Financial Stress Analysis

## Business Context
University students often experience financial stress, but it is unclear whether this stress is driven by discretionary overspending or unavoidable living expenses.  
Understanding the true drivers of financial stress is important for designing effective budgeting tools, financial aid programs, and student-focused fintech solutions.

This project analyzes student spending data to identify the primary contributors to financial stress and translate analytical findings into actionable product insights.

---

## Objective
The objectives of this project are to:
- Define a data-driven measure of financial stress
- Analyze how financial stress varies across income levels and academic years
- Compare spending behavior between financially stressed and non-stressed students
- Derive actionable recommendations for student-focused financial products

---

## Dataset Overview
- **Source:** Student Spending Habits dataset (Kaggle)
- **Size:** ~1000 students
- **Key Features:**
  - Monthly income and financial aid
  - Detailed expense categories (housing, food, transportation, etc.)
  - Demographic attributes such as age and year of study

---

## Methodology

### Financial Stress Definition
A student is classified as **financially stressed** if their **essential expenses exceed 70% of their effective income**, where effective income is defined as the sum of monthly income and financial aid.

A sensitivity analysis was performed across multiple thresholds (60%, 70%, 80%) to validate the robustness of this definition.

---

### Feature Engineering
- **Essential expenses** were calculated by aggregating:
  - Housing
  - Food
  - Transportation
  - Health & wellness
  - Books & supplies
- **Non-essential expenses** were calculated separately using:
  - Entertainment
  - Personal care
  - Technology
  - Miscellaneous spending
- **Income bands** were created using quantile-based segmentation to enable fair comparisons across students with different income levels.

---

### Segmentation Strategy
Students were segmented by:
- Income bands (low, lower-mid, upper-mid, high)
- Year of study (freshman, sophomore, junior, senior)
- Financial stress status (stressed vs non-stressed)

---

## Key Insights

### 1. Financial stress is widespread among students
Approximately **79% of students** were classified as financially stressed using the selected threshold.

---

### 2. Income strongly influences financial stress
Financial stress decreases as income rises; however, even among the highest-income students, more than half still experience financial stress.

---

### 3. Financial stress increases by year of study
Stress levels rise steadily from freshman to senior year, suggesting that financial pressure accumulates as students become more financially independent and approach graduation.

---

### 4. Financial stress is driven by essential expenses, not discretionary spending
Average non-essential spending is nearly identical between stressed and non-stressed students, while essential expenses are significantly higher for financially stressed students.  
This indicates that financial stress is primarily driven by unavoidable living costs rather than discretionary overspending.

---

## Recommendations

### For Low-Income Financially Stressed Students
- Focus on reducing unavoidable costs such as housing, food, and transportation
- Improve visibility into financial aid, scholarships, and subsidy opportunities
- Provide tools for optimizing essential spending rather than restricting discretionary purchases

---

### For Higher-Income Financially Stressed Students
- Implement early-warning alerts when essential expenses exceed safe income thresholds
- Improve budget visibility to detect gradual financial stress before it escalates
- Encourage proactive rebalancing of expenses rather than reactive cuts

---

## Tools & Technologies
- **Programming Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib
- **Techniques:** Feature engineering, segmentation, sensitivity analysis, behavioral analysis

---

## Project Structure
```text
student-financial-stress-analysis/
├── data/
│   └── student-spending-habits.csv
├── notebooks/
│   └── analysis.ipynb
├── README.md
