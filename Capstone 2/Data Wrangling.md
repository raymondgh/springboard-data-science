# Data Wrangling
[Notebook](Data%20Wrangling.ipynb)

### Objective

The dataset involved in this project is over 6GB in size and grows every single day. To achieve the project objective, the data must be collected and cleaned for programmatic consumption.

### Importing Raw Data

The Hacker News corpus is the only data source for this exploration. A Kaggle user has aggregated the data from 2006 through 2017 [Kaggle BigQuery](https://www.kaggle.com/hacker-news/hacker-news) which is accesible freely from Google at their [BigQuery Repository](https://cloud.google.com/bigquery/public-data/hacker-news). Data is exported to a private Google Cloud Storage within the free tier of usage and segmented into 17 CSV files about 350 MB each. Finally, the data is downloaded in Python with the urllib.request library.

### Diagnosing Issues

The dataset is already well-kept and contains few missing values. The greatest source of errors were missing values caused by content deletion, a power any hackernews user has over their own content. The ID and Parent ID fields are cast to integers for easy comparison, and the text bodies of the comments are parsed to remove HTML elements, as the hackernews API provides comments as html, which is not subsequenty parsed by the user maintaining the Google Big Query data store.

### Tidying Data

Each row is one observation of a content item on the website: either a story or a comment. The properties for these two types of content are identical, so it is reasonable to keep them in the same dataframes. Furthermore, it's useful to maintain them this way as the only reference between children and parent nodes in nested discussions are in the ID and Parent ID fields.

### Reflection

Unlike my previous project, wrangling this dataset was a breeze! Most of the work was done for me but a new challenge of scale was presented. Maintaining and managing 6GB of data in memory is not practical for most machines, and under additional constraints, new techniques would be required, such as loading processing data by line for major operations.

