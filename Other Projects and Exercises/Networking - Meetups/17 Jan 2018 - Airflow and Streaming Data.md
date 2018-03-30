## Airflow, Streaming and More Meetup
January 17th, 2018 @ Lyft HQ

### Atmosphere
I found the [SF Big Analytics](https://www.meetup.com/SF-Big-Analytics/events/246039241/) meetup group on Meetup.com after searching for data science. It turned out that the event was specialized for Data Engineering, which was very exciting. How can we use programming to abstract away the more tedious aspects of data science?

The event was at Lyft headquarters. The office was hidden in a semi-secret office park in SoMa near AT&T park. I think it would be a nice place to work! When I got there I found the usual fare: pizza and beer. I found it to be much more crowded than expected; there weren't enough seats for everyone (maybe a good thing since it forced people to network?).

Networking at the event was enjoyable enough. I was fortunate to meet a data scientist at Trulia and a data engineer at Lyft who were both excited for me and my efforts with Springboard. I was able the gather that much of a proficient data scientist's work is with improving models and "feature engineering". I've made a note to study more into this!

The event featured two speakers: Maxime Beauchemin, creator of Apache Airflow, and Gwen Shapira, author of Kafka: The Definitive Guide

### Maxime Beauchemin, creator of Apache Airflow

Apache Airflow is an open source solution for managing data science workflows. It seems that the effort to manage dependencies between growing teams of data scientists and data sources is a problem that grows along with a company. Max created Airflow while at AirBnB to help with these issues and the platform is now widely (probably) used in the industry (most of the audience, though this is a sampling error).  A data engineer is someone who builds data models and pipelines. Getting the data from app events and databases into the hands of the data science team is a major task. Airflow handles the management of processes from input, processing, and output. Apparently, it's also useful for seeing and measuring effects of changes made over time with some decent reporting tools. It's entirely written in Python. I found it funny when Max proclaimed how easy it was to integrate it by saying that it could be done with "just a few dozen lines of code". I think that shows just how nascent this market is. Airflow seems like a great way to handle batch operations and scheduled chron jobs. But when it comes to event streaming, everything is different. Enter: Gwen Shapira.

### Gwen Shapira, author of Kafka: The Definitive Guide

Gwen talked about the evolution of data science over the last 40 years from a focus on data warehouses, to more recently data lakes, and most recently (last 2 years or so) Data Streams. Much of this content went over my head as with the previous talk, but I tried to absorb as much as I could. Hadoop enables data lakes and shifts much of the work from the database admin to the data scientist. With much more analysis possible, this is a common solution. The response to data lakes was to increase accessibility and speed even further by considering every piece of data an event and processing them all together. For example, instead of a database record, an event would be the entry or deletion of a database record. Another big takeaway from the talk was the consolidation of job titles from all different types of data related roles all toward the singular "software engineer". The second half of her talk was entirely technical, describing best practices for Kafka and event streaming. For now, I'll simply remember these names and look them up when I need them.
