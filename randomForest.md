# Random forest:
- Random : Bagging (Bootstraped aggregation)
  - Bagging --> Decision trees.
  - Bootstraped ---> sampling.
  - Sampling:
    - Row sampling-----}
    - Column sampling  } ----> With replacement(repeatation involves) & without replacement (no repeatation)
    - Combination------}
- Forest : Group of trees.

- Bagging:
  - Consider there are n observations and m features in the training set. You need to select a random sample from the training dataset .
 
---

## Algorithm:
- Random Forest is a classifier that contains a number of decision trees on various subsets of the given dataset and takes the average to
  improve the predictive accuracy of that dataset.
-  It is a supervised learning technique.
-  It can be used for both Classification and Regression problems.
-  The greater number of trees in the forest leads to higher accuracy and prevents the problem of overfitting.

<img width="476" alt="image" src="https://github.com/pilipi-puu-puu/Machine-Learning/assets/87390353/86c942d9-d176-4b99-a457-f3f5559f3b5b">

## Why use random forest?
- It takes less training time as compared to other algorithms.
- It predicts output with high accuracy, even for the large dataset it runs efficiently.
- It can also maintain accuracy when a large proportion of data is missing.

## Steps:
- Step-1: Select random K data points from the training set.
- Step-2: Build the decision trees associated with the selected data points (Subsets).
- Step-3: Choose the number N for decision trees that you want to build.
- Step-4: Repeat Step 1 & 2.
- Step-5: For new data points, find the predictions of each decision tree, and assign the new data points to the category that wins the majority votes.

## Applications:
- Banking: Banking sector mostly uses this algorithm for the identification of loan risk.
- Medicine: With the help of this algorithm, disease trends and risks of the disease can be identified.
- Land Use: We can identify the areas of similar land use by this algorithm.
- Marketing: Marketing trends can be identified using this algorithm.

## Disadvantage:
- Although random forest can be used for both classification and regression tasks, it is not more suitable for Regression tasks.

## Implementation in my project:
```py
step1 = ColumnTransformer(transformers=[
    ('col_tnf',OneHotEncoder(sparse=False,drop='first'),[0,1,7,10,11])
],remainder='passthrough')

step2 = RandomForestRegressor(n_estimators=100,
                              random_state=3,
                              max_samples=0.5,
                              max_features=0.75,
                              max_depth=15)

pipe = Pipeline([
    ('step1',step1),
    ('step2',step2)
])

pipe.fit(X_train,y_train)

y_pred = pipe.predict(X_test)

print('R2 score',r2_score(y_test,y_pred))
print('MAE',mean_absolute_error(y_test,y_pred))
```
