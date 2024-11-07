# Spotify-Dataset
 
# Insights
*November 1 2024*

-Started assesing the dataset

-While I was analyzing the dataset, I have noticed that there are particular values in some columns that have NaN values (missing values) and decided that instead of deleting their data I set that NaN values to 0

-I have noticed aswell that the data struggles with recognizing songs from other languages for example The song by Ovy On The Drums and Quevedo, I'm assuming that the song is Sin Señal but in the .csv file it is only displayed as Sin SeÃ¯Â¿Â½Ã¯ and many more songs, to fix this problem I have searched for the appropriate song titles and fixed the spotify-2023.csv file

-In the column of streams there is one value in particular that I deducted was an error in the data gathering which is for the streams for the song "Love Grows (Where My Rosemary Goes)" by Edison Lighthouse where the value of streams is just a line with its characteristics instead of the usual integer value and so I changed the value to 0 instead of removing the song and the song's data entirely

# Changelog
