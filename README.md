# Spotify-Dataset
 
## Insights

-While I was analyzing the dataset, I have noticed that there are particular values in some columns that have NaN values (missing values) and decided that instead of deleting their data I set that NaN values

-I have noticed aswell that the data struggles with recognizing songs from other languages for example The song by Ovy On The Drums and Quevedo, I'm assuming that the song is Sin Señal but in the .csv file it is only displayed as Sin SeÃ¯Â¿Â½Ã¯ and many more songs, this may be due to encoding artifacts when the data was being retrieved

-In the column of streams there is one value in particular that I deducted was an error in the data gathering which is for the streams for the song "Love Grows (Where My Rosemary Goes)" by Edison Lighthouse where the value of streams is just a string with its characteristics instead of the usual integer value and so I deleted the song entirely from the dataframe as we cannot relate its characteristics without having a definite number of streams for the song
![alt text](https://github.com/[LechoncitoParesOverload]/[Spotify-Dataset]/blob/[branch]/1.jpg?raw=true)

## Changelog
### 11/1/2024 

### 11/6/2024 
-

