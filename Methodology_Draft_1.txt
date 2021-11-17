Methodology:

For the analysis, we primarily used the 'data.table', 'tidytext' and 'tidyverse' with some other supporting libraries, including the 'srt' library for reading the subtitle files.

Starting with our list of movies, we import our movieData.csv, which contains the year released, the runtime, and the same if it had a live adaptation. This ensures we'll have all of the initial data for each movie.

We assign each .srt file to one of our movies. From here, we re-scale the runtimes from 0-1 so we can track the runtime of each movie.  Additionally, we add a 'song' column, for movies that possess music.

For movies that contain music, we make sure that the program is aware that those portions of the movie are in song. This will help us track emotion through the songs comparatively to the rest of the dialogue.

Using our three lexicons, Afin, Bing, and NRC, we generate the sentiments for each word of each script, and save them as longer data.

From here, we generate a plot using ggridges, utilizing the NRC sentiment analysis. We can see in Figure 1 the NRC emotions over the course of each movie.

For the Afin lexicon, we run the sentiment analysis by both line and by word for all of the movies. 

We then generate a violin plot that contains the variation in positive and negative emotions of words, by the type. (Figure 2)

Finally, we gather the sentiment scores for each movie. We do this for each of the lexicons, Afin, Bing, and NRC, and we organize it by emotion.

This allows us to generate a 'radar chart' which shows each movie's relation to the relevant emotions.



