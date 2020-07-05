# Amazon Fine Food Reviews Analysis

The Amazon Fine Food Reviews dataset consists of reviews of fine foods from Amazon.<br>
Number of reviews: **568,454**<br>
Number of users: **256,059**<br>
Number of products: **74,258**<br>
Timespan: **Oct 1999 - Oct 2012**<br>
Number of Attributes/Columns in data: **10**<br>

The data source is available [here](https://www.kaggle.com/snap/amazon-fine-food-reviews). 

### Attribute Information:
1. Id
2. ProductId - unique identifier for the product
3. UserId - unqiue identifier for the user
4. ProfileName
5. HelpfulnessNumerator - number of users who found the review helpful
6. HelpfulnessDenominator - number of users who indicated whether they found the review helpful or not
7. Score - rating between 1 and 5
8. Time - timestamp for the review
9. Summary - brief summary of the review
10. Text - text of the review

<img src="https://nycdsa-blog-files.s3.us-east-2.amazonaws.com/2016/04/AmazonReview-300x189.png" width="600">


## What are we trying to achieve?
- Given a review, determine whether the review is positive (rating of 4 or 5) or negative (rating of 1 or 2).


## How to determine if a review is positive or negative?
 
 - We could use score/rating of reviews and build machine learning models that can classify the reviews into being positive or negative.
 - A rating of 4 or 5 can be cosnidered as a positive review.
 - A rating of 1 or 2 can be considered as negative one.
 - A review of rating 3 is considered neutral and such reviews are ignored from our analysis.
 - This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.


## Featurization techniques used to convert reviews to vectors:
- Bag of Words(BoW)
- TF(Term Frequency)
- IDF(Inverse Document Frequency)
> To learn about the featurization techniques discussed above, check out my repository named [Natural Language Processing](https://github.com/deveshSingh06/Natural-Language-Processing).


## Machine Learning Models Built:
- Random Forest Classifier
- GBDT Using XGBoost

## Model Evaluation Metrics Used:
- AUC-ROC Score
- Confusion Matrix for AUC value of a set of hyperparameters
- Precision, Recall, F1-Score

### Additional info:
- Performed Hyperparameter Tuning to find out the best hyperparameters for each model
- Plotted ROC curve for each model on test data
- Provided Feature Importance
- Used Word Clouds to display important features
