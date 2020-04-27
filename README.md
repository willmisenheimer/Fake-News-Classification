# Fake-News-Classification

PURPOSE: 
The purpose of this project is to predict whether or news document is "real" or "fake", using a bag-of-words + Naive Bayes Classification Model. The data is an extract from kaggle.com.

INPUT: 
1) News document -- the body of a news article

OUTPUT:
1) Predicted label ("real" or "fake") for each news document in the testing data set.

METHODOLOGY:
1) "Real" and "fake" news data sets are read in and concatenated into a single pandas dataframe, where the labels of "real" and "fake" are assigned.
2) Data is split into training (70%) and testing (30%) sets.
3) Training set is converted into a matrix of tokens using CountVectorizer() and fit to the Naive Bayes Classifier.
4) Testing set is transformed into a matrix of tokens using CountVectorizer().
5) The label ("real" or "fake") is predicted for the testing set using the trained Naive Bayes model.
6) Accuracy of the predictions are recorded and the confusion matrix is constructed.

LIBRARIES USED:
1) pandas
2) numpy
3) os
4) train_test_split (sklearn.model_selection) 
5) CountVectorizer (sklearn.feature_extraction.text)
6) MultinomialNB (sklearn.naive_bayes) 
7) metrics (sklearn) 

RESULTS:
Recorded accuracy on testing set: 94.86% (proportion of real/fake in testing set is 47.62%)
