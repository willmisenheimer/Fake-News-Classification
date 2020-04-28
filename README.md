# Fake-News-Classification

PURPOSE: 
The purpose of this project is to predict whether or news document is "real" or "fake", using a bag-of-words + Naive Bayes Classification Model. The data is an extract from kaggle.com.

RESULTS:
Recorded accuracy on testing set: 94.86% (proportion of real/fake in testing set is 47.62%). This means that the model correctly classified almost 95% of the news articles that it had not yet seen. 

![Confusion Matrix of trained model scoring testing data](C:\Users\willm\Documents\GitHub\Fake News Classification\Confusion Matrix.png)

POSSIBLE USES:
A possible use of this model would be to identify and remove fake news from social media sites. It is very common for fake news to spread across social media outlets, distributing false information. This model could be implemented to identify articles that are likely to be "fake" news. These articles that are found highly probable to be consistent with known fake news articles could be reported to the governing source (Facebook or Twitter in many cases). Another possible use of this model could be to serve as the primary function of a web-based or desktop application. Users could interface with this model by scoring the pre-trained model with a news article(s) of their choosing, with a straightforward GUI. Thus, in scoring the pre-trained model, which would be re-trained in periodic updates, elements of transfer learning could also be applied. 

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


