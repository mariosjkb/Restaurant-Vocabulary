# Dictionary with positive and negative phrases about restaurants
Jupyter notebook that uses the reviews of some restaurants and extracts positive and negative words/phrases that describe the restaurants.

## Motivation
The algorythm was developed for the purposes of an undergraduate class in in Computer Science and Engineering Department of University of Ioannina and it aims to familiarize the student with data extraction methods.

## Requirements
+ [Python](https://www.python.org/)
+ [Jupyter](https://jupyter.org/)
+ [NumPy](https://numpy.org/)
+ [Scikit](https://scikit-learn.org/stable/)
+ [Gensim](https://radimrehurek.com/gensim/)
+ [Yelp](https://www.yelp.com/dataset)

## Description
The algorythm gets the text reviews for a sample of restaurants found in the Yelp dataset. Then keep only the restaurants with average review score >=4.5 and <=2 in order to polarize our data and guarantee that the reviews left in our dataset are strongly positive and negative.
We vectorize the reviews using Tf-Idf vectorizer and run k-means with n=2. Then we check the centroids of the 2 clusters and the words that are not positive or negative adjectives become stop-words for the Tf-Idf vectorizer. We repeating this process until the 10 most important words for clustering in both centroids contain plenty positive/negative adjectives.
Then we use a Skipgram embedding for the top words we found previously in order to find phrases with these words and then return the result.

## Contributor
+ [Marios Iakovidis](https://github.com/mariosjkb)