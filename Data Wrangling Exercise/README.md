# Data Wrangling Exercise

### Assignment

This exercise demonstrates programmatic wrangling of JSON data into a Pandas Dataframe to answer some basic questions about the data.

### Data

1,499 records of World Bank project data is given in JSON format, including nested key:value pairs and missing values.

### Approach

Using the json and pandas packages, the JSON data is reformatted into Pandas dataframes. Missing values are resolved by converting empty strings to NaN values, then filling the NaN values with their neighbors with the same project theme code. Summary methods are called on columns of interest to answer the business logic questions of which countries propose the most projects and which themes are most proposed.

### Reflection

With this approach, there could be any number of project themes or countries and the code would still produce correct answers to the business questions without modification. One potential risk is that a missing theme name could persist if a given project that uniquely fits a theme is lacking the theme information to start. The resolution would be to check the World Bank Website for the missing information and to confirm that the theme "code" was not mistakenly represented.
