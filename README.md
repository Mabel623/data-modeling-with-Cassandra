# Data Modelling with Apache Cassandra

## Overview

The project is to help a music streaming app to create a NoSQL Cassandra Database. Dataset is project is a set of `csv` format contains app usage data such as user's song play history, user's log in data etc. 

The notebook in the project will walk throught EDA process, create tables and answer questions of the team. 

There are two parts in the notebook: 

- **Part I: ETL pipeline for pre-processing the files** 
- **Part II: Using Apache Cassandra to create tables as followings**:

| Tables          | Columns                                                      | Primary Keys                       |
| --------------- | ------------------------------------------------------------ | ---------------------------------- |
| *app_history*   | *artist, song_title, song_length, session_id, itemInSession* | *sessionId, itemInSession*         |
| *users_history* | *artist, song_title, user_firstname, user_lastname, userId, sessionId, itemInSession* | (userId, sessionId), itemInSession |
| *users_music*   | *artist, song_title, user_firstname, user_lastname, userId*  | *song_title, userId*               |

After tables are created, we are able to answer the following three questions:

1. Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4

2. Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182

3. Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'

