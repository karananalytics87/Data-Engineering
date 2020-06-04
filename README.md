
# Introduction:

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app. The aim is to create a Postgres Database Schema and ETL pipeline to optimize queries for analytics team. I have built queries in Postgres and build an ETL pipeline using Python to complete the project. I have defined fact and dimension tables for a star schema for a particular analytic focus, and writen an ETL pipeline that transfers data from files in two local directories into these tables in Postgres using Python and SQL.

# Database schema design:

Using the song and log datasets, created a star schema that optimizes the queries on song play analysis. 

This includes the following tables.

## Fact Table

songplays - records in log data associated with song plays i.e. records with page NextSong
songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

## Dimension Tables

users - users in the app
user_id, first_name, last_name, gender, level

songs - songs in music database
song_id, title, artist_id, year, duration

artists - artists in music database
artist_id, name, location, latitude, longitude

time - timestamps of records in songplays broken down into specific units
start_time, hour, day, week, month, year, weekday

# Files in repository

sql_queries.py -> contains sql queries for dropping, inserting, creating fact and dimension tables.

create_tables.py -> contains code for setting up database together with fact & dimension table.

etl.ipynb -> a jupyter notebook to analyse data

etl.py -> reading & processing both files

test.ipynb -> testing the data availability in the tables.

# How to run the python scripts

- Wrote drop, create and insert statements in sql_queries.py

- Run create_tables.py in console

- Used test.ipynb to validate that all tables were correctly.

- Followed instructions in etl.ipynb to complete the framework for ETL pipeline.

- Used test.ipynb to validate that all tables were correctly UPDATED.

- Run etl.py in console


