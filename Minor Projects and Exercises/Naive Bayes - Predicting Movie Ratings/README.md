# Naive Bayes: Predicting Movie Ratings

[Python Notebook](Mini_Project_Naive_Bayes.ipynb)

### Assignment

This exercise demonstrates the basics of text analysis using Naive Bayes, hyper parameter tuning, and model selection.

### Data

15,561 movie reviews aggregated on Rotten Tomatoes including fresh/rotten target class and a few other columns in csv format

### Approach

Following a standard histogram exploration of the data, a corpus of reviews is created by vectorizing the movie review text bodies. A Multinomial classifier from scikit-learn is used to model split training data. Hyperparameters of alpha and minimum document frequency are selected through visual analysis of a CDF and by scoring model performance with different values. A Log Likelihood function is created as another optimization method, and thereafter a few different models are tested, but not optimized: TF-IDF, N-Grams, and Random Forest.

### Reflection

As far as I know, Rotten tomatoes relies primarily on scaling numerical scores from other publications to label referenced reviews as rotten or fresh, but a day's work of machine learning can perform surprisingly well. A trigram model was 76.8% accurate on unseen test data. That's pretty cool! Trying out the default settings for the other models included was fun too, but not as engaging, as Scikit-Learn handles everything. 