# econ3916-lab19-random-forests

# Tree-Based Models: Random Forests

## Objective

The goal of this lab was to compare decision trees, random forests, OLS, and Ridge regression to see how well they predict California house values. I also wanted to understand how feature importance and hyperparameter tuning can affect model performance.

## Methodology

- I used the California Housing dataset, which contains 20,640 observations and 8 features.
- I split the data into training and test sets and compared a single decision tree, OLS, Ridge regression, and random forest.
- I evaluated the models using training and test R² and RMSE to see how well they performed and whether they were overfitting.
- I compared MDI and permutation importance to see which features were most important for predicting house values.
- I used 3-fold cross-validation to tune the random forest's `max_depth` and `max_features`.
- I used AI to create a function called `importance_chart()` that calculates permutation importance and displays the top features in a horizontal bar chart.
- I completed two rounds of AI prompting and checked the function's results against Step 3 for different values of k and another decision tree model.

## Key Findings

The single decision tree had a training R² of 1.0000 but a test R² of 0.6228, which showed that it was overfitting the training data. Ridge regression had a test R² of 0.5758, while the random forest performed better with a test R² of 0.8046. This suggests that random forests are better at capturing nonlinear relationships between the features and house values.

When I compared feature importance, I found that MedInc was the most important feature. Latitude had an MDI importance of 0.0890 but a permutation importance of 0.4427. This showed that the two methods can rank features differently because they measure importance in different ways.

After tuning the random forest using cross-validation, the test R² increased from 0.8046 to 0.8094. The best settings were `max_depth=None` and `max_features=0.5`. This showed that changing the number of features considered at each split could improve the model's performance.

For the AI-Assisted Expansion, I completed two rounds of prompting. In the first round, I asked AI to create a function that calculates permutation importance and makes a horizontal bar chart. In the second round, I asked it to add a check for invalid k values. Both rounds passed the notebook's checks, and the importance values matched Step 3 exactly, with a 0% difference. The function also worked with a different decision tree model and reversed feature columns.

Overall, this lab helped me understand why random forests can perform better than individual decision trees and linear regression models. I also learned that feature importance depends on how it is calculated and that AI-generated code should be checked against results we already know.
