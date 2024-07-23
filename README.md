# Module 6 Challenge - Movie Reviews Data Retrieval and Analysis

This repository contains a Jupyter Notebook that retrieves and analyzes movie reviews from The New York Times and movie details from The Movie Database (TMDB). The analysis involves combining data from both sources, cleaning the data, and preparing it for further analysis.

## Analysis Overview

### Part 1: Retrieve Movie Reviews from The New York Times

1. **Construct the Query URL**
    - Base URL: `https://api.nytimes.com/svc/search/v2/articlesearch.json?`
    - Filter for movie reviews with "love" in the headline.
    - Use a date range from 2013-01-01 to 2023-05-31.
    - Sort by newest.

2. **Retrieve and Store Reviews**
    - Loop through 20 pages of results.
    - Store the reviews in a list.
    - Convert the list to a DataFrame.
    - Extract the movie title from the "headline.main" column.

### Part 2: Retrieve Movie Details from TMDB

1. **Prepare the Query**
    - Use the titles from the reviews DataFrame.
    - Search for each title on TMDB to get the movie ID.
    - Use the movie ID to get full movie details.

2. **Store Movie Details**
    - Extract genres, spoken languages, and production countries.
    - Store the details in a list of dictionaries.
    - Convert the list to a DataFrame.

### Part 3: Merge and Clean the Data

1. **Merge DataFrames**
    - Merge the New York Times reviews and TMDB DataFrames on the title column.

2. **Clean Data**
    - Convert list columns to strings.
    - Remove unnecessary characters.
    - Drop unnecessary columns.
    - Remove duplicate rows and reset the index.

3. **Export Data**
    - Export the cleaned DataFrame to a CSV file.

## Requirements

To run this project, you will need API keys for:

- [New York Times API](https://developer.nytimes.com/get-started)
- [TMDB API](https://developers.themoviedb.org/3/getting-started/introduction)