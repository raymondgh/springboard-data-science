# Logisit Regression: Heights and Weights

[Python Notebook](Mini_Project_Logistic_Regression.ipynb)

### Assignment

This exercise demonstrates basic logistic regression techniques and accuracy scoring for the prediction of gender from height and weight data.

### Data

10000 gender-labeled height and weight measurements in a clean CSV format.

### Approach

Data is folded into test and training sets for model hyperparameter tuning. CV Score, Logistic Regression, and Grid Search are used to maximize accuracy for the regularization parameter. 

### Reflection

Logistic regression is really the more approachable type of machine learning for beginners. The simple tasks of creating and testing models was quick. The bulk of the lesson for this exercise came from the explanations of the math behind logistic regression and the interpretation. The concept of generative classifier was also introduced, but it was just a link to the Wikipedia page. Some quick googling found great descriptions of the differences between p(x,y) and p(y|x) though! Apparently discriminative models generally outperform generative models on classification tasks (ex: is this animal an elephant or a dog?), but generative models can give better similarity rankings (ie: does this animal look more like a dog or an elephant).