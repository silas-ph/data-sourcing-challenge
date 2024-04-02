# data-sourcing-challenge
Module 6 Challenge
# Data Sourcing Challenge

## Overview
This repository contains the solution for the Data Sourcing Challenge, which includes accessing data from the New York Times API and The Movie Database API, merging and cleaning the data, and exporting it to a CSV file.

## Before You Begin
Before starting the Challenge, be sure to complete the following steps:

1. **Create a new repository**: Create a new repository for this project called `data-sourcing-challenge`. When creating your new repository, make sure to select "Python" under the "Add .gitignore" option to prevent accidentally uploading your API keys in your `.env` file.

2. **Clone the repository**: Clone the new repository to your computer.

3. **Add starter files**: Inside your local Git repository, add the starter files `retrieve_movie_data.ipynb` and `example.env` from your file downloads.

4. **Rename example.env**: Rename `example.env` to `.env` and add your API keys to the file.

5. **Ensure .env file is not listed**: Ensure the `.env` file is not listed when you perform a `git status` check on the repo before performing your `git add` action.

6. **Push changes**: Push these changes to GitHub or GitLab.

## Part 1: Access the New York Times API
1. Set up the base URL, filter query, sort, field list, begin date, and end date for the New York Times API.
2. Create an empty list called `reviews_list` to store the retrieved reviews.
3. Iterate through 20 pages (starting from page 0) to retrieve 200 reviews.
4. Extend the query URL to include the page parameter.
5. Make a GET request to retrieve the page of results and store the JSON data.
6. Write a try-except clause to handle errors and retrieve reviews from the JSON data.
7. Preview the first five results in JSON format and convert `reviews_list` to a Pandas DataFrame.
8. Extract the movie title from the "headline.main" column and save it to a new column called "title".
9. Use the `extract_keywords` function to convert the "keywords" column from a list of dictionaries to strings.
10. Create a list called `titles` from the "title" column.

## Part 2: Access The Movie Database API
1. Prepare The Movie Database query URL.
2. Create an empty list called `tmdb_movies_list` to store the results.
3. Initialize a variable called `request_counter` and increment it for every iteration through the titles list.
4. Loop through the titles list and make GET requests to The Movie Database API.
5. Extract relevant movie details from the JSON results and append them to `tmdb_movies_list`.
6. Preview the first five results in JSON format and convert them to a DataFrame called `tmdb_df`.

## Part 3: Merge and Clean the Data for Export
1. Merge the New York Times reviews and TMDB DataFrames on the "title" column.
2. Fix the columns containing lists (genres, spoken_languages, and production_countries).
3. Remove duplicate rows and reset the index.
4. Export the cleaned data to a CSV file without the DataFrame's index.

---
## Resources:
- Coursera
- Datacamp
- Solved in class work
- ASK BCS
- Stack Overflow
