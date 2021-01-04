# The Elements of a Good Anime
## Genre
The first thing I inspected was what genres were best received by the anime community.
<img src="Visual Resources/Top Genres.png" style="width: 800px;">
*Josei: Anime aimed at women over the age of 18

**Shounen: Anime aimed at boys from 12-28

As we can see, the most well received genres tend to be mature, non-sexualised, content, perhaps with darker elements, in genres such as thriller, psychological and mystery, or more political elements, in genres such as military, samurai and police.

This can be compared to the worse received genres:
<img src="Visual Resources/Bottom Genres.png" style="width: 800px;">
*In this context, Yuri, Yaoi, and Hentai all refer to pornographic content, with Yuri and Yaoi refering to homosexual content between women and men respectively.

** Ecchi: heavily sexualised (non-pornographic) anime

It is clear that, apart from content aimed at young children, sexualised and pornographic content do particularly poorly.
This is likely in part due to the tendency from all of these genres to have a lower budget, as they are often produced to a lower standard than most regular anime.
In fact it would not be too far to say all genres in this bottom list are generally associated with lower production value.
Horror and Dementia, for example, are, in theory, not miles apart from thriller, psychological and mystery, however they do tend to have lower production standards.
At this point I hypothesised that even accounting for the production factors, we would still see the same genres having similar, significant, negative effects.
I was, however, shown wrong.

## Modelling
The modelling was principally very simple.
I reduced the shows genre, production company, original source material (book, comic, etc.), animation studio, and year produced into a series of binary yes-no's.
Each show therefore had a 1 under each genre it was, studio that created it, etc., and a 0 under each variable it wasn't.
I then removed factors in which there were less than 50 shows, to avoid an overfitting scenario.
This left us with 163 factors.

I then split my data into a training and test set at a ratio of 2:8, and standardised it to allow me to apply a wide variety of models.
The accuracy of the best performing model of each model type is shown in the graph below:
<img src="Visual Resources/Rating Predictor Results.png" style="width: 800px;">

I noted that the Linear Regression produced very similar results to the best alternatives, so I reran the model on un-standardised data.
This allows a more intelligible understanding of the impact of different variables.
The variables in this model (as all data was binarised) are simply an addition of the coefficients of all the factors it has.
The most influential variables are as shown here:
<img src="Visual Resources/Rating Predictor Factors.png" style="width: 800px;">

The model thus predicts, all else being equal, that a show animated by studio DLE will be rated almost 1 whole point worse than if it had not been.

One highly notable thing, is that among the most important factors, only one genre is present, hentai, and it is considered a positive.
This is highly surprising, and is likely due to most hentai being made by producers and studios who only make hentai work.
If those studios and producers have strong negative coefficients, this may offset the positive hentai coefficient.
It is clear regardless, however, that genres do not seem to have as significant an impact on the rating of anime as I had previously assumed.
Factors such as animation studio, of which there are 7 in the top 20 most influential variables (DLE, Studio Ghibli, Kyoto Animation, Sunrise, ufotable, Nippon Animation, Shaft) seem to have much more of an impact.

It should be said that the accuracy scores of the model were by no mean perfect.
More of the variation is accounted for outside these factors than within them.
The residuals, the difference between the predicted and actual scores, did not raise any alarm bells, however they were larger than I would have liked.
<img src="Visual Resources/Residuals.png" style="width: 800px;">
I would like to gather more data to attempt to make a better model in the future.
I imagine factors such as the director and the voice actors would be useful in predicting a high scoring anime.
