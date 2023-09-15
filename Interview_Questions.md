# Interview questions: (Taken from Medium)
- What is Regression?
- What are the Types of regression?
- Explain the assumptions of Linear regression.
- How to evaluate regression models?
- Explain different types of model Testing methods.
- Explain Benefits of cross validation?
- What is overfitting?
- What are different ways to fix overfitting?
- How to handle imbalanced data in a dataset?
- What to do if your data is skewed?
- What if your data has outliers, how to identify and different ways to fix?
- What is difference between lasso and ridge regression?
- What is cross entropy?
- Difference between precision and recall?
- What is a confusion matrix?
- What is AUC?
- What is bias variance trade-off?
- What is correlation? How is it related to covariance?
- What are activation function? Explain different Types? Where and why it is used? Sigmoid vs tan h vs relu?
- What is classification?
- How to evaluate classification models?
- What are ensemble models?
- What is clustering?
- What are types of clustering?
- How to decide the K in k means clustering? Can we automate it? If yes how?
- What is hypothesis testing?
- What is A/B testing?
- How does time series work? Explain how to approach a time series problem step by step.
- How do you treat seasonality in time series?
- What to do if your time series data is not stationary?
- Difference between ARIMA and SARIMA?
- What is auto correlation?
- Can we use deep learning for time series forecasting? If yes what models to use? How do they work?
- What is null hypothesis?
- What is PCA? Why do we use? What alternatives are there?
- What is bagging and boosting? Explain xgboost?

---

## Answers:
## 1. What is regression?
- In machine learning, regression is a type of supervised learning algorithm that is used to predict a continuous numerical value or output based on input data. It is 
  particularly useful when we want to establish a relationship between independent variables (features) and a dependent variable (target) where the target variable is a 
  real number.
- The goal of regression is to find a mathematical function or model that best represents the relationship between the input features and the target variable.

## 2. What are the types of regression?
- Simple Linear Regression
    - Involves one independent variable and one dependent variable, assuming a linear relationship between them.
- Multiple linear regression
    - Extends simple linear regression to include multiple independent variables, allowing for more complex modeling of relationships.
- Logistic regression
    - Despite its name, logistic regression is used for classification tasks. It models the probability of a binary outcome and uses a logistic (Sigmoid) function.
 
## 3. Explain the assumptions of Linear regression.
- **Linearity**: The relationship between X and the mean of Y is linear.
- **Homoscedasticity**: The variance of residual is the same for any value of X.
- **Independence**: Observations are independent of each other.
- **Normality**: For any fixed value of X, Y is normally distributed.


## 4. How to evaluate regression models?
- R Square/Adjusted R Square
- Mean Square Error(MSE)/Root Mean Square Error(RMSE)
- Mean Absolute Error(MAE)

---

- R squared

![image](https://github.com/pilipi-puu-puu/Machine-Learning/assets/87390353/a4b36b5c-2027-40d7-94f7-4732d474a360)


- MAE
  
![image](https://github.com/pilipi-puu-puu/Machine-Learning/assets/87390353/c78d4772-56dd-42fc-86c2-1bb0e970589e)


- MSE
  
![image](https://github.com/pilipi-puu-puu/Machine-Learning/assets/87390353/f2600d32-18cf-4354-a2aa-afc286042b10)


- RMSE
  
![image](https://github.com/pilipi-puu-puu/Machine-Learning/assets/87390353/6bd4b198-a0ce-4ed0-a757-b228e16c90a1)


## 5. Explain different types of model Testing methods.
- Unit test: Check the correctness of individual model components.
- Regression test: Check whether the model breaks and test for previously encountered bugs.
- Integration test: Check whether the different components work with each other within your machine learning pipeline.

## 6. Explain Benefits of cross validation?
- Overcoming Overfitting: Cross validation helps to prevent overfitting by providing a more robust estimate of the model’s performance on unseen data.
- Model Selection: Cross validation can be used to compare different models and select the one that performs the best on average.
- Data Efficient: Cross validation allows the use of all the available data for both training and validation, making it a more data-efficient method compared
  to traditional validation techniques.

## 7. What is overfitting and underfitting?
### Overfitting:
  - A statistical model is said to be overfitted when the model does not make accurate predictions on testing data. When a model gets trained with so much data, it starts      learning from the noise and inaccurate data entries in the data set. And when testing with test data results in High variance. Then the model does not categorize the       data correctly.
- Reasons:
  -  High variance (variance is the error due to the model’s sensitivity to fluctuations in the training data) and low bias (Bias refers to the error due to overly         
     simplistic assumptions in the learning algorithm).
  - The model is too complex.
  - The size of the training data.
 
- Techniques to Reduce Overfitting
  - Increase training data.
  - Reduce model complexity.
  - Use dropout for neural networks to tackle overfitting.

### Underfitting:
- A statistical model or a machine learning algorithm is said to have underfitting when a model is too simple to capture data complexities. It represents the inability of 
  the model to learn the training data effectively result in poor performance both on the training and testing data.
  
- Reasons:
  - High bias and low variance.
  - The model is too simple
  - The size of the training dataset used is not enough
  - Features are not scaled.

- Techniques to Reduce Underfitting
  - Increase model complexity.
  - Increase the number of features, performing feature engineering.
  - Remove noise from the data.

## 8. What to do if your data is skewed?
**Note:Skewness is the degree of asymmetry of a distribution. A distribution is symmetric if it is centred around its mean and the left and right sides are mirror images of each other. A distribution is skewed if it is not symmetric**

- Log Transformation
- Feature Engineering
- Resampling Techniques:
  - Oversampling: Increase the number of instances in the minority class by replicating existing samples or generating synthetic samples.
  - Undersampling: Reduce the number of instances in the majority class to balance class distribution.
