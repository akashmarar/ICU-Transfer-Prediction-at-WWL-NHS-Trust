# ICU Transfer Prediction at WWL NHS Trust

This repository includes the **final report**, **poster**, and **presentation** for a project conducted as a Data Scientist Intern at Wrightington, Wigan, and Leigh NHS Foundation Trust. The project focused on leveraging machine learning to predict ICU transfers, aiming to enhance early identification of critically ill patients and optimize hospital resource management.

## Project Overview

Early and accurate prediction of ICU transfers is critical to improving patient outcomes and hospital efficiency. This project aimed to:
1. Develop a machine learning model to predict ICU transfers.
2. Address the challenge of class imbalance in ICU transfer data.
3. Identify the most significant features contributing to ICU transfer predictions to support clinical decision-making.

### Key Insights:
- **Data Scope**: The dataset included information from 73,628 unique patients spanning January 2019 to May 2024.
- **Model Performance**: XGBoost with SMOTE delivered the highest F1-score, significantly outperforming the traditional NEWS2 scoring system.
- **Feature Importance**: Albumin, age, and globulin emerged as the top predictors for ICU transfers.

## Repository Contents

- **Predicting ICU Transfers.pdf**: Comprehensive report detailing the project's objectives, methodology, results, and future directions.
- **Poster_Akash_Updated.pdf**: Visual summary of the project's key findings and achievements.
- **Predicting ICU Transfers PPT.pdf**: Presentation slides used for project review and dissemination.

## Methodology

### 1. Preprocessing:
- Handled missing values using forward/backward filling and iterative imputation.
- Addressed outliers through Winsorization, preserving clinically relevant extremes.
- Encoded categorical data and removed potential data leakage variables.

### 2. Modeling:
- **Class Imbalance Techniques**: Tested methods such as SMOTE, Tomek Links, and Random Under-Sampling.
- **Algorithms**: Implemented Random Forest and XGBoost, optimizing hyperparameters for F1-score using GridSearchCV.
- **Feature Importance**: Analyzed predictors using SHAP for interpretability and actionable insights.

### 3. Validation:
- Temporal split was used to simulate real-world scenarios, training on pre-April 2024 data and validating on post-April 2024 data.

### Results:
- **F1-score**: XGBoost with SMOTE achieved the highest F1-score, balancing precision and recall for critical care predictions.
- **AUC-ROC**: Random Forest demonstrated stable performance across class balancing techniques, with AUC values clustering between 0.83 and 0.86.

## Ethical Considerations

- **Data Privacy**: Adhered to UK data protection regulations with robust anonymization measures.
- **Model Transparency**: Ensured accessible documentation and regular audits to prevent biases.
- **Human Oversight**: Designed the model to complement clinical judgment, not replace it.

## Future Work

- Incorporate natural language processing to analyze doctors' diagnostic notes.
- Expand the dataset to include additional hospitals for improved generalizability.
- Explore time-series models for capturing patient condition progression.

## How to Use

This repository is intended for reference purposes, showcasing the approach and results of implementing predictive analytics in a healthcare setting. The included materials offer insights into handling imbalanced datasets, feature engineering, and model evaluation for critical care predictions.

## Acknowledgements

- **Supervisors**: Nishchay Joshi, Thomas Ingram, and Brian Wood.
- **Academic Guidance**: Marco Battiston (Lancaster University).
- **Institution**: Wrightington, Wigan, and Leigh NHS Foundation Trust.


