# Student Final Exam Score Prediction using ANN

## Overview

This project uses an Artificial Neural Network (ANN) built with TensorFlow and Keras to predict students' Final Exam Scores from academic and student-related features.

The project focuses on applying Deep Learning to a tabular regression problem and understanding how preprocessing and feature scaling affect neural network performance.

## Objective

The objective is to develop a regression model that can predict a student's Final Exam Score based on relevant academic features such as study hours, attendance, assignment performance, and previous exam performance.

## Problem Type

* Problem: Regression
* Target Variable: `Final_Exam_Score`
* Dataset: Tabular CSV
* Model: Artificial Neural Network
* Framework: TensorFlow / Keras

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* TensorFlow
* Keras

## Project Workflow

```text
Data Collection
      ↓
Data Preprocessing
      ↓
Train-Test Split
      ↓
Feature Scaling
      ↓
ANN Model Development
      ↓
Model Training
      ↓
Early Stopping
      ↓
Prediction
      ↓
Model Evaluation
```

## Data Preprocessing

The target variable `Final_Exam_Score` was separated from the input features. The dataset was then divided into training and testing sets.

Since the input features had different numerical ranges, `StandardScaler` was used to standardize the features. The scaler was fitted only on the training data and then applied to both training and testing data.

## Model Architecture

The ANN consists of two hidden layers:

```text
Input Layer
    ↓
Dense Layer (64 neurons, ReLU)
    ↓
Dense Layer (32 neurons, ReLU)
    ↓
Output Layer (1 neuron, Linear)
```

The model uses the Adam optimizer and Mean Squared Error (MSE) as the loss function. Early stopping was used during training to monitor validation loss and restore the best model weights.

## Model Performance

The final model achieved the following results on the test dataset:

| Metric   | Score |
| -------- | ----: |
| MAE      |  4.05 |
| MSE      | 25.79 |
| R² Score | 0.712 |

An R² score of 0.712 indicates that the model explains approximately 71.2% of the variation in Final Exam Scores within the test dataset.

The MAE of 4.05 indicates that the model's predictions differ from the actual scores by approximately 4 score units on average.

## Model Improvement

The initial model achieved an R² score of 0.117. After applying feature scaling and improving the training configuration, the R² score increased to 0.712, while MAE decreased from 7.62 to 4.05.

This improvement highlights the importance of appropriate preprocessing and feature scaling when training neural networks on tabular data.

## Key Learnings

* Applying preprocessing to tabular data for Deep Learning
* Understanding the importance of feature scaling in ANN models
* Building neural networks using TensorFlow and Keras
* Using ReLU and Linear activation functions
* Training models with the Adam optimizer
* Applying Early Stopping
* Evaluating regression models using MAE, MSE, and R²
* Improving model performance through preprocessing and training adjustments

## Conclusion

This project provided practical experience in developing a TensorFlow-based ANN for tabular regression. The final model achieved an R² score of 0.712 on the test dataset, demonstrating that the selected features contain useful information for predicting Final Exam Scores.

The project also showed how proper feature scaling and training configuration can significantly improve neural network performance.
