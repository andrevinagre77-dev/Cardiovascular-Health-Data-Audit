# Cardiovascular Biometrics: A Systematic Data Audit & Inferential Analysis

## 1. Executive Summary
This technical audit targets a dataset of 1,000 patient records to validate data integrity and assess the impact of lifestyle interventions on cardiovascular performance. The analysis identifies critical biometric inconsistencies and employs a frequentist statistical approach to test hypothesis significance.

## 2. Data Integrity & Risk Mitigation (GIGO Prevention)
A preliminary audit revealed structural flaws in the source data that would lead to "Garbage In, Garbage Out" (GIGO) scenarios.

* **Audit of Faulty BMI**: The original `BMI` column exhibited mathematical drift. I implemented a recovery field `BMI_Real` derived from raw `Weight_kg` and `Height_cm`.
* **Structural Deconstruction**: The `Blood_Pressure` string variable was parsed into `Systolic` and `Diastolic` integers, enabling granular clinical risk profiling.
* **Validation Metric**: A Pearson correlation matrix confirms the audit's success, showing a robust **0.82** correlation between weight and the corrected BMI.



## 3. Inferential Framework & Hypothesis Testing
The core objective was to determine if physical activity levels significantly shift the biometric mean of heart rate.

* **Statistical Methodology**: Two-sample Student's T-test.
* **Null Hypothesis ($H_0$)**: No significant difference exists in heart rate between active and sedentary cohorts.
* **The Verdict**: Computed **P-Value = 0.4614**.
* **Strategic Insight**: We **fail to reject the null hypothesis**. The variance is not statistically significant, proving that cardiovascular health in this cohort is a **multifactorial system**.

## 4. Technical Stack
* **Environment**: JupyterLab.
* **Language**: Python 3.10+.
* **Libraries**: Pandas (Auditing), Seaborn/Matplotlib (Visualization), Scipy.stats (Inferential Analysis).

---
*Audit performed by André Vinagre.*
