# Week 11 Assignment
## Findings
After comparing three models, one where 30% of the data was used for testing, another where 50% of the data was ued for testing, and the last one where 70% was used for testing; I was able to conclude that, the higher the percentage of data dedicated to testing, the lower the accuracty of the model.

This is evident in the accuracy percentage calculations, which was derrived through:
  ```bash
  knn.score(X=X_test, y=y_test)
  ```
With that, we got the following scores for all three categories
```plaintext
20% Testing:  98.61111111111111
50% Testing:  97.55283648498332
70% Testing:  96.89984101748807
```
![image](https://github.com/user-attachments/assets/0011096e-329d-42b1-ba65-5676855ff0ad)

![image](https://github.com/user-attachments/assets/d4c8d5bf-ba4b-40b3-85b0-bf1f9f42cda8)

![image](https://github.com/user-attachments/assets/cbfa9240-ff5b-4ca2-9344-dd4c053f4172)

## Analysis
These results show, the higher the proportion of testing data, the lower the accuracy.
This makes sense, given the fact that, when performing supervised learning, one must make a tradeoff between how much of the dataset should be for training, and how much should be for testing. If the model does not have sufficient training data i.e. a majority of the data is dedicated to testing, it means that it has less information to make predicitons, and might lead to:
  1. Ovefitting - With less data to learn from, the model may not capture the underlying patterns and relationships in the data effectively. As a result, it may perform well on the training data but poorly on new, unseen data (test data). This is known as overfitting.
  2. Underfitting - The model may also end up being too simple and not capture the complexity of the data, leading to underfitting where the model performs poorly both on the training data and on the test data.
  3. Unrelaible Performance - With a small training set, the model's performance can become highly sensitive to the specific data points in the training set. Small changes in the training data can lead to significant changes in model performance. In that case, model might have high variance, which means it will perform well on some subsets of the data but poorly on others. This inconsistency can make the model unreliable.
