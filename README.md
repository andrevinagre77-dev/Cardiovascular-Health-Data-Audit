# Cardiovascular Biometrics: A Systematic Data Audit & Inferential Analysis

### Executive Summary

I was given a dataset of 1,000 patient records to understand one simple but critical question: **Do lifestyle changes actually improve cardiovascular health, or are we just seeing noise in the data?**

Coming from 26 years working with human behavior and addiction patterns, I knew that numbers alone don’t tell the full story. So I started where I always start — by checking if the data was trustworthy.

I discovered that the original BMI column was mathematically incorrect. I rebuilt it from the raw weight and height, and split the blood pressure field into systolic and diastolic values. Only after cleaning the foundation did I run the analysis.

Using a two-sample T-test, I compared heart rate between physically active and sedentary patients. The result was clear: **there was no statistically significant difference** (p-value = 0.4614).

This wasn’t a failure. It was a powerful insight: cardiovascular health in this population is influenced by many more factors than just physical activity — something my years of behavioral experience already suspected.

**Technical Stack:** Python (Pandas), SciPy, Seaborn, JupyterLab
