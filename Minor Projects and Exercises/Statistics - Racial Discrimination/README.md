# Statistics: Racial Discrimination

[Python Notebook](sliderule_dsi_inferential_statistics_exercise_2.ipynb)

### Assignment

This exercise demonstrates statistical analysis of a sample of 4870 job applications to explore the relationship between the apparent race of an applicant and the probability of getting a call back from the employer.

### Data

4870 job applications with 65 columns of details in a Stata DTA file

### Approach

Using SciPy and Matplotlib, a Chi-Squared Goodness of Fit test is applied to the data. The null hypothesis assumes applicants with black-sounding names will have the same probability of employer calls as applicants with white-sounding names. A visualization is given to help explain the interpretation of the chi-squared test results.

### Reflection

This was my first statistical hypothesis testing with categorical data. It's simplified to only one degree of freedom, but the approach wouldn't change with more variety of outcomes beyond "call/no call". As with the first Springboard statistic exercise, I found outside resources helpful.

 - [Greg Hamel on Chi-Squared Tests](http://hamelg.blogspot.com/2015/11/python-for-data-analysis-part-25-chi.html)