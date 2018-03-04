# Springboard Capstone Report: Predicting County Business Growth
## Ray Harris
### March 4, 2018

#### Outline

- Introduction
- Data Acquisition and Cleaning
- Data Exploration
- Modeling
- Using Model and Recommendations
- Assumptions and Limitations
- Other Data and Future Work
- Conclusion

#### Introduction

[Original Proposal](Proposal.md)

**Problem**

How much will a given local economy in the US grow or shrink this year? Since the great recession, awareness of economic trends has reached an all-time high. Corporations, governments, and families strive to make more economical investments. Given the complex range of factors contributing to a town or geography's economic growth and momentum, is it possible to predict the net growth or shrinkage of employer establishments in a county? Using historical US county-to-county population migration and historical business establishment data, this study aims to build a model for predicting the change in number of employer establishments in a given US county.

**Problem**

The historical data on business growth comes from the [County Business Patterns](https://www.census.gov/data/tables/2015/econ/cbp/us-states-counties-pr-island-areas.html) report from the United States Census. This includes the number of establishments by sector in all counties from 2005 through 2015 as well as payroll information and number of paid employees. The historical data on taxpayer migration comes from the [U.S. Population Migration Data](https://www.irs.gov/statistics/soi-tax-stats-migration-data) from the United States Internal Revenue Service which comes in two formats: an older style of a zip of XLS files for 1990 through 2011, and a newer style of CSVs from 2011 through 2016. The migration data includes total inflow and outflow of tax filers by year.

#### Data Acquisition and Cleaning

**Objective**

To answer the study's core questions about the relationship between US migration and business growth, observations of counties and their attributes of business status, immigration, and emigration are needed for each year between 2005 and 2015. 

**Importing Raw Data**

[County Business Patterns data](https://www.census.gov/data/tables/2015/econ/cbp/us-states-counties-pr-island-areas.html) was acquired by downloading 11 CSV files from the census website, selecting all optional columns to be included. Each was read into a dataframe and columns renamed to remove punctuation. 

[U.S. Population Migration Data](https://www.irs.gov/statistics/soi-tax-stats-migration-data) was aquired by downloading 4 CSV files and 7 ZIP files including 102 XLS files each. These files were further segmented into three different data formats for parsing, and four different filename formats for gathering for batch processing. Unlike the County Business Patterns data, the only year-identifying information in the migration data was found in the filenames. To add this information to the dataframes, dictionaries of years and lists of files were created and iterated over as tuples using the .items() method.

**Diagnosing Issues**

Missing values were initially identified by comparing the resulting dataframe shapes and uniques before concatenating them, typically by year. To determine how to handle changes in county districting from 2005 to 2015, the [US Census Bureau](https://www.census.gov/geo/reference/county-changes.html) was consulted. Based on this information, some counties had missing values filled with 0s and some were backfilled. The census bureau also witholds employee count information when values are low enough to reveal personally identifiable information (less than 10); these missing values were converted to 0s.

Some unidentified county GeoIDs were also discovered by visually examining the data. There is no state with a FIPS code of 97 (most are between 1 and 50). Exploration of the data [documentation](https://www.irs.gov/pub/irs-soi/1415inpublicmigdoc.pdf) indicates that summary data is included inline and formatted with unused GeoIDs. These were filtered out accordingly.

**Tidying Data**

The unique identifier was determined to be a "Geo ID" which is a combination of a State FIPS code and a County FIPS code. This information is found on a [Census Help Page](https://www.census.gov/geo/reference/geoidentifiers.html) and [Glossary](https://www.census.gov/programs-surveys/metro-micro/about/glossary.html). While much more information is available including various CBSAs (combined statistical areas) that are grouped by economic exchange, this can ultimately be described as derivative. GeoIDs were also normalized into 5-digit strings (two for state, two for county).

Data was ultimately pivoted into multi-index dataframes, dropping unneeded columns and filling remaining null values with 0. Lastly, data is saved to three CSV files in the "/data/interim/" folder. However, these files are over the GitHub filesize maximum of 100MB and are added to the .gitignore file.
