# HR Workforce Analytics

## Project Overview

This project examines workforce data to assess workforce structure, employee characteristics, workforce stability, and resignation patterns.

Rather than treating HR analytics as a collection of descriptive charts, the analysis is structured around business questions relevant to workforce planning, employee retention, and management decision-making.

The analysis combines data quality assessment, exploratory analysis, workforce segmentation, statistical testing, multivariate analysis, predictive modelling, and decision-oriented visualisation.

The objective is to move from understanding **what is happening** to determining **where meaningful differences exist, what relationships are supported by the data, and what actions the evidence can reasonably support**.

---

## Business Problem

Organisations can accumulate large volumes of employee data without having a clear understanding of the workforce patterns contained within it.

A simple attrition rate, average salary, or departmental headcount does not adequately explain whether particular employee characteristics are associated with resignation or whether meaningful workforce risks are concentrated within specific segments.

This project investigates the workforce from several analytical perspectives:

- Where is employee attrition concentrated?
- Which employee and job characteristics are associated with resignation?
- How do compensation, tenure, workload, and employee satisfaction relate to workforce outcomes?
- Are certain departments, roles, or employee segments experiencing materially different resignation rates?
- Which relationships remain relevant when multiple employee characteristics are considered simultaneously?
- Can the available workforce variables support reliable resignation prediction?
- What evidence can be translated into practical workforce-management recommendations?

---

## Analytical Objectives

The analysis was designed to:

1. Establish the structure, quality, completeness, and reliability of the dataset.
2. Profile the workforce across demographic, organisational, compensation, and employment characteristics.
3. Measure and examine employee resignation across relevant workforce segments.
4. Compare resigned and retained employees across key workforce measures.
5. Identify statistically meaningful relationships rather than relying solely on visual differences.
6. Assess the explanatory and predictive value of the available workforce variables.
7. Translate evidence into practical workforce-management recommendations.
8. Communicate analytical limitations and avoid interpreting association as causation.

---

## Dataset

**Source:** Onyx Data / DataDNA Employee Performance and Productivity Dataset — October 2024

The dataset contains:

- **100,000 employees**
- **20 variables**
- Unique employee identifiers
- Demographic characteristics
- Department and job information
- Compensation measures
- Employment and workload measures
- Training and promotion information
- Performance and satisfaction measures
- Remote-work frequency
- Employee resignation status

The primary workforce outcome examined in this project is `Resigned`.

---

## Analytical Approach

The project followed a structured analytical workflow:

1. Dataset understanding and business framing
2. Data quality and integrity assessment
3. Data preparation and feature engineering
4. Exploratory workforce analysis
5. Attrition and workforce segmentation
6. Statistical analysis
7. Multivariate analysis
8. Business interpretation
9. Recommendations and management implications
10. Final documentation and reproducibility

The analysis used descriptive statistics, workforce segmentation, independent-samples testing, effect-size analysis, chi-square tests, Cramér's V, correlation analysis, logistic regression, ROC analysis, precision-recall analysis, classification-threshold analysis, and out-of-sample validation.

---

## Key Findings

### Workforce Profile

The workforce is broadly balanced across departments and job titles, with relatively limited variation in the overall organisational structure.

Department-level analysis also showed broadly similar workforce conditions across tenure, salary, working hours, workload, overtime, training, performance, and employee satisfaction.

### Resignation

A total of **10,010 employees resigned**, representing an overall resignation rate of **10.01%**.

Resignation rates were broadly consistent across:

- Departments
- Job titles
- Gender
- Education level
- Remote-work frequency
- Age groups
- Tenure groups
- Salary quartiles
- Employee satisfaction groups

### Statistical Evidence

Statistical testing found no statistically significant differences between resigned and retained employees across the continuous workforce variables examined.

Effect-size analysis also indicated that the observed differences were negligible.

Chi-square analysis found no statistically significant association between resignation and the major categorical workforce segments examined, with Cramér's V values indicating negligible association strength.

Correlation analysis similarly found extremely weak relationships between the continuous workforce variables and resignation.

### Predictive Modelling

The logistic regression model demonstrated very limited explanatory value:

- **McFadden pseudo R²:** 0.000399
- **Likelihood-ratio test p-value:** 0.837
- **Full-dataset ROC-AUC:** approximately 0.516
- **Held-out test ROC-AUC:** approximately 0.492
- **Held-out Average Precision:** approximately 0.098

At the standard 0.50 classification threshold, the model classified all employees as retained. This produced an apparent accuracy of **89.99%**, but precision, recall, and F1-score for the resignation class were all zero.

The results demonstrate why accuracy alone is insufficient for evaluating an attrition model when the outcome is imbalanced.

### Overall Analytical Conclusion

The analysis does not identify a single demographic, department, compensation level, tenure group, satisfaction category, or other available workforce characteristic that can reliably explain employee resignation.

This should not be interpreted to mean that these factors are universally unrelated to retention. Rather, the available dataset does not provide sufficient evidence to identify strong relationships with resignation within the observed workforce.

The findings indicate that important factors associated with resignation may lie outside the variables captured in the dataset.

---

## Business Recommendations

1. **Strengthen employee exit and experience data**

   Collect structured information on reasons for leaving, career development, manager relationships, workload, organisational culture, benefits, compensation competitiveness, and other relevant employee-experience factors.

2. **Monitor attrition continuously**

   Establish regular workforce monitoring rather than targeting broad employee groups without supporting evidence.

3. **Develop a more complete workforce analytics framework**

   Integrate employee engagement, career progression, manager and team information, benefits, absenteeism, performance history, internal mobility, and structured exit data where available.

4. **Use predictive models responsibly**

   The current model should not be used as an employee-level resignation-risk scoring mechanism. Future models should demonstrate acceptable performance on unseen data and undergo appropriate validation, fairness assessment, monitoring, and governance.

5. **Establish evidence-based retention reviews**

   Use the 10.01% resignation rate as a baseline for ongoing monitoring and investigate material changes using both quantitative workforce data and qualitative employee feedback.

---

## Limitations

The analysis is subject to the variables and observations available in the supplied dataset.

The dataset does not adequately capture several potentially important aspects of employee experience, including career progression, manager relationships, organisational culture, employee engagement, benefits, internal mobility, labour-market opportunities, and structured reasons for leaving.

The dataset is also cross-sectional, limiting the ability to assess how workforce conditions change over time or establish temporal relationships preceding resignation.

The statistical and predictive analyses identify associations rather than causal relationships. The absence of a statistically significant relationship within this dataset does not demonstrate that a workforce characteristic has no effect on retention in other organisational settings.

The predictive model demonstrated weak out-of-sample performance and should therefore not be interpreted as a reliable operational resignation-risk model.

---

## Project Deliverables

The completed project contains:

- Reproducible Python analysis
- Documented data-quality assessment
- Exploratory workforce analysis
- Workforce segmentation
- Statistical analysis
- Multivariate analysis
- Predictive model evaluation
- Decision-oriented visualisations
- Evidence-based findings
- Business recommendations
- Executive Report
- Technical documentation
- Reproducible project environment

---

## Project Structure

```text
hr-workforce-analytics/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── docs/
│   └── HR_Workforce_Analytics_Executive_Report.pdf
│
├── notebooks/
│   └── hr_workforce_analysis.ipynb
│
├── sql/
│
├── src/
│
├── visuals/
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt