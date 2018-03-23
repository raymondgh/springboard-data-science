# Take Home Challenge - Relax Inc.

[Python Notebook](Relax%20Inc.ipynb)

### Assignment

A take-home assignment asking to determine the most influential factors in determining whether a software user will "adopt" the product by meeting an activation criteria of 3 visits in one week.

### Data

12,000 user records with origin data and some basic information in CSV format. 20,7917 login records with timestamps and user IDs in CSV format.

### Approach

First, a target variable column is created based on the definition of "3 visits in one week" by finding the number of visits within 7 days of each visit, then merging the data into the users table. Next, data is cleaned and missing values filled in. Exploratory data analysis shows a few basic differences in adoption rates by feature before modeling. To model the data, dummies are generated for non-numerical feature of signup origin and a irrelevant columns are dropped. 

With an imbalanced data set like this one, simply telling the model to weigh features by class volume was not sufficient to yield accurate predictions. The SMOTE synthetic oversampling technique is used. Furthermore, it is shown that logistic regression is far inferior to random forest for this data, presumably because all of the explanatory variables are binary classes rather than continuous values.

### Reflection

This assignment was a great way to see the importance of resampling as a solution to imbalanced data. It's a little disappointing that the machine learning model could not provide much more insightful prioritization of features, but I believe that with an improved model, it could be used as part of a growth or revenue prediction pipeline in which user adoption is a key factor. 
