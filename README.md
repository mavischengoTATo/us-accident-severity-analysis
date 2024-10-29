# U.S. Accident Severity Analysis

## Introduction

The **U.S. Accident Severity Analysis** project aims to investigate factors that influence the severity of accidents across the United States. By analyzing the **U.S. Accident dataset** covering accidents from February 2016 to December 2021, this study seeks to provide insights into key variables that impact accident severity. The findings of this analysis could assist policymakers and law enforcement in enhancing road safety, implementing preventive measures, and managing high-risk traffic areas more effectively.

### Dataset Overview
The dataset contains approximately 2 million records of traffic incidents reported across 49 U.S. states. This data is sourced from multiple APIs that capture incident details from traffic cameras, sensors, and various transportation departments. Due to computational constraints, a subset of the dataset was used for the analysis.

## Project Structure

This repository is organized as follows:
.
├── code
│   ├── data_analysis        # Scripts for analyzing accident severity factors
│   ├── data_cleaning        # Data cleaning scripts to preprocess raw data
│   └── eda                  # Exploratory Data Analysis scripts for initial insights
├── data
│   ├── clean_data           # Preprocessed data ready for analysis
│   └── raw_data             # Original, unprocessed data files
├── img                      # Folder containing images used for visualizations
└── poster                   # Poster summarizing the project methodology and findings
## Methodology

### Step 1: Model Selection and Tuning
The analysis began by testing various machine learning models to identify the most suitable classifiers for predicting accident severity, classified from levels 1 to 4. Models tested included:
- Logistic Regression
- Linear Discriminant Analysis (LDA)
- Quadratic Discriminant Analysis (QDA)
- Bagging
- Random Forest
- Naive Bayes
- Decision Trees
- Neural Networks

After initial testing, **Bagging** and **Random Forest** were selected as top-performing models due to their high accuracy and AUC scores.

### Step 2: Model Training
The chosen models, Bagging and Random Forest, were trained on the entire training dataset. Hyperparameter tuning was applied to optimize their performance in classifying accident severity.

### Step 3: Feature Importance Analysis
The models highlighted significant variables influencing accident severity, including:
- **Weather Conditions**: Temperature, Humidity, Wind Chill
- **Accident Details**: Duration, Distance
- **Geographical Indicators**: Specific state IDs like CA, AZ, and NC

These factors were found to play a crucial role in predicting accident severity, with weather conditions significantly impacting road safety.

## Results

The analysis revealed that:
- **Bagging and Random Forest** models demonstrated high accuracy in classifying accident severity.
- **Weather-related factors** (such as temperature and humidity) and **accident-specific variables** (like duration and distance) are key predictors of accident severity.
- The presence of unique road signs or specific state identifiers contributed minimally to severity prediction.

## Conclusion

This project underscores the importance of analyzing environmental and contextual factors in accident severity prediction. With the aid of machine learning models, we identified crucial determinants of accident severity, offering actionable insights for policymakers and traffic safety officials to reduce accident severity in high-risk areas.

Future research could expand upon this analysis by incorporating additional data (such as post-COVID traffic patterns) to provide a more comprehensive understanding of accident dynamics in the U.S.

---

## References

1. Moosavi, Sobhan, et al. "A Countrywide Traffic Accident Dataset." (2019).
2. Moosavi, Sobhan, et al. "Accident Risk Prediction based on Heterogeneous Sparse Data: New Dataset and Insights." 27th ACM SIGSPATIAL International Conference on Geographic Information Systems, ACM, 2019.

