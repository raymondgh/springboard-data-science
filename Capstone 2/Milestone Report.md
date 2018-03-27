# Capstone 2: Milestone Report

## Problem

Who should I follow on Hackernews? Unlike popular social media platforms like Facebook and Instagram, Hackernews has no version of a "news feed," or any content customization for that matter. As the hackernews audience continues to grow, front-page content becomes increasingly general and shallow, decreasing the depth of interaction, and ultimately the value created both for users and for the Y Combinator professional network.

## Client

Y Combinator may have intentionally ignored the trend of personalized activity feeds, but the creation of a minimum-viable-product could provide actionable insights for the organization, or at least additional confidence in the existing path. Recruiters and advertisers would rejoice at the increased targeting made possible by this reorganization of data, and special-interest groups would benefit from having relevant content promoted to relevant people.

## Data

The Hacker News corpus is the only data set used for this project. The data is acquired on March 18, 2018 from [Google BigQuery](https://bigquery.cloud.google.com/dataset/bigquery-public-data:hacker_news). From here, the "full" table is exported into a private Google Cloud Storage Bucket and subsequently downloaded as 17 .CSV files. The data consists of "story" and "comment" items with associated information.

## Other Potential Data Sets

A natural parallel to the news prong of the technical community could be the "code" prong; an analysis of the networking of GitHub repositories and users could complement the hackernews dataset nicely. This could be used for user classification and profile construction, but would be limited to the instances for which a profile match could be made.

## Initial Findings

Looking at key metrics of user activity, trends can be seen that show a general shift from a communal portal for discussion toward a news portal to discuss technology news with the lens of startup culture. This is supported by significant shrinkage in number of stories submitted per active user and an corresponding increase in number of comments per story. Growth in users and stories has been nearly linear, while growth in comments has been exponential. These observations suggest that discussions are growing deeper and more thorough over time, though not growing as numerous. It also indicates an increased bar of difficulty for a submitted story to reach the ranks of the front page.

Topics of the top scoring stories from each year reveal another trend of continued focus on people and organizations over technical details. This is somewhat surprising as HN is known for its rich discussion on technical matters and even technical "one-upmanship". Most of the top threads feature stories about more generally relatable events, which makes sense, since the nuanced topics should only appeal to certain niches.

Thirdly, key words and phrases are analyzed in popularity over time. The number of mentions a keyword has can serve as an adequate measure of its topic's popularity. Expectedly, hot topics and trends come and go with some beyond their heyday and some still rising. For example, "Web 2.0" and "Prediction Market" were on their way out of the lexicon when HN was founded, while "nfc" and "crowdsourcing" have risen and fallen in popularity, and "deep learning" and "blockchain" are still on their way up.

Statistically examining the data, it's seen that there is a very strong relationship between number of comments and upvotes each story receives. It's also shown that this relationship varies by type of post; users are relatively more likely to contribute comments to the "Ask HN" threads of inquiry, and relatively more likely to contribute only upvotes to "Show HN" threads.

In summary, site content production ratios between users, stories, and comments have been found to have shifted over time, but not in a way that detracts from this project's ability focus on exploring influential commenters. The project is further supported by early findings corroborating the ability to identify topics by descriptiveness and keyword usage.

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
