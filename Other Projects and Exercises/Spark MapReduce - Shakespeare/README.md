# Spark MapReduce: Shakespeare

[Python Notebook](pyspark_exercise.ipynb)

### Assignment

This exercise demonstrates competent navigation of basic MapReduce functions for parallelization of data processing using the full texts of works of Shakespeare.

### Data

33,381 words of the raw text of Julius Caesar in .txt format.

### Approach

To stage the data, it is read into memory using PySpark's SparkContext.textFile() function. A stop-word dictionary of common words are read into memory line by line with Python's 'with open' function. After using the .flatMap() method on the text body to separate words, common words are removed with the .filter() method. The words are each mapped to a tuple with integer 1 as the second value so that the reduceByKey() method can be used to count the appearances of each word. Some functions are parallelized by specifying data partitions.

On a second data set with information about a population's height, weight, and gender, Pandas dataframes are integrated into the workflow, and a classification model is used to predict gender based on height and weight.

### Reflection

This was a fun little exercise. There are a couple more optional segments that I may come back to when I need more practice. The hardest part was installing all of the dependencies on my Windows 10 computer, but that's good practice as well. Using the MapReduce paradigm reminded me of some of the basic functions used in my first Computer Science course that was taught in Racket (of the Lisp family).