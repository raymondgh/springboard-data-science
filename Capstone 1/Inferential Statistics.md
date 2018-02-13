# Inferential Statistics
[Notebook](Inferential%20Statistics.ipynb)

## Objective

To explore the significance of a few observations from the exploratory data analysis, selected metrics are evaluated against measures of statistical significance. In particular, this analysis aims to corroborate the hypothesis that increased immigration leads to increased growth in retail establishments.

## Methodology

Distributions of county populations and retail establishment counts are provided for context, showing exagerrated exponential distributions. Following which, a regression plot confirms that the data are linearly correlated. To answer the study's main question, growth statistics are calculated as the difference between number of establishments and county populations for two consecutive years. This relationship is explored across all 10 years, and across pairs of years. The Pearson Correlation Coefficient is selected to measure the correlation between the values, showing that nearly all years have significant correlations. Finally, county immigration is compared to emigration to confirm that a county's base population is the key determining factor in predicting volume of tax-payer flow. Outliers of residual calculations are highlighted as well.

## Conclusion

Unexpectedly, the correlation across all 10 years of change was found only to be -0.02 between population change and retail establishment change. Examining by year revealed the phenomenon of every year displaying a positive correlation except for 2008 and 2009, which showed strong negative correlations. An interpretation would be that when the economy is growing, more people means more business establishments, and that when the economy is in recession, more people means fewer business establishments. This raises the question of whether people are attracted to economies or economies are generated by people. Perhaps migrants are making their decisions to move with incomplete or substandard information during economic recession. 

Looking deeper at the relationship between county immigration and emigration, it can be seen that the bigger the county, the more the churn. While that's true, a handful of outliers were identified, representing counties with the greatest "unexpected" population growth and shrinkage. Interestingly, Los Angeles County, previously seen as the US's largest county by headcount, is also the most unexpectedly deserted county for a number of years. The areas of New Orleans and Chicago also suffered major losses, Chicago's Cook County being the US's second largest county by headcount. On the positive side, the areas of Riverside CA, Phoenix AZ (of US's fourth largest county, Maricopa, AZ), and Austin, TX (Of Travis County, TX) experienced the greatest unexpected growth.

## Reflection

As expected, this dataset still has many relationships to explore and uncover. Not as expected, the correlation between population and growth is reversed during different economic cycles! That's certainly interesting and deserves further exploration. It's likely that outside factors beyond a shallow understanding of establishment and population counts affect these relationships. It can also be seen that the correlation accelerates in growth over time during strong financial periods. It's possible that this relationship itself is a predictor of economic trends, though data going further back in time would be needed for that analysis. However, the multi-year trends imply that predicting one year's economic changes may require data from more than just the previous year, as previously wondered.