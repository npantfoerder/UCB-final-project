# UCB Final Project
## Link to Google Slides Presentation
Here is the link to the presentation: https://docs.google.com/presentation/d/1nddvQA9pJ1J52MaG6unWViKxsb_lgtQ5arq4Pr88yl0/edit?usp=sharing 

## Project Overview
My group decided on the topic of predicting musical genres because of our common interest in music. Being in charge of the machine learning portion, I chose to create a model that would predict a song's genre based on lyrics and audio features. The steps of my work are outlined below:
- Data Preprocessing
  - Using the Spotify and Genius APIs, my first task was to create a CSV file filled with song data
  - The next step was to filter the songs based on language and clean all of the song lyrics
  - Then I created a natural language processing pipeline that tokenized the lyrics and removed stop words
  - Lastly I created a DataFrame containing the term frequenices of each song
- Data Analysis
  - Looking at top words and word count distributions by genre and popularity I created DataFrames for the following:
    - Top ten words for each genre
    - Top ten co-occurring words for each genre
    - Word count distributions for each genre
    - Word count distributions for each quartile of songs based on popularity
- Feature Selection
  - I defined my features set (X) as the numerical audio features and term frequencies columns
  - The target set (y) was the genres of the songs
  - By removing songs where the artist's genres did not match the song's category, I improved the model's accuracy
- Random Forest Model
  - I used a random forest model because it allows for feature ranking, runs efficiently on large datasets, and is robust to outliers
  - First, I split the data into training and testing sets and scaled the features set
  - I trained the model using the scaled X training set and the y training set with 500 estimators
- Results
  - Using the entire dataset, the model's accuracy started at 51.6%
  - Filtering the data to only include songs with matching categories and genres, the accuracy increased to 72.1%
  - The model's weighted average precision score was 0.73
  - The model's weighted average recall score was 0.72d
