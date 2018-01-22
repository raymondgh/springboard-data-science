# Case Study: Investigating a Drop in User Engagement
_Note: this data is fake and was generated for the purpose of this case study. It is similar in structure to Yammer’s actual data, but for privacy and security reasons it is not real._

SQL Code for my solution can be seen on [Mode](https://modeanalytics.com/editor/raymondgh/reports/034563872c01)

### The Problem

> You show up to work Tuesday morning, September 2, 2014. The head of the Product team walks over to your desk and asks you what you think about the latest activity on the user engagement dashboards. You fire them up, and something immediately jumps out:

![Weekly Active Users](wau.png)

### Hypotheses

We want to know why user engagement has dropped. We'd know already if our servers went down, so a few deeper questions should be asked. Here are some ideas why we might have experienced the drop:

 - A client switched to a competitor along with all their users
 - A new feature was pushed that discourages some segment of users
 - The drop is within normal cyclical activity trends
 - A special promotion or incentive recently ended
 - The service launched on another platform that isn't represented here
 - A large source of traffic dropped in popularity
 - Dropoff was normal but new signups lagged


### Digging In

We are given four tables with a few fields each to analyze the situation. I start be examining some summary information, and continue by drilling down on user engagement to find patterns.

#### What does the distribution of users look like?

Showing the top 50 largest companies [SQL](https://modeanalytics.com/raymondgh/reports/034563872c01/queries/69c109d3e756)

![Weekly Active Users](users-company.png)

#### How many new signups have we had?

By day [SQL](https://modeanalytics.com/raymondgh/reports/034563872c01/queries/8f841912a9a4)

![Weekly Active Users](signups.png)

#### Are major changes to user engagement localized to one subgroup?

By Company [SQL](https://modeanalytics.com/raymondgh/reports/034563872c01/queries/51a8b3fe3869)

![Weekly Active Users](wau-company.png)

By Device Type [SQL](https://modeanalytics.com/raymondgh/reports/034563872c01/queries/c7080b92553c)

![Weekly Active Users](wau-device.png)

By Language [SQL](https://modeanalytics.com/raymondgh/reports/034563872c01/queries/195d636fb981)

![Weekly Active Users](wau-language.png)

By Signup Date [SQL](https://modeanalytics.com/raymondgh/reports/034563872c01/queries/16686f890caf)

![Weekly Active Users](wau-signup.png)


#### Have there been any changes to our email strategy or success?

All events on one chart [SQL](https://modeanalytics.com/raymondgh/reports/034563872c01/queries/764bf5bb39e2)
![Weekly Active Users](email.png)



### Recommendation

 - Further questions & how to answer
 - Questions beyond data & how to answer them
 - Most likely cause of engagement dip
 - What the company should do
