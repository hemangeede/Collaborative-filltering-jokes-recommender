# Collaborative-filltering-jokes-recommender
This a machine learning code using Collaborative filtering for jokes recommender system. It uses the dataset Jester Collaborative Filtering Dataset from Kaggle.
Use: A Joke recommender system can be a very good companion for joke lovers. The system might get the user with new and amusing jokes everyday. 
For every joke it can take user's ratings and make the recommendation more better.

Collaborative filtering technique is a method used for predicting(filtering) user interests using the users previous preferences.
This can be implemented in 2 ways:
1) Explicitly : When we take user ratings according to which the machine decides the reccomendation
2) Implicitly : When if the user watches a movie we think that he is interested in it

In this project I have used the first method, by displaying some jokes to the user from the Jester Dataset and asking for his ratings in those jokes. Then we use the collaborative filtering method to get the jokes of user interest.

The Collaborative Filtering Method is based on finding similarities in feature values and the least distance between the similarities to get the optimum result.
Here in Joke Recommender the *rating* dataframe has its users in the index column and all the ratings to the corresponding Joke Ids in its respective cells for a particular user. Then we mask the NAN values and use normalization techniques to get a resonable rating of same range. We then find the cosine similarities among the ratings of all the users and create a utility matrix.
In this way when we get a new rating of a new user to a particular joke we find the cosine similarity and then find the user and the joke which has the closest similarity to it. This helps in predicting a joke that the user may like.
