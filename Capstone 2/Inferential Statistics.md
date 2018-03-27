# Inferential Statistics
[Notebook](Inferential%20Statistics.ipynb)

## Objective

To dive a bit deeper into the the hackernews data, the relationship between a story's score and its generated discussion is examined. In particular, this study should answer whether upvotes and comments are produced by users at a different rate for three different types of content: links, Ask HN's, and Show HN's.

## Methodology

Distributions of story properties of descendants and scores are shown. Descendants is a measure of how many comments were added by users in association with the story, including comments referencing other comments. Score is a measure of how many upvotes a story received. From two simple distribution plots, it can be seen that the vast majority of stories submitted to hackernews are ignored by most users. There is an exponential distribution whereby most stories have no comments and few have very many, likewise with points.

With 2.8 million entries, rendering a scatterplot is not feasible. Instead, a hexbin is plotted that simplifies the data by binning it into 80 bins along the x axis with a corresponding number of bins (based on the data) to maintain hexagon regularity. 

Strong relationships are seen across all three types of content. The Pearson coefficient measures a positive correlation of 0.82, 0.81, and 0.80 for links, show, and ask type stories. 


## Conclusion

The sheer quantity of content posted to hackernews that goes without votes or replies is astounding. When browsing the main website, users will only encounter the top ranked posts under normal circumstances. It has been seen as an achievement to have self-produced content reach the front of hackernews, and the data strongly supports that. On the other hand, much of it could be spam, though it seems unlikely, as spam is not a major issue on the site.

The correlation between replies and upvotes is unsurprisingly strong, though it is noteworthy that the personal threads of "Ask" and "Show" HN threads appear to have less variance by visual inspection. Relationally, "Ask HN" threads generate most comments, "Show HN" threads generate fewest comments, and linked stories generate a wide range of comments per upvote.

## Reflection

This portion didn't reveal any mind blowing insights, but it did provide a foundation upon which more questions can be asked. What is the deviation from the norm? What factors predict deviation? How can these further insights be used to optimize a newly posted HN thread aimed at the front page? My expectation would be that most of the variance in a post's "success" is determined by the content, and little can be done to improve the presentation on hackernews, though analyzing sentiment in thread documents could reveal relationships between positive/negative sentiment and various properties of a post also revealed by the comments.