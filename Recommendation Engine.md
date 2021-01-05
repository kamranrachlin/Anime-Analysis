# Creating a Recommendation Engine
For the final part of this investigation, I wanted to look into the possibilities of creating a recommendation engine using the data available. This proved extremely hardware intensive, and I cannot say I am entirely happy with where I left this off. I intend to return to this at some point in the future and use AWS or an equivalent service to take a deeper look at this.

I split the 20,000,000 data points into a train and test set of 9:1. The median number of ratings per user was well over 100, and median ratings per show was not far from 1000, so I felt a smaller test set could be justified, to give the models the best chance of performing.

I then ran various models on the training data, and compared their RMSE to each other on the train and test data
## The Results
<img src="Visual Resources/RMSE Reccomendation Engines.png" style="width: 800px;">
<img src="Visual Resources/Baseline Rec Res.png" style="width: 800px;">
<img src="Visual Resources/SVD Res Red.png" style="width: 800px;">



As we can see, our most successful model, SVD, is definitely better than baseline, however it still has a RMSE of over 1.7 on the test set, which is higher than I would consider practical to build a useful recommendation engine. It is still significantly better than the 2.7 that would be got from simply predicting the average score voted, and it is somewhat better than the 2 from guessing the baseline, which gives hope that given more computing time, we could find a model which recommends anime within a reasonable tolerance. In the future, I hope to improve upon these results.


