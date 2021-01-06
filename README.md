# Anime-Analysis
An analysis into the anime community based on a 2018 dataset [found here](https://www.kaggle.com/azathoth42/myanimelist)
## Anime
Anime is a term used in English to refer to Japanese animation. The Japanese animation industry is rather unique, and has had a cult following in the west for well over 30 years, a following that has only grown in recent years. Anime was, and perhaps still is, best associated in the west with a series of films released by Studio Ghibli from the late 1980s to the early 2000s to much critical acclaim. These titles include Princess Mononoke (1997), My Neighbor Totoro (1988), and Oscar winning Spirited Away (2001). In recent times, however, more attention has been given to the wide birth of other anime that has been and is being produced, and it's cultural impact is evident, from a character from Darling in the Franxx (2018) on [Kim Kardashian West's Instagram Page](https://www.instagram.com/p/Bf655uvFf0T/?hl=en) to a shout out to Your Name (2016) on [Elon Musk's twitter page](https://twitter.com/elonmusk/status/1051377948916215810?lang=en). Anime has a growing global market, currently valued at upwards of £15 Billion. Netflix in particular has in recent years put a focus on attaining the rights to a number of anime, claiming to have had over 30 Netflix original anime at various stages production in 2017, obtaining the rights to cult classic Neon Genesis Evangelion (1995) in 2019, and the rights to a number of the aforementioned Studio Ghibli films in Europe in 2020. This appears to be paying off, as in October they announced that over 100 Million households worldwide had watched Anime since the previous September, a rise of 50%. It is clear then, that there is value in anime.

## The Data
[My Anime List](https://myanimelist.net) is one of the largest websites dedicated to anime and anime ratings. Users create a profile, on which they have a list with every anime that they have rated on the website. Ratings are made on a discrete scale of 1-10.
I had originally planned to produce this project by scraping original data from My Anime List, however the size of this dataset made it too attractive to pass up, even if it is slightly outdated. The Dataset contained 80 million recordings, however following the initial EDA and subsequent cleanup, this was reduced to about 20 million, which was still enough to give my hardware issues at times. I hope to advance this project further using AWS at some point in the future.

## The Approach
I approached this project from the perspective of Netflix, or one of its competitors, attempting to find valuable information from this dataset. Therefore, the primary aims of this project were to gain insights into the anime community, the factors that lead to an anime being highly rated, and to investigate the viability of building a recommendation engine for anime using the data, all three of which might be valuable insights to a company such as Netflix.

## The Results
As a summary, I found that general trends suggest that mature, non-sexualised content is better received by audiences, whilst sexualised content is generally poorly received. Further analysis shows, however, that other factors, particularly the animation studio, have a more significant impact. I found that viewers do not cluster particularly well on their preferences, however their preferences do in some way give information correlating with what their gender might be. It is suggested, based on the evidence, that female marketed content may be more divisive than male marketed content. Finally, it was shown that improvements can be made to a baseline recommendation system, however I arguably did not find a model strong enough to make a useful product.

The full process, results and analyses have been laid out in four parts. As they share common factors, it is recommended to read them in order:

[Initial Cleaning](https://github.com/kamranrachlin/Anime-Analysis/blob/master/Initial%20Cleaning.md)

[Understanding Anime](https://github.com/kamranrachlin/Anime-Analysis/blob/master/Understanding%20Anime.md)

[Understanding the Community](https://github.com/kamranrachlin/Anime-Analysis/blob/master/Understanding%20the%20Community.md)

[Recommendation Engine](https://github.com/kamranrachlin/Anime-Analysis/blob/master/Recommendation%20Engine.md)

The slides of a presentation based on an early version of this project can be found [here](https://docs.google.com/presentation/d/1-RxgS6i8_6-tbyKVt2wjApyxqs-bpdMry0NDbs_THgQ/edit?usp=sharing), though not all information on these slides can be considered the most up to date.
