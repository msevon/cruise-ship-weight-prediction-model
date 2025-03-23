Machine Learning Project - Predicting Cruise Ship Deadweight

TABLE OF CONTENTS

    Introduction
    Problem Formulation
    Methodology
    Results
    Conclusion

INTRODUCTION

Predicting cruise ship deadweight is a critical task in ship design, with significant implications for the economic viability of cruise ship ventures. The deadweight of a cruise ship affects various aspects of its operation. Employing regression models for predicting deadweight allows cruise companies to balance safety and performance standards with economic viability.

In this project, we will:

    Define the machine learning problem we aim to solve.
    Discuss the methodology, including data preparation, model selection, loss functions, and model validation.
    Analyze the results and select the most promising regression method.
    Conclude the project.

PROBLEM FORMULATION

The machine learning problem at hand is supervised learning. We aim to predict cruise ship deadweight based solely on the ship's physical dimensions. Ship size, particularly length, breadth, and draft, has a direct correlation with deadweight. Our dataset contains categorical (Name) and continuous (Length, Breadth, Draft, Deadweight) variables.

METHODOLOGY

Our dataset includes 87 data points with ship names, dimensions, and deadweight. We perform data preprocessing and cleaning, removing the "Name" column and eliminating non-alphanumeric characters. We also scale the data using the preprocessing standard scaler.

We consider ship dimensions (Length, Breadth, Draft) as essential features for predicting deadweight. A 3D plot of the data highlights the complex relationship between these dimensions and deadweight. No single dimension exhibits a significantly stronger correlation with deadweight.

We explore two regression models: Lasso Regression and Polynomial Regression.

    Lasso Regression: This model includes regularization to prevent overfitting. It can also perform feature selection by driving some feature coefficients to zero.

    Polynomial Regression: We experiment with polynomial regression of different degrees to capture non-linear relationships between features and deadweight.

For our regression problem, we use the following loss functions:

    Root-Mean Squared Error (RMSE): It gauges the average prediction error by calculating the square root of the average squared difference between actual and predicted values.

    Mean Absolute Error (MAE): It measures error magnitudes regardless of size.

    R-squared (R²): It quantifies the model's explanatory power.

We split our dataset into training (80%) and validation (20%) sets. The training set is used to train the model, while the validation set evaluates its performance. This design assesses how well the model generalizes to unseen data.

RESULTS

After testing the models, we found that the 2nd-degree Polynomial Regression performed the best. It achieved an RMSE of 1300.54, MAE of 1112.92, and an R² of 0.84 on the test dataset. This model balanced complexity and predictive accuracy effectively.

Lasso Regression and Polynomial Regression with a 4th-degree polynomial exhibited less favorable outcomes. Lasso struggled to capture data patterns, while the 4th-degree polynomial regression suffered from overfitting.

CONCLUSION

In conclusion, this machine learning project successfully predicted cruise ship deadweight based on ship dimensions. The 2nd-degree Polynomial Regression model emerged as the most promising, explaining 84% of the variance in ship deadweights. Nevertheless, there is room for improvement, particularly in mitigating overfitting and obtaining a more extensive and diverse dataset. These refinements can advance the accuracy of cruise ship deadweight prediction through machine learning.
