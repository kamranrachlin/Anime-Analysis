# Cleaning

The initial cleaning was overall straighforward and can be followed rather linearly.
I first removed a number of shows from my data that I found to have obvious erronious scores.
Appart from shows rated 0, on the other end a pornographic show called 'Doki Doki Little Ooyasan' had an average score far higher than anything else.
A quick search shows that this is clearly an incorrect rating for the show.

I also removed users with too few scores (less than 5), or who only rated shows 0, or 10.
Finally, I removed ratings for incomplete shows that were 0.
The reasoning for this is that in these cases, null values had been filled with 0.
As 0s constituded a very low fraction of legitimate, I felt it made more sense to drop these.

This reduced the data to around 20,000,000 recordings, 7000 shows, and 100,000 users.
