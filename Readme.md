# Sydney Residential Property Market Analysis

A statistical case study analysing residential house sales across Sydney in 2021 to identify the property and suburb characteristics most strongly associated with sale price.

## Overview

This project analyses a dataset of 3,676 residential house sales across Sydney in 2021 for a hypothetical property investment group. The analysis covers four tasks: 

1. **Exploratory Data Analysis (EDA)** – summary statistics, distributions, and relationships between price and key variables (distance from CBD, suburb income, property size, bedrooms, bathrooms, parking).
2. **Group Comparisons** – one-way ANOVA testing whether mean (log) property prices differ across property size groups and CBD distance groups, including assumption checks (Q-Q plots, Bartlett's test) and a log transformation of price to address non-normality and heteroscedasticity.
3. **Pairwise Analysis** – Tukey HSD post-hoc tests to identify which specific group pairs drive the differences found in Task 2.
4. **Multiple Linear Regression** – a model predicting log(sale price) from property size, distance from CBD, suburb median income, suburb elevation, bedrooms, bathrooms, and parking, with full diagnostics and plain-language coefficient interpretation.

## Repository Contents

| File | Description |
|---|---|
| `analysis.Rmd` | R Markdown source code for the full statistical report (EDA, ANOVA, Tukey HSD, regression, diagnostics). |
| `report.pdf` | Final rendered report — executive summary plus full technical analysis. |

**Note:** The original dataset and case study brief are not included, as they were provided as part of a university assessment and are not mine to redistribute.

## Key Findings

- **Distance from the CBD** is the strongest predictor of price — inner-suburb properties sold for roughly double the price of outer-suburb properties.
- **Suburb median income** is the second strongest driver, with higher-income suburbs commanding higher prices independent of other factors.
- **Bathrooms** are the most valuable physical property feature, adding roughly 14% to sale price per additional bathroom — well above the effect of extra bedrooms or parking spaces (~2% each).
- The final regression model explains approximately **49% of the variation** in log sale price (R² = 0.49), with all seven predictors statistically significant at the 5% level.

## Notes

- Methods used: exploratory data analysis, histograms, boxplots, scatterplots, one-way ANOVA, Bartlett's test, Tukey HSD, multiple linear regression, log transformation, t-tests, and regression diagnostics.
- This repository is shared for portfolio/reference purposes.
