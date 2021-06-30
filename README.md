# Spotify Song Recommender
Building a song recommender based off the spotify song features of my listening history.

According to Spotify's Wrapped for 2020, I was in the top 0.5 % of J. Cole's listeners. #realcoleworld. However, spotify has a plethora of songs by millions of artists available and I feel like I am missing out and should explore new songs. So I decided to create a **song recommender to help me classify whether I would like the new song or not**.

## Data
- StreamingHistory.json - personal listening history provided by spotify 
- [tracks.csv](https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks?select=tracks.csv) - dataset containing audio features of around 600k songs from kaggle

### Spotipy
[Spotipy](https://spotipy.readthedocs.io) - a lightweight python library for the Spotify Web API - was used to obtain audio features of missing songs. This was done in the [missing-features](missing-features.ipynb) notebook.  

## Spotify Song Features
Spotify gives all songs several audio features such as: *danceability, energy, loudness, speechiness, acousticness, instrumentalness, liveness, valence and tempo.*

- A great article describing spotify audio features [here](https://medium.com/@boplantinga/what-do-spotifys-audio-features-tell-us-about-this-year-s-eurovision-song-contest-66ad188e112a#379f) 
- Spotify API reference [here](https://developer.spotify.com/documentation/web-api/reference/#endpoint-get-audio-features)

I'll be using these audio features to find the highest correlation with my **favourite** songs.  

## Dependent variable
The variable 'favourite' will be the prediction variable. I will assign the songs that have **more than or equal to 9 listens** with 1 (favourite) and less than 9 listens as 0 (not favourite). 
When I plotted the number of times I've listen to a specific song on a histogram, a sharp drop off at 9 listens clearly divides the songs that I deliberately listen to and the ones that I clicked on by accident or when I was trying to find new music.

<img src="images/why9.PNG" height="300">

## Objective
To create a song recommender using my Spotify listening history, by comapring Decision Tree and Random Forest classifier models and testing the models' accuracy using F1 score.

## Process
1. Data Cleaning / Exploration
2. Feature Selection and Oversampling to balance classes
3. Model Selection with Cross-validation and Hyperparameter Optimization
4. Predictionof Songs


## Conclusion

## Credits
[isacmlee's song recommender](https://github.com/isacmlee/song-recommender.git)
