### Predicting Popularity Level of Songs

November 2022 | Elif Sena Özefe

If I was working in Spotify's marketing departmant, I would like to know that which songs deserves more marketing spending. Thus, answer of this question can be the base of budget allocation problem and can be helpful about showing the spending distributions.

#### Question
Can the popularity of the song predicted by using its features such as genre, acousticness, danceability, tempo etc.

#### Data Source
Downloaded data from https://www.kaggle.com/datasets/zaheenhamidani/ultimate-spotify-tracks-db on 2022, 26th October

#### Sample from Data
![alt text](https://github.com/elifsenaozefe/song_popularity_prediction/blob/main/sample.png?raw=true)

#### Methodology

I tried to two approaches to the question. First one is, taking it as a regression problem. This approach 35 as mean absolute error. As a second way, I treated the question as a classification problem and cut the data into three bins with ranges equal to (-1, 25), (25, 50) and (50, 100) and labels as low, mid and high respectively. Ranges of bins are not equal to not create an imbalanced data problem.

<p> After feature elimination with RFECV, final data has shaped as (164060, 43). With this data; decision tree, random forest, XGBoost, LightGBM and naive bayes have run. </p>

#### Results
For now, LightGBM with default parameters can predict songs' popularity with 79% accuracy. 79% can be taken as base line score.

<p> A feature engineering step can be added to improve the success of the model. </p>

Both EDA & predictions are on [here](https://github.com/elifsenaozefe/song_popularity_prediction/blob/main/spotify_tracks_popularity_prediction.ipynb).
