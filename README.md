# Spotify-Dataset
 
## Insights while cleaning the Dataset

-While I was analyzing the dataset, I have noticed that there are particular values in some columns that have NaN values (missing values) and decided that instead of deleting their data I set that NaN values

-I have noticed aswell that the data struggles with recognizing songs from other languages for example The song by Ovy On The Drums and Quevedo, I'm assuming that the song is Sin Señal but in the .csv file it is only displayed as Sin SeÃ¯Â¿Â½Ã¯ and many more songs, this may be due to encoding artifacts when the data was being retrieved

-In the column of streams there is one value in particular that I deducted was an error in the data gathering which is for the streams for the song "Love Grows (Where My Rosemary Goes)" by Edison Lighthouse where the value of streams is just a string with its characteristics instead of the usual integer value and so I deleted the song entirely from the dataframe as we cannot relate its characteristics without having a definite number of streams for the song
![1](https://github.com/user-attachments/assets/3589ad54-d3d1-4ff6-aa56-9b836fb1e4ff)

-After dropping that specific row we replace NaN values with 0 and drop the row in the position of 574, we check for the datatypes for each column present in the dataset 
![image](https://github.com/user-attachments/assets/6a9b337c-aeea-465b-a473-495563786f3a)

-We can see that on the column for 'in_deezer_playlists', 'in_shazam_charts' and 'streams' is actually an object datatype rather than a integer value. We remove the commas present in 'in_deezer_playlists' and 'in_shazam_charts' with the function .str.replace in order to change it to an integer datatype
![image](https://github.com/user-attachments/assets/ca0b1b35-818d-4b0e-b22a-9f4e5da71605)

-Now we can convert them to an integer value and sort the values based on how popular they are in the streams column
![image](https://github.com/user-attachments/assets/b6324b73-750b-46bd-9f99-66d32ed2b120)

-After analyzing the dataset again, I saw that there are songs that have multiple entries in the dataset and they have their own data 
![image](https://github.com/user-attachments/assets/4ecf86f5-f383-4038-b78a-a7c2aecc0f24)

-I decided to drop the row with the fewer number of streams as to keep only one entry of the songs in the dataset
![image](https://github.com/user-attachments/assets/8198cec2-9655-4bca-a97a-cedcc8ad5783)

## Data Analysis

### Overview of Dataset
