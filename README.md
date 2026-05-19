# Medical_Data_Visualizer
This mini project demonstrates basic data cleaning and reshaping data for visualization, categorical plots, and correlation heatmaps using pandas, matplotlib, and seaborn.

## Objectives:

- Visualize realistic medical data using the seaborn package in Python
- Analyze trends and correlation between features and cardiovascular health
- Practice precaution with intpretation of results, especially because true causation of cardiovascular disease is very complex and likely cannot be determined from a quick visual analysis alone
- Reshape data using pandas for easier visualization with seaborn
- Practice cleaning data and feature engineering

## Languages/packages used

- Python
- pandas
- seaborn
- NumPy
- matplotlib

# Description

## Import data and engineer features

All data is imported from freeCodeCamp. The "overweight" categorical feature is added to denote whether a patient is overweight or not, determined via a BMI threshold. Risk-based feature values are also normalized so that each becomes a binary indicator of risk level to the patient (0 as good, 1 as bad).

## Categorical plot

A categorical plot is used to show differences in risk levels from a variety of different features on patients that possess cardiovascular disease vs. patients who don't. 

Data is reshaped using pandas, variables are renamed for clarity, and a categorical plot is made using seaborn.

## Heatmap

A heatmap is used to visualize correlation between risk features and outcomes from the dataset. 

First, outliers and patients with implausible medical results are removed, followed by heatmap generation using seaborn.

# Results

## Findings from categorical plot

Generally, cholesterol levels, glucose levels, and whether a patient is overweight show moderate correlation with cardiovascular disease presence in patients. Smoking, alcohol, and whether a patient is active or not have minimal to no correlation with cardiovascular disease presence in patients based on this data. Of course, this does not indicate causation by any of these factors.

## Findings from heatmap

After removing outliers and potentially problematic patient data, it appears that no feature is very strongly correlated with the presence of cardiovascular disease, but systolic blood pressure, cholesterol levels, age, and weight have the greatest correlation (ranging from 0.17 to 0.33). It is difficult to comment on the exact reasons for these factors having the largest effects on cardiovascular disease presence without a proficient background in medicine and health (and even then it might be difficult or even impossible). However, all of these factors could sensibly have some effect on cardiovascular health (i.e., they are all related to health and/or physical attributes of patients), so it makes sense that some factors are notably correlated with cardiovascular health. 

Weight and overweight status have noticeable correlation, as expected. A heavier person generally means a higher likelihood that the person is overweight, and vice versa.

## Comparison of findings

From the categorical plot, cholesterol levels, glucose levels, and whether a patient is overweight or not correlate most strongly with cardiovascular health, whereas the factors that correlate most from the heatmap are cholesterol levels, age, systolic blood pressure, and weight. 

The categorical plot neglects any factors that do not categorize patients into two different categories based on risk level, so systolic blood pressure, age, and weight do not show up on this plot. For this reason, as well as the removal of implausible and outlying data, the heatmap provides a more significant and complete description of factors correlated with cardiovascular health. Neglect of many features for the categorical plot also likely contributes to the discrepancy between feature importances from the categorical plot and the heatmap. Another factor could be removal of implausible and outlying data for the heatmap, which was not done for the categorical plot.
