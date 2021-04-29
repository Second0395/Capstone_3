# title

We all know that there are differences between 1 star ratings and 5 star ratings. No matter what website you go on, there is a general understanding that 5 star means the product or service met or even exceeded your expectations, and a 1 star rating means that it did not. 

But what is the case for 2,3, and 4 star ratings? Depending on the person, there's a wide range of things that people would consider a 2 star rating, for example. For a lot that could mean "slightly better than 1 star" or depending on the person's mood that day, maybe a slight defect in the product could change their rating from 5 stars to 2 stars. In general, it's hard to draw a line between the middle ratings, as the way people approach rating them varies a lot as well. That being said, is there perhaps a pattern in the language that people use depending on the rating they give?

That is what this project focuses on. Using both a classification and a regression model, it will explore some insights we can gather from constructing these models.

# Data

The movies and TV reviews dataset has around 1.7 million reviews from Amazon, whose character length is above 100. For the purposes of this project, I chose to only consider reviews in the 500-3000 character range to get reviews with a significant body but a reasonable size.

As an enjoyer of movies, I thought this dataset would be really useful for the project. Movies and TV are something that a lot of people feel strongly about, so there would be a lot of emotions present in their reviews. So, the models would be able to use NLP to pick up on them

# Modeling

For the purposes of modeling, I created a balanced dataset, composed of 40,000 reviews from each star rating class, so 200,000 for the whole dataset. This balanced dataset would allow me to use 

This project aims to use both classification and regression to pull insights about the original dataset, first let's start with classification.

## Classification

Trying out a Random Forest, Logistic Classifier, Multinomial Naive Bayes' model and a KNN Classifier, the Logistic Classifier performed the best with an accuracy of 53%. This actually performs well, considering that random guessing in a 5-class model would give 20% accuracy.

ROC CURVE

This ROC curve does a good job of showing how each category performs in the model. They are evaluated by AUC (Area under curve), so the ones that perform the best are the ones with the most area under the curve. If we go from best-performing to worst-performing, then the best class is 5 stars (purple) followed closely by 1 star (blue). These two are grouped together, which is intuitive. 1 and 5 star ratings are the most polarized, representing when somoene is either very pleased or very displeased with a product. So the model is able to detect these the easiest out of all the classes. There is also the fact that they are the boundary classes, and in a sense will "absorb" all the sentiment that extends past them as well, like if someone was very, VERY displeased with a product, it would still appear in the 1 star class.

If we look a little further down, we can see that 2 stars and 4 stars are also grouped together. Again, this makes sense--these classes are somewhat less defined than the 1 and 5 star classes, but they still have some signal in them that indicates whether they're positive or negative. There is a general understanding that 4 and 2 star rating are less potent versions of 5 and 1 star ratings, so again, this is intuitive.

And at the lowest value, we have the 3 star class represented by the green curve. The 3 star rating posesses qualities of both the 2 and 4 star rating, which are already loosely defined for a lot of people. But this line still performs significantly better than the mean regressor, notated in the dotted black line, so the model does successfully pick up on words that are unique to this class. 

All in all, this ROC curve does a great job at giving an intuitive understanding of how the model is performing on this dataset with regard to the classes, and it reflects our real world understanding of the classses as well.

FEATURE IMPORTANCES

For the logistic model, I also pulled out the feature importances for each class. These gave some very intuitive results:

picture

Notice the absense of any words that relate directly to the topic of Movies and TV. These coefficients pulled from the Logistic Classifier give us a very intuitive and generic list of words pertaining to all of the star classes. However
