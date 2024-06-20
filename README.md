# Classification with Academic Success Dataset for PSS S04 E06 

## Overview
This repository contains code and documentation for predicting students' dropout and academic success using machine learning techniques. The models are trained on synthetic data generated using deep learning to mimic the characteristics of the original dataset.

## Dataset
The dataset used in this project is a synthetic version of the "Predict Students' Dropout and Academic Success" dataset. It has been generated using deep learning techniques to maintain the statistical properties and relationships present in the original data.

### Data Source
The original dataset was obtained from [[kaggle](https://www.kaggle.com/competitions/playground-series-s4e6/data)].

## Methods
This project utilizes several machine learning algorithms to build predictive models:

- **Decision Tree (DT)**: A simple, interpretable model that splits the data into subsets based on feature values, forming a tree structure for decision making.
- **Random Forest (RF)**: An ensemble of decision trees that improves prediction accuracy by averaging the predictions of multiple trees to reduce overfitting.
- **XGBoost**: An optimized gradient boosting algorithm that builds sequential trees, using the errors of the previous trees to correct and improve model performance.
- **CatBoost**: A gradient boosting algorithm specifically designed to handle categorical features more effectively and prevent overfitting.
- **LightGBM**: A fast, distributed gradient boosting framework that uses a histogram-based approach for efficient training and improved accuracy.

## Results
### Best Performing Model
The LightGBM model achieved the best classification accuracy in predicting student dropouts and academic success. Key metrics for LightGBM are:

- **Accuracy**: 83.33%
- **Precision**: 90%
- **Recall**: 83%
- **F1-score**: 86%

### Output
The predictions made by the LightGBM model are stored in the `submission.csv` file.
