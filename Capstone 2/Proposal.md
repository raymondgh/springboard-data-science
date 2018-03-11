# Capstone Project Proposal

### Problem

Who should I follow on Hackernews? Unlike popular social media platforms like Facebook and Instagram, Hackernews has no version of a "news feed," or any content customization for that matter. As the hackernews audience continues to grow, front-page content becomes increasingly general and shallow, decreasing the depth of interaction, and ultimately the value created both for users and for the Y Combinator professional network.

### Client

Y Combinator may have intentionally ignored the trend of personalized activity feeds, but the creation of a minimum-viable-mvp could provide actionable insights for the organization, or at least additional confidence in the existing path. Recruiters and advertisers would rejoice at the increased targeting made possible by this reorganization of data, and special-interest groups would benefit from having relevant content promoted to relevant people.

### Data

The Hacker News corpus will be the only data source for this exploration. A Kaggle user has aggregated the data from 2006 through 2017 [Kaggle BigQuery](https://www.kaggle.com/hacker-news/hacker-news) and if necessary, the [HackerNews API](https://github.com/HackerNews/API) can be used to pull additional content. 

### Approach

To create a content recommendation engine, a multi-step process is necessary. First, popular submissions and comments will be clustered into topics. Second, influential users will be identified for those topics. Thirdly, a recommender will be created that suggests influential users to a given user of interest.

### Deliverables

1. Code (notebooks)
2. Written report of findings
3. Summary presentation
