# Capstone_3 proposals

# Olympics

I think the olympics as an event is so interesting in itself. It's the biggest event in the world and there's a lot that happens. I want to check news coverage for news organizations in America and compare how they deliver news about other countries compared to America. I'm anticipating there will be more "patriotic" content in the American coverage. I will have to remove a lot of stop words to avoid data leakage

https://olympicsapi.docs.apiary.io/#reference/olympics/athlete/retrieve-olympic-games

# Predicting real estate value

I want to grab images of houses off of a real estate website with their respective listing prices. Then, I will try to predict the value of the house based on the image. This would be a CNN/Neural network problem and I would have to spend a while training the data on AWS. This would be an interesting problem since there is likely a connection between appearance and value, but to see a model pick up those differences would be cool.


https://www.realtor.com/realestateandhomes-search/Piscataway_NJ

# Classifying star ratings

I'm thinking of pulling a bunch of reviews from Amazon's review API from many different categories, and then doing an NLP analysis of the review bodies. It's already been established that there is a difference in sentiment between 1 star ratings and 5 star ratings, but I wanted to see if a model could classify ratings of 1,2,3,4 or 5 stars based on sentiment. There wouldn't likely be a super strong connetion, but even a moderate connection would mean that there is some standard of say, a 3 star rating, across people's reviewing styles. I want to try predicting this with both a regression and a classification model
