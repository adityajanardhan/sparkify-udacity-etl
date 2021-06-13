# Sparkify ETL 

1. <b>Purpose of the project</b>: To solve business problems, a robust analytics system is required where we can easily query data and get insights. In this scenario, Sparkify wants to analyze songs and user activity on their music streaming app. In this project, we'll achieve this by creating a Postgres database with tables that are well designed and adjusted to optimize queries and to do analysis. The Postgres is built using an ETL pipeline using Python.

2. <b>Database schema design and ETL pipeline</b>: We have used song and log datasets and using them we have created a star schema that are optimized for song play analysis. The schema is explained below. This type of schema is well suited to answer questions such as finding out popular artists and songs, average duration per user and other questions related to user engagement etc. 


## Schema for Song Play Analysis

## Fact Table

<ol><li>songplays - records in log data associated with song plays i.e. records with page NextSong</li></ol>
    <ul><li>songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent</li></ul> 
  

## Dimension Tables

<ol><li>users - users in the app</li>
   <ul><li>user_id, first_name, last_name, gender, level</li></ul> 
<li>songs - songs in music database</li>
   <ul><li>song_id, title, artist_id, year, duration</li></ul> 
<li>artists - artists in music database</li>
   <ul><li>artist_id, name, location, latitude, longitude</li></ul> 
<li>time - timestamps of records in songplays broken down into specific units</li>
   <ul><li>start_time, hour, day, week, month, year, weekday</li></ul> 
</ol> 
    

## Files structure

1. <b>test.ipynb</b>: displays the first few rows of each table to let you check your database.
2. <b>create_tables.py</b>: drops and creates the tables. You run this file to reset your tables before each time you run your ETL scripts.
3. <b>etl.ipynb</b>: reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables.
4. <b>etl.py</b>: reads and processes files from song_data and log_data and loads them into your tables. Its filled based on the work in the ETL notebook.
5. <b>sql_queries.py</b>: contains all the sql queries, and is imported into the last three files above.
