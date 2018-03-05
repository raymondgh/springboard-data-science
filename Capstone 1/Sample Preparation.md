# Sample Preparation
[Notebook](Sample%20Preparation.ipynb)

## Objective

To prepare the canonical data for modeling, interim data is concatenated and simplified into a single CSV file.

## Methodology

A target variable is created as the boolean comparison of a year's business establishment count to the previous year's count. The inflow and outflow data from the IRS is combined with the business data frame with the growth target variable for a completed data set. In the migration data, per-county immigration is simplified from 3,142 counties to in-state and out-of-state to counter the irrelevance of in-state data to each of the other 49 states. In other words, since each state is likely to be most affected by in-state migration, and data from another state is likely only to severely affect its own state, migration data is normalized to in and out of state. Without this modification, more populous states and states with greater volumes of migration would outweigh counties in smaller, less populous states across the entire nation, despite those smaller counties informative value to their immediate neighbors.

## Conclusion

The csv file is saved with ten years of samples for 3,142 counties with 1 target variable and 17 explanatory variables.

## Reflection

Initially, I had planned to use the same notebook for this process and for modelling, but performance considerations and readability complications encouraged the decision to break it apart. I'm concerned with the data format as it relates to the original proposal, as immigration from in and out of state is far less interesting than from each and every county. On the other hand, this reduction makes it much easier to feed the data into machine learning algorithms. 