# Take Home Challenge - Ultimate Technologies Inc.

[Python Notebook](Ultimate%20Technologies.ipynb)

### Assignment

A sample take-home interview assessment proposing an Uber/Lyft imitation with a reasonable business need that can be solved using data science and statistics.

### Data

9,788 user login records with date-times. 50,000 user records with properties regarding their use of the Ultimate application and activity levels.

### Approach

For this problem, a less visual exploration is utilized to avoid the anguish of reading box plots with massive outliers. These outliers could be removed, but ultimately the data is compared ordinally and the visualization is not as relevant. The Python datetime library is used to resample the data as necessary. 

User data is cleaned and relabeled to suit vectorization in machine learning models. Scikit-learn is the primary python library used to model and evaluate predictions on user retention.

### Reflection

As a take-home assessment, this could be a valuable way to assess a potential employees suitability for a job. It includes a wide range of questions and hits most major themes. I completed the assignment to a level of satisfaction, but for a real job assignment, I would certainly focus more on the business stakeholders ingestion of the report. That means more visualizations and less jumps in logic so that everything can be followed intuitively without a major understanding of how the models are working. On the job, it's important to share findings early, and to report what it would take to further improve them. There is always a balance between model efficacy and timeliness of the report. It would be a shame to improve the model by 10% and deliver 10 days late!
