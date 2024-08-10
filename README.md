# TMDb Database Analysis

## Overview
The TMDb Database Analysis project explores and extracts insights from The Movie Database (TMDb), a comprehensive dataset containing information about movies and TV shows. This project aims to:

Analyze Historical Data: Discover trends and historical data about movies, including the oldest films and their characteristics.

Examine Awards: Query and analyze Oscar award data to identify trends and notable winners.
Explore Movie Genres: Investigate genres and keywords to find patterns, such as the most common genres and movies with specific themes.

Assess Production Companies: Identify top production companies based on movie popularity.

Update and Create Views: Perform data cleaning and create views to simplify complex queries and enhance data accessibility.

This analysis is designed to help users understand movie trends, award histories, and genre dynamics using TMDb's extensive dataset. Whether you are a researcher, a data analyst, or a movie enthusiast, this project provides valuable insights into the movie industry.

![TMDb ER Diagram](TMDB_ER_diagram.png)

## Setup

1. **Load SQL Extension**: Ensure you have `mysql` and `pymysql` installed.
    ```python
    %load_ext sql
    ```

2. **Connect to Database**: Download the `TMDB.db` SQLite file and connect to it.
    ```python
    %sql sqlite:///TMDB.db
    ```

## Example Queries

### 1. Oscar Winners

**Find the 2015 Oscar winner for “Actor in a Leading Role”:**
```sql
%%sql
SELECT * FROM oscars WHERE year = 2015 AND award = 'Actor in a Leading Role';
