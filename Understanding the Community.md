# Analysing the Community
## Creating Data
Whilst I had a lot of data about indiviual ratings, the data did not contain much in the way of information about the users, so I set about to create some using what was avaliable.
My plan was overall quite simple: create a baseline prediction for each user, using the average score an anime recieves, and the relative average score the user gives, we can create a primative mean as to what the user might have rated that show.
This should account for the overall quality of the show, and the users tendencies towards treating ratings.
The difference that is left should be how the user felt about that show in particular, compared to other shows with a similar rating, and thus should form some kind of representation of personal taste.  

For each user,for each category established in the previous section, plus an added category of whether or not a show was in the top 100 most popular shows on the website, I worked out their average rating difference vs baseline for shows in that category.
This creates a list of baises. For example, if a person regularly rated shows in the by Kyoto Animation higher than expected, we could say that they show a preference or bias towards shows by Kyoto Animation.
A small section of the Dataframe:
<img src="Visual Resources/Anime rating Count Large.png" style="width: 800px;">
