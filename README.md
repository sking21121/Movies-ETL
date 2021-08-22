## MOVIES-ETL
Amazing Prime wants to create an automated pipeline that takes in new data, performs the appropriate transformations,
and loads the data into existing tables. My purpose is to create one function that takes in the three files—Wikipedia
data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database. 

## Overview of Project

Deliverable 1: Write an ETL Function to Read Three Data Files
Deliverable 2: Extract and Transform the Wikipedia Data
Deliverable 3: Extract and Transform the Kaggle data
Deliverable 4: Create the Movie Database

## Analysis 
In Deliverable 1 an ETL function is written to read in the three data files. The function converts the Wikipedia JSON
file to a Pandas DataFrame. The function converts the Kaggle metadata file to a Pandas DataFrame.  And 
the function converts the MovieLens ratings data file to a Pandas DataFrame.

In Deliverable 2 I need extract and transform the Wikipedia data so you can merge it with the Kaggle metadata. To do this
I first need to filter out tv show and create a wiki_movies_df. Write a try-except block that will catch errors while
extracting the IMDb IDs with a regular expression string and dropping any imdb_id duplicates. Clean the box office,
budget, release date, and running time columns. 

In Deliverable 3 I extracted and transformed the Kaggle metadata. The wiki and kaggle dataframes are merged. Then
unnecessary columns are dropped, a function is used to fill in the missing Kaggle data, movies_df DataFrame is filtered
to keep specific columns, and movies_df DataFrame columns are renamed. The the Movies Lens ratings data is cleaned. The
movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame. The empty
values in the movies_with_ratings_df DataFrame are filled with “0”. 

In Deliverable 4 I added the movies_df DataFrame and MovieLens rating CSV data to a SQL database. Also added code to
display the elapsed time to add the data to the database. Then write a SQL query that retreives the number of rows for
the movies and ratings tables. 


