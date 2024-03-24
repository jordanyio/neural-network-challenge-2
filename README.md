# Employee Attrition & Department Prediction README

## Overview

This project focuses on constructing and training a neural network model to predict two key aspects based on various employee features:

1. **Employee Attrition:** Whether an employee is likely to leave the company.
2. **Department Classification:** The department to which an employee belongs.

The dataset features employee demographics, job roles, satisfaction levels, and performance metrics, aiming to utilize these factors to accurately predict outcomes in the aforementioned categories.

## Data

The dataset comprises a rich set of features, including but not limited to:

- Age
- Years at the company
- Total working years
- Hourly rate
- Distance from home
- Job role
- Levels of job satisfaction

The target variables for prediction are:

- **Attrition:** Binary outcome (Yes/No)
- **Department:** Multiclass variable (e.g., Sales, Research & Development, Human Resources)

## Model Architecture

The model employs a neural network architecture designed to handle both binary and multiclass classification tasks simultaneously. Key components include:

- **Input Layer:** Accepts feature data.
- **Hidden Layers:** Multiple dense layers with ReLU activation, the number and size of which were subject to hyperparameter tuning.
- **Output Layer 1:** For department classification, using softmax activation to output a probability distribution across departments.
- **Output Layer 2:** For attrition prediction, using sigmoid activation to output a probability indicating the likelihood of attrition.

## Hyperparameter Tuning

Hyperparameter tuning was performed using Keras Tuner, optimizing for model performance as measured by validation loss. Parameters tuned include:

- Number of units in dense layers
- Learning rate

## Results

The model's performance was evaluated separately for each prediction task, yielding the following results:

- **Department Prediction Accuracy:** Approximately 63.27%, indicating the model correctly classifies the department for a majority of employees.
- **Attrition Prediction Accuracy:** Approximately 87.07%, suggesting high reliability in predicting whether an employee will leave.

## Improvement Suggestions

Several strategies could potentially enhance the model's predictive power, including:

- Extending hyperparameter search space
- Experimenting with deeper or more complex architectures
- Implementing regularization techniques to mitigate overfitting
- Using alternative metrics (e.g., F1 score, precision, recall) for imbalanced classes
- Further feature engineering to uncover more predictive signals

## Conclusion

The project demonstrates the feasibility of using neural networks to predict employee attrition and department classification. While achieving promising results, there remains room for improvement and optimization to increase the model's accuracy and reliability further.
