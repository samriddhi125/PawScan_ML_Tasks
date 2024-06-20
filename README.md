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
- **Random Forest (RF)**: An ensemble of decision trees that improves prediction accuracy by averaging the predictions of multiple trees, reducing overfitting and variance.
- **XGBoost**: An optimized gradient boosting algorithm that builds sequential trees, leveraging the errors of previous trees to make corrections and enhance model performance.
- **CatBoost**: A gradient boosting algorithm specifically designed to handle categorical features effectively and reduce overfitting through advanced regularization techniques.
- **LightGBM**: A fast, distributed gradient boosting framework that uses a histogram-based approach for efficient training and enhanced accuracy, particularly well-suited for large datasets with many features.

### Traditional Machine Learning vs. Deep Learning
Given that the dataset used in this project is relatively simple and small in scale compared to datasets typically used for deep learning, traditional machine learning methods were preferred for several reasons:

1. **Risk of Overfitting with Deep Learning**: Deep learning models, such as neural networks, are highly flexible and can capture complex patterns in large datasets. However, they tend to overfit when applied to simpler datasets because they can easily memorize the training data instead of generalizing from it. This leads to poor performance on unseen data.
2. **Interpretability**: Traditional machine learning models, like decision trees and gradient boosting methods, provide more interpretability and insights into the data and model behavior, which is valuable for understanding student dropout and success factors.
3. **Efficiency**: Traditional models often require less computational power and time to train and evaluate, making them more efficient for the given dataset size and complexity.

## Results
### Best Performing Model
The LightGBM model achieved the best classification accuracy in predicting student dropouts and academic success. Key metrics for LightGBM are:

- **Accuracy**: 83.33%
- **Precision**: 90%
- **Recall**: 83%
- **F1-score**: 86%

### Why LightGBM Performed Better
LightGBM (Light Gradient Boosting Machine) outperformed other models in this project due to several factors:

1. **Efficient Handling of Large Data**: LightGBM uses a histogram-based algorithm that reduces the time complexity and speeds up training, which is advantageous for large datasets or those with many features.
2. **Advanced Leaf-Wise Growth**: Unlike depth-wise growth used in many traditional boosting algorithms, LightGBM grows trees leaf-wise. This method allows the model to focus on the most significant splits, improving accuracy and reducing overfitting.
3. **Optimal Handling of Sparse Features**: LightGBM is designed to handle sparse data effectively, which is common in educational datasets where many features might not apply to all students.
4. **Tunable Complexity**: The model provides flexibility to control complexity through parameters like `num_leaves` and `min_data_in_leaf`, allowing it to generalize better than other algorithms while maintaining high accuracy.

### Output
The predictions made by the LightGBM model are stored in the `submission.csv` file.
