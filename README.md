# Medical_Data_Visualizer
This project demonstrates basic data cleaning, reshaping data for visualization, and creating categorical plots and correlation heatmaps using pandas, matplotlib, and seaborn.

## Objectives:

- Practice cleaning data and feature engineering
- Reshape data using pandas for easier visualization
- Visualize realistic medical data using the seaborn package in Python
- Analyze trends and correlation between physiological or behavioral features and cardiovascular health
- Practice careful interpretation of visualized trends and correlations (especially because causes of cardiovascular disease are complex and likely cannot be determined from simple visual analysis alone)

## Tools and libraries

- Python
- pandas
- seaborn
- NumPy
- matplotlib

# Description

## Import data and engineer features

All data is imported from freeCodeCamp. The "overweight" categorical feature is added to denote whether a patient is overweight or not, determined using a body mass index threshold. Several risk-related features are converted into binary indicators representing healthy vs. elevated-risk categories.

## Categorical plot

A categorical plot is used to show differences in health risk levels from a variety of different behavioral and physiological attributes on patients that possess cardiovascular disease vs. patients who don't. 

Data is reshaped using pandas, variables are renamed for clarity, and the categorical plot is made using seaborn.

<img width="1403" height="526" alt="categorical_plot" src="https://github.com/user-attachments/assets/55064784-55d2-4c2e-ab11-8fc68263905c" />

## Heatmap

A heatmap is used to visualize correlation between behavioral and physiological features and outcomes from the dataset. 

First, outliers and patients with implausible medical results are removed, followed by heatmap generation using seaborn.

<img width="735" height="618" alt="heatmap" src="https://github.com/user-attachments/assets/b8520d00-c31a-46f4-a1e5-f683ffe3b329" />

# Results

## Findings from categorical plot

Generally, cholesterol levels, glucose levels, and whether a patient is overweight show moderate correlation with cardiovascular disease presence in patients. Smoking, alcohol use, and whether a patient is active or not have minimal to no correlation with cardiovascular disease presence in patients based on this data. Of course, this does not indicate or rule out causation by any of these factors.

## Findings from heatmap

After removing outliers and implausible patient data, it appears that no feature is very strongly correlated with the presence of cardiovascular disease. However, systolic blood pressure, cholesterol levels, age, and weight have the greatest correlation with cardiovascular disease presence (ranging from 0.17 to 0.33, where 0 indicates no correlation and 1 indicates perfect correlation). I refrain from commenting on the reason that these factors have the greatest correlation because doing so would be highly speculative due to the high complexity and large number of processes that cause cardiovascular disease.

Weight and overweight status have noticeable correlation, as expected. A heavier person generally means a higher likelihood that the person is overweight, and vice versa.

## Comparison of findings

From the categorical plot, cholesterol levels, glucose levels, and whether a patient is overweight or not correlate most strongly with cardiovascular health, whereas the factors that correlate most with cardiovascular disease presence from the heatmap are cholesterol levels, age, systolic blood pressure, and weight. 

The categorical plot neglects any factors that do not categorize patients into two different categories based on risk level, so systolic blood pressure, age, and weight do not show up on this plot. For this reason, as well as the removal of implausible and outlying data from the heatmap, the heatmap provides a more interpretable and complete description of factors correlated with cardiovascular health. 

Neglect of many features for the categorical plot also contributes to the discrepancy between feature importances from the categorical plot and the heatmap. Another factor contributing to this discrepancy could be the removal of implausible and outlying data before creating the heatmap, which was not done for the categorical plot.
