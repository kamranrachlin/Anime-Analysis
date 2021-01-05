# Analysing the Community
## Creating Data
Whilst I had a lot of data about individual ratings, the data did not contain much in the way of information about the over 100,000 users, so I set about to create some using what was available.
My plan was overall quite simple: create a baseline prediction for each user, using the average score an anime receives, and the relative average score the user gives, we can create a primitive mean as to what the user might have rated that show.
This should account for the overall quality of the show, and the users tendencies towards treating ratings.
The difference that is left should be how the user felt about that show in particular, compared to other shows with a similar rating, and thus should form some kind of representation of personal taste.  

For each user,for each category established in the previous section, plus an added category of whether or not a show was in the top 100 most popular shows on the website, I worked out their average rating difference vs baseline for shows in that category.
This creates a list of biases. For example, if a person regularly rated shows in the by Kyoto Animation higher than expected, we could say that they show a preference or bias towards shows by Kyoto Animation.
A small section of the Dataframe:
<img src="Visual Resources/Bias Frame Example.png" style="width: 800px;">

For example, we would expect the user with the URL tag of karthiga would respond more positively than average to an action show about demons, and more negatively to a drama.

## Utilising the Data

One of my initial plans was to attempt to form clusters of users; to group users with similar biases to see if it's possible to gain insights into trends that users share.
This unfortunately turned out to be very difficult, time consuming, and ultimately unsuccessful.
Silhouette score is a metric for measuring the compactness of groups.
It effectively measures whether points are closer to members of their own cluster, or members of others, and it ranges from -1 to 1.
Despite trying to group users into a wide range of number of clusters, none produce a particularly impressive silhouette score:
<img src="Visual Resources/Clustering Silhouettes.png" style="width: 800px;">

With little success in unsupervised learning, I looked to supervised learning to extract some information from the data.
As part of their profile, every user in the data had idenified their gender as either male, female, or non-binary. I decided to see if we could use our data to predict the gender of a user based on their biases.

As there was a serious class imbalance (very few users identified as non-binary), I decided to attempt to predict whether or not a user identified as male.
Male identifying users made up around 2/3rds of the user base, which set a baseline for our models (as a model is clearly ineffective at predictions if it would be more successful to simply guess every user is male)
With a similar process to the previous section, I tested a wide range of models, this time splitting my testing and training sets more evenly, at a ratio of 1:2.
The best model of each type performed as follows:
<img src="Visual Resources/Gender Predictor Results.png" style="width: 800px;">

As we can see, logistic regression fared poorly, with the neural network and decision tree performing much better.
Within the decision tree, we can look at the feature importance:
<img src="Visual Resources/Gender Predictor Factors.png" style="width: 800px;">

These factors were the most significant when splitting up groups to decide if they were to be predicted male or not.
Shounen Ai refers to content focusing on a homosexual relationship between men, and is often heavily marketed towards women, whilst Shoujo referes to content marketed towards teenage girls.
This may suggest that the gender divide on female focused media is stronger than the gender divide on male focused media, however without further analysis, that cannot be confirmed.


