# Statistics: Hospital Readmissions

[Python Notebook](sliderule_dsi_inferential_statistics_exercise_3.ipynb)

### Assignment

This exercise demonstrates critical evaluation of an analysis of hospital data relating hospital size to readmission rates for heart attack, heart failure, and pneumonia.

### Data

11,578 hospital records including 13 columns of data in CSV format.

### Approach

To evaluate the correlation between hospital size and readmission rate, the Spearman's coefficient was used. Pearson's correlation coefficient was disqualified, due to a lack of bivariate normality. An alternative method would be to draw permutations of logistic regressions, but without agreed upon definitions of small and large hospitals, this was also discounted. SciPy and Seaborn provided analysis and plotting tools.

### Reflection

The more statistical analysis I do, the more I learn about the power of the Central Limit Theorem and the idea of normal distribution. Many techniques are based off these foundations, and choosing a methodology to suit the data and the question of interest is paramount to scientific validity. The most eye-opening part of the experience was realizing that rigorous and agreeable use of statistical analysis is not universally found in the most important areas of decision making; this data and analysis were a part of the Affordable Care Act and had real financial implications for hospitals across the US.