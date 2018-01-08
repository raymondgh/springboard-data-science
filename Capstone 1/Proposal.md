# Capstone Project Proposal

### Problem

How much will a local United States economy grow or shrink this year? Since the great recession, awareness of economic trends has reached an all-time high. Corporations, governments, and families are all striving to make more economical investments. Given the complex range of factors contributing to a town or geography's economic growth and momentum, is it possible to predict the net growth or shrinkage of employer establishments in a county? Using historical US county migration and business establishment data, this study aims to build a model for predicting the change in number of employer establishments in a given US county.

### Client

Small business-focused solutions providers such as Intuit, Xero, Zenefits, Gusto, and more can use such a model to predict where marketing investments will be more effective. They can segment their audiences geographically and act accordingly. Families seeking to move can use such a model to predict where job growth is likely to occur. They could also avoid moving to a county where a superficially attractive county could have a high likelihood of decline or stagnation. Local governments could use this data as a starting point to evaluating growth opportunities and strategies of neighboring counties and towns.

### Data

The historical data on business growth comes from the [County Business Patterns](https://www.census.gov/programs-surveys/cbp.html) report from the United States Census. This includes the number of establishments by sector in all counties from 2005 through 2015 as well as payroll information and number of paid employees. The historical data on taxpayer migration comes from the [U.S. Population Migration Data](https://www.irs.gov/statistics/soi-tax-stats-migration-data) from the United States Internal Revenue Service which comes in two formats: an older style of a zip of XLS files for 1990 through 2011, and a newer style of CSVs from 2011 through 2016. The migration data includes total inflow and outflow of tax filers by year.

### Approach

To predict the growth or shrinkage of a US county's number of established firms, a regression algorithm will be used. A basic exploration will include an overview of the fastest and slowest growing and shrinking economies, a plot of net flow of taxpayers against net change in businesses, and breakdown by industry. It's possible that neighboring counties affect each other, and also that the specific destinations and origins of migrants correlate correlate differently with economic trends. Furthermore, it could be seen that business growth follows population growth subsequently in time (years) at different rates of reaction

### Deliverables

1. Code (notebooks)
2. Written report of findings
3. Summary presentation
