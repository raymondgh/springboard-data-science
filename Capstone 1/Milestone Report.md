# Capstone 1: Milestone Report

## Problem

Which local economies in the US grow and shrink next year? Since the great recession, awareness of economic trends has reached an all-time high. Corporations, governments, and families strive to make more economical investments. Using historical US county-to-county population migration and historical business establishment data, this study aims to build a model for predicting whether a county will see an increase or decrease in retail establishments as a proxy measure for overall economic health of a county.

## Client

Small business-focused solutions providers such as Intuit, Xero, Zenefits, Gusto, and more can use such a model to predict where marketing investments will be more effective. They can segment their audiences geographically and invest accordingly. Families seeking to move can use such a model to predict where job growth is likely to occur. They could also avoid moving to a county where a superficially attractive county could have a high likelihood of decline or stagnation. Local governments could use this data as a starting point to identify successful counties worthy of emulating.

## Data

[County Business Patterns data](https://www.census.gov/data/tables/2015/econ/cbp/us-states-counties-pr-island-areas.html) was acquired by downloading 11 CSV files from the census data explorer website. [U.S. Population Migration Data](https://www.irs.gov/statistics/soi-tax-stats-migration-data) was aquired by downloading 4 CSV files and 714 XLS files. These files were further segmented by document layouts and filename formats. To determine how to handle changes in county districting from 2005 to 2015, the [US Census Bureau](https://www.census.gov/geo/reference/county-changes.html) was consulted. Based on this information, some counties had missing values filled with 0s and others were backfilled. Summary statistics of statewide, regional, and nationwide totals were also removed

County "Geo IDs," a combination of a State FIPS code and a County FIPS code, were selected as unique observation identifiers as per a [Census Help Page](https://www.census.gov/geo/reference/geoidentifiers.html) and [Glossary](https://www.census.gov/programs-surveys/metro-micro/about/glossary.html). Data was ultimately pivoted into multi-index dataframes, dropping unneeded columns and filling remaining null values with 0. Lastly, data is saved to eight CSV files in the "/data/interim/" folder. 

## Other Potential Data Sets

A county's economic growth would ideally be measured by its gross domestic product, however, such figures are not available. Nor is it widely agreed upon what factors contribute to GDP growth. Population is understood to be a factor, but not the only one. Complexity of regulations could inhibit or enable entrepreneurship. Exact geographical details could afford or preclude commercial zoning. Overall culture, natural resources, climate, access to local and foreign markets, and education could all play parts in determining economic growth. 

Of these suggested factors, perhaps data such as average temperature, graduation rates, and proximity to larger populations would be most accessible and informative.


## Initial Findings

From basic summary analysis, it becomes immediately clear that the recent recession was most impactful on local businesses in the years from 2007 through 2011, when the number of establishments decreased year-over-year. Following this recession, new establishments that sprung up were found in different industries; there was a significant decrease in construction establishments and a corresponding increase in professional, technical, and food service establishments.

Throughout the entire dataset, Texas was found to hold the most counties with very high population growth. Of the non-urban counties, a band of western states all exhibited growth, as well as a few areas in the south east. Contrasting with each other, western states featured a mix of shrinkage and growth, implying local consolidation, whereas Florida experienced state-wide growth, implying nationwide attraction.

During the recession, a significant drop in tax filings was found, as well as an overall decrease in mobility. For every year, a strong correlation was found between net population change and net retail establishment count change, however, in the two years of 2008 and 2009, the correlation was reversed: instead of population increase correlating with business increase, population increase correlated with population decrease. The interpretation of this phenomenon is yet unclear. 

In summary, population and retail trade have been found to be strongly linked, but the ability to predict retail trade growth will depend on more detailed data than the summary data of net changes.

## Code

Proposal
 - [Read Me](Proposal.md)

Data Wrangling
 - [Read Me](Data%20Wrangling.md)
 - [Python Notebook](Data%20Wrangling.ipynb)

Exploratory Data Analysis
 - [Read Me](Exploratory%20Data%20Analysis.md)
 - [Python Notebook](Exploratory%20Data%20Analysis.ipynb)

Inferential Statistics
 - [Read Me](Inferential%20Statistics.md)
 - [Python Notebook](Inferential%20Statistics.ipynb)