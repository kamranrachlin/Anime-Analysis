# Cleaning

The initial cleaning was overall straightforward and can be followed rather linearly.
I first removed a number of shows from my data that I found to have obvious erroneous scores.
Apart from shows rated 0, on the other end a pornographic show called 'Doki Doki Little Ooyasan' had an average score far higher than anything else.
A quick search shows that this is clearly an incorrect rating for the show.

I also removed users with too few scores (less than 5), or who only rated shows 0, or 10.
Finally, I removed ratings for incomplete shows that were 0.
The reasoning for this is that in these cases, null values had been filled with 0.
As 0s constituted a very low fraction of legitimate, I felt it made more sense to drop these.

This reduced the data to around 20,000,000 recordings, 7000 shows, and 100,000 users.

# Data Distributions
The Data left was heavily skewed, with most users rating few shows, and most shows getting rated few times:
<img src="Visual Resources/User Input Count Large.png" style="width: 800px;">

<img src="Visual Resources/Anime rating Count Large.png" style="width: 800px;">

It was overall rather normally distributed, with a mean close to it's median both close to 7. It has a slight left tail, but this is to be expected as the mean is so large compared to the available scores. Notably, the genres of shows made a big impact on their success, a point which will be further discussed at a later point.
<img src="Visual Resources/Anime Score Distribution.png" style="width: 800px;">


