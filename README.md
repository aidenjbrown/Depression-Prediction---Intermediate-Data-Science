# Depression Prediction with NHANES Data

Code and analysis repository for a predictive modeling project using NHANES 2017–2018 survey data to explore whether demographic, income, sleep, work, weight, and health-related variables could predict depression score.

This project was completed for Intermediate Data Science at Vassar College by Aiden Brown and Tony Nguyen.

## Project Website

Full writeup, visualizations, methodology, and results summary:

[Depression Prediction Website](https://aidenjbrown.github.io/depression-prediction-website/)

Website repository:

[depression-prediction-website](https://github.com/aidenjbrown/depression-prediction-website)

## Overview

This project explored whether survey variables from NHANES could predict depression questionnaire scores or classify elevated depression-risk cases.

We calculated depression score by aggregating NHANES depression symptom indicators and used demographic, income, sleep, work, and body-weight-related variables as predictors.

The goal was exploratory: to evaluate whether these variables showed meaningful predictive signal, not to create a diagnostic or clinical tool.

## Research Question

What impact, if any, do demographics, sleep behaviors, income, body weight, and work hours have on predicting depression score?

## Methods

We tested multiple modeling approaches, including:

- Linear regression
- LASSO regression
- Neural network regression
- Gradient boosting regression
- Gradient boosting classification
- SHAP analysis for model interpretation

## Results Summary

The models showed limited predictive power for exact depression-score prediction. The regression models performed worse on average than predicting the mean depression score.

Headline model results:

| Model | Task | RMSE | R² | Accuracy | Recall | Precision |
|---|---|---:|---:|---:|---:|---:|
| Linear Regression | Regression | 4.39 | -0.034 | — | — | — |
| LASSO | Regression | 4.39 | -0.034 | — | — | — |
| Neural Network | Regression | 4.60 | -0.150 | — | — | — |
| Gradient Boosting | Regression | 4.48 | -0.022 | — | — | — |
| Gradient Boosting | Classification | — | — | 60% | 85% | 64% |

## Key Takeaways

- Broad demographic, income, sleep, work, and body-weight variables were not strong enough on their own to predict depression score accurately.
- EDA suggested possible relationships involving education and income, but the predictive models did not show strong individual-level performance.
- The classification model had high recall but lower accuracy and precision, suggesting many false positives.
- SHAP analysis helped identify influential predictors, but the project does not claim causal relationships.

## Repository Structure

- `data/` — project data files
- `scripts/` — cleaning, analysis, and modeling code
- `presentation/` — presentation materials

## Tech Stack

- Jupyter Notebook
- Python
- R
- Regression and classification modeling
- SHAP
- Data cleaning and visualization

## Disclaimer

This project is for exploratory data analysis and research practice only. It is not intended for diagnosis, clinical screening, or individual decision-making.

## Contributors

- Aiden Brown
- Tony Nguyen
