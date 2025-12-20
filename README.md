# CCSF Student Success Services and Program Completions

### Capstone Project – Exploratory Data Analysis (EDA) and Predictive Modeling

## Table of Contents

* [Project Overview](#project-overview)
* [Research Question](#research-question)
* [Data Sources](#data-sources)
* [Methods and Techniques](#methods-and-techniques)
* [Expected Results](#expected-results)
* [Importance of the Study](#importance-of-the-study)



---

## Project Overview

This capstone project examines whether student participation in support services at City College of San Francisco (CCSF) is associated with higher rates of program award completion over time.

Student support services—such as counseling, orientation, education planning, assessment, and probation services—are widely regarded as critical to student success. However, these services are often evaluated independently from completion outcomes. This project links multi-year service utilization data with institutional award data to explore patterns, trends, and statistical relationships.

The analysis uses publicly available institutional data from the California Community Colleges Chancellor’s Office DataMart, covering academic years 2014–2015 through 2024–2025. The project emphasizes transparent data cleaning, rigorous exploratory analysis, and interpretable baseline modeling.

---

## Research Question

**Does greater participation in student support services at CCSF correspond to higher program award completions over time?**

This question addresses an institutional need. CCSF provides a wide range of student services but does not currently link participation data to program completion outcomes. Understanding this relationship can guide more effective investments and program decisions.

---

## Data Sources

Data Source: [California Community Colleges DataMart](https://datamart.cccco.edu/), covering 2014–2025 data for the San Francisco Community College District.


## 1. Student Success Services (2014–2025)

1. Counts of students receiving services, including:

2. Counseling / Advisement

3. Education Planning

4. Orientation

5. Assessment / Placement

6. Academic or Progress Probation Services

Data are reported at the term level and aggregated to annual totals.

## 2. Program Awards (2014–2025)

Annual counts of:

1. Associate degrees

2. Certificates (credit and noncredit)

3. Total institutional program awards

## 3. Student Headcount (2014–2025)

Annual unduplicated student enrollment, used to normalize:

1. Service utilization rates

2. Program award rates (per 1,000 students)
---

## Methods and Techniques

Notebook 1 — Data Cleaning & Integration

The first notebook constructs a reproducible data-cleaning pipeline that:

1. Removes DataMart metadata rows

2. Standardizes service names across years

3. Extracts only “Service Received” counts

4. Converts string-formatted counts to numeric values

5. Reshapes wide term-level data into long format

6. Aggregates term data into annual totals

7. Produces a clean, analysis-ready master dataset (2014–2025)

### 2. Notebook 2 — Exploratory Data Analysis, Visualization & Baseline Modeling


The EDA notebook focuses on understanding trends, distributions, and relationships through:

1. Time-series visualization of total service delivery

2. Service-specific utilization trends (rates per 1,000 students)

3. Program award trends and normalization by enrollment

4. COVID-19 disruption analysis

5. Correlation analysis between service rates and award rates

6. Exploration of same-year vs. lagged service effects

7. Summary statistics and variability analysis for each service

This notebook establishes context, identifies anomalies, and informs modeling decisions.

## Baseline modeling includes:

1. Multiple Linear Regression (OLS) using service participation rates as predictors

2. Model fit assessment (R², adjusted R², p-values)

3. Interpretation of coefficients in an institutional context

4. Identification of multicollinearity and timing limitations

5. Discussion of why same-year causal interpretation is inappropriate

This notebook establishes a statistical baseline, demonstrating that service participation rates collectively explain a substantial proportion of variation in program award rates.

---

## Expected Results

The project anticipates finding:

* A positive association between counseling, orientation, and education planning participation and program award completions
* Identification of the most impactful services
* Trend alignment or divergence between service participation patterns and completion trends

Such findings will help highlight which support services have the strongest influence on program completion rates.

---

## Key Analytical Themes (So Far)

* Service utilization patterns differ substantially by service type

* Counseling and assessment services account for the largest share of student interactions

* Program award rates increased during COVID-era enrollment declines, requiring careful interpretation

* Several services exhibit stronger relationships with completions when analyzed longitudinally rather than cross-sectionally

* Results caution against simple same-year causal assumptions

## Importance of the Study

* This project contributes to institutional research and planning by:

* Linking service utilization to completion outcomes for the first time at CCSF

* Providing a reproducible, transparent analytical framework

* Supporting evidence-based resource allocation

* Highlighting the importance of timing, scale, and context when evaluating student success services

Rather than treating student services as isolated activities, this analysis frames them as part of a longitudinal student success ecosystem.

## Notebooks

### Notebook 1 — Data Cleaning Pipeline
[notebook_1_student_success_services.ipynb](https://github.com/mgesteban/ccsf-student-success/blob/main/notebook_1_student_success_services.ipynb)
### Notebook 2 for EDA Visualization and Baseline Model
[notebook_2_eda_visualization.ipynb] (https://github.com/mgesteban/ccsf-student-success/blob/main/notebook_2_eda_visualization.ipynb)


