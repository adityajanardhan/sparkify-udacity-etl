# Sparkify ETL 

1. <b>Purpose of the project</b>: To solve business problems, a robust analytics system is required where we can easily query data and get insights. In this scenario, Sparkify wants to analyze songs and user activity on their music streaming app. In this project, we'll achieve this by creating a Postgres database with tables that are well designed and adjusted to optimize queries and to do analysis. The Postgres is built using an ETL pipeline using Python.

2. <b>Database schema design and ETL pipeline</b>: 


## Schema for Song Play Analysis
Using the song and log datasets, you'll need to create a star schema optimized for queries on song play analysis. This includes the following tables.

## Fact Table

  <ol><li>songplays - records in log data associated with song plays i.e. records with page NextSong</li><ol>
   <ul><li>songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent<li></ul> 
  

## Dimension Tables
    


