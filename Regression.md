# Regression
- Independent variables:
The independent variables, also known as explanatory variables, can be seen as the causes of those states. The independent variables are shown conventionally by X.
- Dependent variable:
 The dependent variable can be seen as the state, target, or final goal we study and try to predict. The dependent variable is notated by Y.

---
## Types:
### - Simple Regression:
  - Simple linear regression.
  - Simple non-linear regression.
### - Multiple Regression:
  - Multiple linear regression.
  - Multiple non-linear regression.

---

## Applications:
- Sales forecasting
- Satisfaction analysis
- Price estimation
- Employment income
---

## Regression Algorithms:
- Ordinal Regression
- Poisson regression
- Fast forest quantile regression
- Linear, Polynomial, Lasso, Stepwise,Ridge regression
- Bayesian linear regression
- Neural network regression
- Decision forest regression
- Boosted forest regression
- KNN (K-nearest neighbours)

---

## Simple linear Regression :
Simple linear regression is when one independent variable is used to estimate a dependent variable. For example, predicting Co2 emission using the engine size variable.

---
y^ = theta(0)+ theta(1)x1  **(Here theta(0) and theta(1) are the coefficient of the fit line of simple linear regression)**

                
## Pros:
- Very fast
- No parameter tuning
- Easy to understand and highly interpretable.

---

## Multiple linear Regression :
When more than one independent variable is present the process is called multiple linear regression. For example, predicting Co2 emission using engine size and cylinders of cars.

---

## Model Evaluation in Regression Models:
- Approaches:
  - Train and test on the same data.
  - Train/Test split 

---
### Train and test on the same data :

- Training accuracy:
  - High training accuracy isn't necessarily a good thing.
  - Result of over-fitting.
    -  **Over-fit** : The model is overly trained to the dataset, which may capture
    - noise and produce a non-generalized model.

- Out-of-Sample Accuracy:
  - It's important that our models have a high,out of sample accuracy.

**To overcome the out of sample accuracy , we have Test split approach.**

---
## How to use K-fold cross-validation?
- K-Fold Cross Validation In this method, we split the data-set into k number of subsets(known as folds) then we perform training on the all
the subsets but leave one(k-1) subset for the evaluation of the trained model.

```python
from sklearn import cross_validation
 
# value of K is 10.
data = cross_validation.KFold(len(train_set), n_folds=10, indices=False)
```

<img width="464" alt="image" src="https://github.com/pilipi-puu-puu/Machine-Learning/assets/87390353/93270fa2-f9d3-4a14-a6f8-8e5761ebe6fc">







