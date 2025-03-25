[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Yi0Zbe2y)
# MAST30034 Project 1 README.md
- Name: `Yicong Yao`
- Student ID: `1302642`

**Timeline:** The timeline for the research area is 2023.Dec.1 - 2024.May.31.

To run the pipeline, please visit the `scripts` directory and run the files in order:
1. `reading.ipynb`: This downloads the raw data into the `data/landing` directory.
2. `preprocess.ipynb`: This notebook details all preprocessing steps and outputs it to the `data/raw` and `data/curated` directory.
3. `EDA.ipynb`: This notebook is used to conduct analysis on the curated data.
4. `model.py` and `model_analysis.ipynb`: The script is used to run the model from CLI and the notebook is used for analysing and discussing the model.



## Taxi Data Analysis Project

This repository contains notebooks for preprocessing, analyzing, and modeling New York City taxi data using Apache Spark, Pandas, and machine learning techniques.

### Project Structure

- **Data Preprocessing:** Cleans and prepares the raw taxi data.
- **Exploratory Data Analysis (EDA):** Analyzes the data to uncover patterns and insights.
- **Model Building:** Implements and evaluates predictive models.

### 1. Data Preprocessing

#### Overview

The preprocessing steps involve cleaning the data, generating new features, and ensuring the data fits the expected ranges and types for analysis.

#### Steps

1. **Drop Unused Columns:** Removes columns that are not needed for the analysis to reduce memory usage and improve processing speed.
2. **Missing Values:** Fills missing values for specific fields (e.g., passenger count).
3. **Data Filtering:** Ensures that only valid records are included based on predefined criteria (e.g., passenger count between 1 and 4).
4. **Feature Engineering:** Adds new columns such as `date_time` and `period` to aid in further analysis.
5. **Data Joining:** Joins additional data (e.g., zone data to add borough information for pickups and drop-offs).
6. **Date Filtering:** Filters data to include only records within specific date ranges.


### 2. Exploratory Data Analysis (EDA)

#### Overview

Performs temporal and geospatial analyses, as well as fare and weather impact studies to understand the data's underlying patterns.

#### Key Analyses

- **Temporal Analysis:** Looks at daily and hourly trip patterns.
- **Geospatial Analysis:** Analyzes spatial patterns of trips across different boroughs and zones.
- **Fare Analysis:** Studies the distribution of fare and tip amounts and explores how they correlate with other factors like trip distance.
- **Weather Impact Analysis:** Examines how different weather conditions affect taxi usage metrics.


### 3. Modeling

#### Overview

Builds predictive models to forecast taxi fares based on various features like passenger count, trip distance, and weather conditions.

#### Models Used

- **Linear Regression:** To establish a baseline for performance.
- **Random Forest Regressor:** To capture non-linear relationships and interactions between features.

#### Evaluation

Compares models based on metrics like Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared.