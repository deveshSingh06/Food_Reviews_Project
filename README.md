# Amazon Fine Food Reviews Analysis


Data source is available [here](https://www.kaggle.com/snap/amazon-fine-food-reviews). 

The Amazon Fine Food Reviews dataset consists of reviews of fine foods from Amazon.

Number of reviews: 568,454<br>
Number of users: 256,059<br>
Number of products: 74,258<br>
Timespan: Oct 1999 - Oct 2012<br>
Number of Attributes/Columns in data: 10 

Attribute Information:

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

<img src="http://nycdatascience.com/blog/wp-content/uploads/2016/04/AmazonReview.png" width="600">


### Objective:
Given a review, determine whether the review is positive (Rating of 4 or 5) or negative (rating of 1 or 2).


**Ques.** How to determine if a review is positive or negative?

**Ans.** 
1. If we simply use the score/rating column, the problem becomes very trivial and a simple if-else condition is enough to find out the polarity of a given review.<br>
2. To turn this problem into a machine learning problem, we remove the score column and use the reviews column and convert reviews to d-dimensional vectors.<br>
3. We apply the concepts of linear algebra along with some machine learning algorithms on these vectors and find out the polarity of each review.<br>
4. A rating of 4 or 5 could be considered a positive. A rating of 1 or 2 could be considered negative. A review with rating 3 is considered neutral and ignored. This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.

# Featurization techniques used to convert reviews to vectors:
- Bag of Words(BoW)
- TF(Term Frequency)
- IDF(Inverse Document Frequency)
- Word to Vector(Word2Vec)
- Average Word to Vector(Avg Word2Vec)
- TF-IDF Weighted Word2Vec<br>
To learn about the featurization techniques discussed above, check out my repository named [Natural Language Processing](https://github.com/deveshSingh06/Natural-Language-Processing).

# Technique used for dimensionality reduction: T-SNE
- t-SNE stands for T-distributed Stochastic Neighbour Embedding.
- It is a machine learning algorithm for visualization developed by Laurens van der Maaten and Geoffrey Hinton.
- t-SNE is neighbuorhood preserving embedding.
- In t-SNE, the distances between a given point, in d-dimensions, and the points in its neighbourhood are preserved.
- When a given point is embedded to a point in low-dimensions(say 2-d), the actual distances between the given point and the points in its neighbourhood are similar(might be same or slightly different) to the distances that were in d-dimensions(d >>> 2).<br>
To learn about more about t-SNE, check out my repository named [t-SNE on MNIST Dataset](https://github.com/deveshSingh06/t-SNE-on-MNIST-Dataset).

