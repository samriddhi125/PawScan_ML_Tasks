# Classification with Academic Success Dataset for PSS S04 E06 

## Overview
This repository contains code and documentation for predicting students' dropout and academic success using machine learning techniques. The models are trained on synthetic data generated using deep learning to mimic the characteristics of the original dataset.

## Dataset
The dataset used in this project is a synthetic version of the "Predict Students' Dropout and Academic Success" dataset. It has been generated using deep learning techniques to maintain the statistical properties and relationships present in the original data.

### Data Source
The original dataset was obtained from [[kaggle](https://www.kaggle.com/competitions/playground-series-s4e6/data)].

## Methods
This project utilizes several machine learning algorithms to build predictive models:

- Decision Tree (DT)
- Random Forest (RF)
- XGBoost
- CatBoost
- LightGBM

## Results
### Best Performing Model
The LightGBM model achieved the best classification accuracy in predicting student dropouts and academic success. Key metrics for LightGBM are:

- **Accuracy**: [accuracy]
- **Precision**: [precision]
- **Recall**: [recall]
- **F1-score**: [F1-score]

### Output
The predictions made by the LightGBM model are stored in the `submission.csv` file.
