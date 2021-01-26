Topic Analysis of Review Data


Dataset here: https://drive.google.com/file/d/1Sks0bCfDSDlbHT0mQj5O7P5e46DkpEEX/view?usp=sharing


DESCRIPTION

Using NLP and machine learning, make a model to predict the rating in a review based on the content of the text review. This will help identify cases with a mismatch.

Problem Statement:  

Zomato is India’s largest platform for discovering restaurants and ordering food. It operates in India as well as a few cities internationally. Bangalore is one of the biggest customers and restaurant bases for Zomato with 4 to 5 million users using the platform each month.

Users on the platform can also post reviews of restaurants and provide a rating accompanying the review. The content in the reviews should ideally reflect the rating provided by the customer. In many cases, there is a mismatch, owing to multiple reasons, where the rating does not match the customer review. The reviews and rating match is very important as it builds customer trust on the platform and helps the user get an accurate picture of the restaurant. 

You, as a data scientist, need to enable the identification and cleanup of such cases to ensure the ratings reflect the reviews and that the reviews seem trustworthy to the customer. You will need to use NLP techniques in conjunction with machine learning models to predict the rating from the review text. 

Domain: Hospitality and internet

Analysis to be done: Perform specific data cleanup, build a rating prediction model using the Random Forest technique and NLP. 

Content: 

rating: the rating given by the customer

review_text: the text in the review

Steps to perform:

Perform clean up on the data; tweak the stop words (negative terms are important). Follow up with a Random Forest Regressor to predict the star rating given by the customers.

Tasks: 

Load the data using read_csv function from pandas package

Null values in the review text? 

Remove the records where the review text is null

Perform cleanup on the data 

Normalize the casing

Remove extra line breaks from the text

Remove stop words

Note: Terms like ‘no’, ‘not’, ‘don’, ‘won’ are important, don’t remove

Remove punctuation

Separation into train and test sets

Use train-test method to divide your data into 2 sets: train and test

Use a 70-30 split

Use TF-IDF values for the terms as features to get into a vector space model

Import TF-IDF vectorizer from sklearn

Instantiate with a maximum of 5000 terms in your vocabulary

Fit and apply on the train set

Apply on the test set

Model building: Random Forest Regressor

Instantiate RandomForestRegressor from sklearn (set random seed)

Fit on the train data

Make predictions for the train set

Model evaluation

Report the root mean square error

Hyperparameter tuning

Import GridSearch

Provide the parameter grid to choose:

max_features – ‘auto’, ‘sqrt’, ‘log2’

max_depth – 10, 15, 20, 25

Find the parameters with the best mean square error in cross-validation

Choose the appropriate scoring as the metric for scoring

Choose stratified 5 fold cross-validation scheme

Fit on the train set

What are the best parameters?

Predict and evaluate using the best estimator

Use the best estimator from the grid search to make predictions on the test set

What is the root mean squared error on the test set?

Can you identify mismatch cases? 

Make a rule based on the predicted value and the actual value that identifies mismatch cases (e.g. difference in actual and predicted being more than a cutoff)

How many such cases do you see?

Are all these mismatch cases genuine?
