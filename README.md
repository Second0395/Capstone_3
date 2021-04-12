# Capstone_3 proposals

# Olympics

I think the olympics as an event is so interesting in itself. It's pretty much the biggest event in the world, so there is bound to be some interesting things regarding its logistics. 

https://olympicsapi.docs.apiary.io/#reference/olympics/athlete/retrieve-olympic-games

# Light pollution

Light pollution is an interesting phenomenon. It blocks visibility for people in highly populated areas, if there is enough light to do so. GADM has a good database where I can pull data from specific countries, so I could analyze the content of America or some of the countries in North America. I will most likely have to use Geopandas
https://gadm.org/formats.html

# Classifying star ratings

I'm thinking of pulling a bunch of reviews from Amazon's review API from many different categories, and then doing an NLP analysis of the review bodies. It's already been established that there is a difference in sentiment between 1 star ratings and 5 star ratings, but I wanted to see if a model could classify ratings of 1,2,3,4 or 5 stars based on sentiment. There wouldn't likely be a super strong connetion, but even a moderate connection would mean that there is some standard of say, a 3 star rating, across people's reviewing styles. I want to try predicting this with both a regression and a classification model
