# Linear Regression: Boston Housing

[Python Notebook](Mini_Project_Linear_Regression.ipynb)

### Assignment

This exercise demonstrates predictive modeling and model evaluation of Boston housing prices using a variety of factors including crime, number of bedrooms, pupil-student ratios, and more.

### Data

506 house sale records including 12 independent variables and 1 target variable loaded from SciKit Bunch object.

### Approach

Beginning with computed and visual exploratory data analysis, the factors are investigated separately and together. Statsmodels, Seaborn, SciPy, and SkLearn are the main Python packages used in this exercise. Regression through the origin is discussed with respect to sensibility of the implications as well as statistical significance. F-Statistics, T-Statistics, and AIC values are used to evaluate feature selection (and their p-values). Outliers are detected using influence and leverage plots, and the models are futher evaluated.


### Reflection

It's fun to try modeling with different features to see the effects. I found the initial one-to-one grid of scatterplots to be especially helpful in identifying interesting features and speculating on outliers. For thoroughness though, I would probably prefer to automate an exhaustive search or at least a smarter search for features than eyeballing and trialing.