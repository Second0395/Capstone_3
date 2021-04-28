# title

We all know that there are differences between 1 star ratings and 5 star ratings. No matter what website you go on, there is a general understanding that 5 star means the product or service met or even exceeded your expectations, and a 1 star rating means that it did not. 

But what is the case for 2,3, and 4 star ratings? Depending on the person, there's a wide range of things that people would consider a 2 star rating, per say. For a lot that could mean "slightly better than 1 star" or depending on the person's mood that day, maybe a slight defect in the product could change their rating from 5 stars to 2 stars. In general, it's hard to draw a line between the middle ratings, as the way people approach rating them varies a lot as well. That being said, is there perhaps a pattern in the language that people use depending on the rating they give?

That is what this project focuses on. Using both a classification and a regression model, it will explore some insights we can gather from constructing these models.

# Data

The movies and TV reviews dataset has around 1.7 million reviews from Amazon, whose character length is above 100. For the purposes of this project, I chose to only consider reviews in the 500-3000 character range to get reviews with a significant body but a reasonable size.

As an enjoyer of movies, I thought this dataset would be really useful for the project. Movies and TV are something that a lot of people feel strongly about, so there would be a lot of emotions present in their reviews. So, the models would be able to use NLP to pick up on them

# Modeling

For the purposes of modeling, I created a balanced dataset, composed of 40,000 reviews from each star rating class, so 200,000 for the whole dataset. This balanced dataset would allow me to use 

This project aims to use both classification and regression to pull insights about the original dataset, first let's start with classification.

## Classification

Trying out a Random Forest, Logistic Classifier, Multinomial Naive Bayes' model and a KNN Classifier, the Logistic Classifier performed the best with an accuracy of 53%. This actually performs well