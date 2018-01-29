# Exploratory Data Analysis
[Notebook](https://github.com/raymondgh/springboard-data-science/blob/master/Capstone%201/ExploratoryDataAnalysis.ipynb)

## Objective

Visualizing the data enables insights beyond the summary statistics available with simple methods like .info() and .describe(). In the Exploratory Data Analysis notebook, I visualize a few attributes of interest across counties and time. It should be noted that the time-based analysis should not be treated with the same level of scrutiny as the snapshot views, as the data is _not_ time series data; there is no guarantee as too how many migrants originate and destine for a county within the year, nor how many businesses are started and closed down within the year. Only the totals are made available.

This brief exploration serves best as an overview of the data to be modeled. While a few conclusions can be drawn from the visualizations, nearly each pattern warrants additional exploration. For this summary-level analysis, exploration is kept broad and thin.


## Importing the Data

The data is imported as needed from the data/interim directory. All data has been keyed to geo_id, the unique US County and county equivalent identifier. Data is available for the years of 2005 through 2015. Analysis is done on the canonical 3,142 US counties represented in the Business Establishments and Employees files, not the divergent county lists in the population files.

## Analyzing it

The county data is overviewed for the most recent year of 2015 and for identified periods of interest representing the financial recession from 2007 through 2011 and subsequent recovery from 2011 through 2015. Visualizations are categorized into business focus, migration focus, and relationship focus.

### Business

Business data includes total number of establishments and employees for each US county for the years 2005 through 2015.

#### Snapshot 2015

![Map of Number of Establishments](images/eda1.png)

![Boxplot of Number of Establishments](images/eda2.png)

![Histogram of Number of Establishments](images/eda3.png)

#### Country-wide trends

![Line chart of Numbers of Establishments and Employees](images/eda4.png)

![Bar chart of Number of Establishments by Industry](images/eda5.png)

#### Trends within periods

![Box plot of Establishment Count Growth by Period](images/eda6.png)

![Map of Establishment Growth Rate 2005-2015](images/eda7.png)

![Map of Establishment Shrinkage Rate 2007-2011](images/eda8.png)

![Map of Establishment Growth Rate 2011-2015](images/eda9.png)

### Migration

Migration data includes totals for inflow and outflow for each county regarding each county in the dimensions of tax returns (representing a household), tax exemptions (approximating number of people), and adjusted gross income (not visualized) for the years 2005 through 2015.

#### Country-wide trends

![Line chart of Number of Exemptions Filed](images/eda10.png)

![Line chart of Number of Exemptions Filed by New Local Residents](images/eda11.png)

![Line chart of Number of Exemptions Filed by County Emigrants](images/eda12.png)

![Line chart of Percent of Exemptions Filed by County Immigrants](images/eda13.png)

#### County-local trends

![Map of County Immigration as Percent of Local Population](images/eda14.png)

![Map of County Emigration as Percent of Local Population](images/eda15.png)

![Map of County Immigration Destinations as Percent of Total Migrants](images/eda16.png)

![Map of County Emigration Origins as Percent of Total Migrants](images/eda17.png)


#### Overall

![Map of County Population Change (Positive or Negative)](images/eda18.png)

![Map of County Population Change (Growth Percent)](images/eda19.png)


### Business and Migration

Correlative analysis is kept simple for the data exploration and focus on the summary level data of total establishments and migrations.

#### Snapshot 2015

![Map of County Establishment Count Growth Rate for 2014-2015](images/eda20.png)

![Scatter Plot of Establishment Count Growth vs New Resident Percent 2015](images/eda21.png)

![Scatter Plot of 2015 Establishments Increase vs New Resident Count 2015](images/eda22.png)

![Scatter Plot of Establishment Growth vs Net Resident Growth 2015](images/eda23.png)

#### Periods

![Scatter Plot of Recession (2007-2011) Business vs Population Growth](images/eda24.png)

![Scatter Plot of Recovery (2011-2015) Business vs Population Growth](images/eda25.png)


#### Hide some outliers

![Scatter Plot of Recession (2007-2011) Business vs Population Growth (middle 80th percentile)](images/eda26.png)

![Scatter Plot of Recovery (2011-2015) Business vs Population Growth (middle 80th percentile)](images/eda27.png)


## Reflection

Whoa that was neat. how neat was that?
