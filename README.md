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

-For the first start of data analysis we begin by checking the number of rows and columns present before cleaning the data and after cleaning the data as seen below
![image](https://github.com/user-attachments/assets/08954ce0-7a68-47b7-839d-4952afca50a6)

-After checking the number of rows and columns we check the datatypes present in both versions and we see to it that the datatypes are now in the correct types as some int values may be counted as string values and we can see that in the clean dataset we changed the columns to their respective datatypes and we can see that the NaN values can be listed below for both datasets
![image](https://github.com/user-attachments/assets/28e044d8-6a1b-4087-be43-a1a68b6fc4a5)

### Basic Descriptive Statistics

-From this point onwards we will only be using the cleaned dataset. The mean, median and standard deviation for the dataset is actually easily retrieved with the function being fully implemented into pandas
![image](https://github.com/user-attachments/assets/6ca4e857-49ce-4a98-8e9b-61f90e5aa227)

-The trends and outliers in the dataset is easier to be spotted with using box graphs because their outliers and whiskers can show upper quartiles, lower quartiles and outliers that are not within the box
![image](https://github.com/user-attachments/assets/05553973-d99c-457f-98a1-47717091993d)
![image](https://github.com/user-attachments/assets/bec338ce-3381-4431-8217-dde08e03fb2a)

-Most released songs and artists present in the dataset actually were made in the years near the year the data was gathered and for the artists they usually have 1 to 2 songs in the set

### Top Performers

-The top performers in the song can easily be drafted in the charts where we can also see that "Blinding Lights" by The Weeknd is the most streamed song reaching billions of streams
![image](https://github.com/user-attachments/assets/1b8c9674-3b0b-43b1-98fc-f61e51efef37)

-But despite him having the most streamed song Taylor Swift was the person with the most streamed songs present in the dataset this may be because of multiple tracks reaching higher values of streames in comparison to The Weeknd's songs
![image](https://github.com/user-attachments/assets/f0a0bcab-3455-4a9a-954c-2a845d1de21c)

### Temporal Trends

- The tracks in the list was made in the year the data was gathered seeing as huge spike in the years going into 2020s
![image](https://github.com/user-attachments/assets/d2531419-2ec6-4316-8ecb-5276b22f5cf2)

- But the months on the other hand shows that most tracks are made in the months of January with May being the second month with the most generated tracks
![image](https://github.com/user-attachments/assets/4e28b76a-2820-468e-9e3a-b9b5de7ed621)

### Genre and Music Characteristics

- The number of streams in the heat map as they are closer to the value of 1
![image](https://github.com/user-attachments/assets/0e196b7e-1878-41c4-8cfd-6b9d72981076)
![image](https://github.com/user-attachments/assets/39eef507-4674-4da1-bea1-bf06dd1a12fc)

- The correlation with energy and danceability has a positive corelation as well as valence and acousticness

### Platform Popularity

- The popularity of streaming platforms is subjective but we can see that most people use Spotify instead of Deezer and Apple, we can also see that the most streamed song follows the same pattern.
![image](https://github.com/user-attachments/assets/be4ba104-0b30-4057-a6bb-89d653da2132)
![image](https://github.com/user-attachments/assets/6c0fd403-1dec-4cc6-972f-8db2928458b7)

### Advanced Analysis

- Number of tracks released with their respective modes and keys we can see that the key C# is the most popular while the mode major is the most famous
![image](https://github.com/user-attachments/assets/a9bcc54a-97ac-473b-9da0-4b042b3f2a61)
![image](https://github.com/user-attachments/assets/3c0d5a5e-f39e-4ce9-9ee5-daffd01a4572)

- The top 5 artists on the other hand can be seen below the artists present in most playlists don't correlate with the top 5 artists in the charts across platforms
![image](https://github.com/user-attachments/assets/6255cbf5-9717-414b-9101-95539e78631e)
![image](https://github.com/user-attachments/assets/30746388-91b8-4da6-807a-029ab44a41de)






