# Modeling

[Notebook](Modeling.ipynb)

## Objective

To use the prepared samples to train, test, and optimize machine learning models to classify counties to predict the target variable of retail growth or non-growth.

## Methodology

Samples are imported and non-variable labels of geo_id and year are removed. The data is split 75/25 into a train and test set. The training set is fed to multiple pipelines executed by a exhaustive grid-search cross validation function to optimize the selected parameters. Sci-kit Learn's Logistic Regression function is first used with four solvers: liblinear, newton-cg, sag, and lbfgs. Despite a range of hyperparameters to try, the training confusion matrix reveals that the model is not able to effectively learn the data. There are too many false negatives. 

Before balancing the classes by weight, the recall for True outcomes is reported in the area of 0.15, and increased to 0.33 thereafter. In other words, the model is predicting a lack of retail growth in most areas. 

Examining the false negative and false positives reveals a significant distortion of predictability in the recession years on 2007-2011. Geographically, misses were widespread, though seem concentrated in the continental Central Timezone, the coastal northeast, across California.

In further analysis, years of data are excluded for a subsample analysis, though results do not improve significantly. The highest accuracy reached is 67%

## Conclusion

The nully hypothesis that there is no relationship between US domestic migration and retail growth cannot be rejected. 

## Reflection

While frustrating that I didn't find a model that reached the idealized 95-99% range of accuracy, I'm glad I had the opportunity to exercise a few techniques for improving a model when the results aren't immediately excellent. It was interesting however to see that some areas of the country were more predictable than others. With more interest in this topic, it's possible that exploration into a single state maybe be more fruitful. It's also possible that complex ensemble methods could improve the results, though with such a low starting point, I don't think it's reasonable to expect that.