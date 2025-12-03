# CCSF Student Success Services and Program Completions

### Capstone Project – Exploratory Data Analysis (EDA) and Predictive Modeling

## Table of Contents

* [Project Overview](#project-overview)
* [Research Question](#research-question)
* [Data Sources](#data-sources)
* [Methods and Techniques](#methods-and-techniques)
* [Expected Results](#expected-results)
* [Importance of the Study](#importance-of-the-study)
* [Repository Structure](#repository-structure)


---

## Project Overview

This capstone project examines whether student participation in support services at City College of San Francisco (CCSF) correlates with increased student program completions over time. Support services include counseling, orientation, education planning, and other student success initiatives.

The analysis uses multi-year institutional data (2014–2025) from the California Community Colleges Chancellor’s Office DataMart. Exploratory Data Analysis (EDA) techniques and predictive modeling are used to understand trends, correlations, and the relative impact of specific services on completion outcomes.

---

## Research Question

**Does greater participation in student support services at CCSF correspond to higher program award completions over time?**

This question addresses an institutional need. CCSF provides a wide range of student services but does not currently link participation data to program completion outcomes. Understanding this relationship can guide more effective investments and program decisions.

---

## Data Sources

Data Source: [California Community Colleges DataMart](https://datamart.cccco.edu/), covering 2014–2025 data for the San Francisco Community College District.


### Student Success Services Summary

Data elements include counts for:

* Counseling
* Orientation
* Education planning
* Other success services

### Program Awards Summary

Totals for:

* Certificates
* Associate degrees
* Program awards by type and year

### Student Headcount Reports

* Term and annual enrollment (used for normalization and trend comparison)

### Full-Time Equivalent Students (FTES)

* Enrollment-based funding metric used for statewide apportionment

Reference: Capstone proposal.

---

## Methods and Techniques

### 1. Exploratory Data Analysis (EDA)

The EDA phase includes:

* Data cleaning and preparation
* Examination of year-over-year and term-over-term trends
* Normalization using headcount and FTES
* Visualization of service usage versus program completions
* Correlation analysis
* Exploration of lag effects (service participation in year t vs. completions in year t+1)

### 2. Predictive Modeling

To evaluate relationships between service participation and completions:

* Multiple Linear Regression to test the predictive value of service participation while controlling for enrollment size
* Decision Tree Regressor to identify which services contribute most to completions
* Regularized models (Ridge) or Random Forest Regressor may be tested to address potential overfitting

Reference: Techniques section of proposal.

---

## Expected Results

The project anticipates finding:

* A positive association between counseling, orientation, and education planning participation and program award completions
* Identification of the most impactful services
* Trend alignment or divergence between service participation patterns and completion trends

Such findings will help highlight which support services have the strongest influence on program completion rates.

---

## Importance of the Study

This project is important for educational planning and resource allocation at CCSF. Without studying these relationships, institutional decisions may lack evidence-based justification. If strong correlations are identified, the college can prioritize services with the greatest effect on student outcomes and improve service design, outreach, and retention strategies.

---

## Repository Structure

```
.
├── data/                     # Raw CSVs and cleaned datasets
├── eda/                      # EDA notebooks (Notebook 1, 2, and 3 to be added)
├── models/                   # Regression and tree-based model scripts
├── visualizations/           # Generated charts and figures
├── reports/                  # Initial and final capstone reports
└── README.md                 # Project documentation (this file)
```

---

## Notebooks

### Notebook 1 — Data Cleaning Pipeline
[student_success_services.ipynb](https://github.com/mgesteban/ccsf-student-success/blob/main/student_success_services.ipynb)
* Build Notebook 2 for EDA and visualization
* Build Notebook 3 for regression modeling and decision tree analysis
* Draft the initial report summarizing EDA insights and early findings
* Produce final analysis and recommendations

