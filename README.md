Module 6 Challenge
# Data Sourcing Challenge
# Problem Statement
Prepare data for a recommendation system to help people find movie reviews and related movies. The data is from two different sources: The New York Times API and The Movie Database. After the data has been extracted, clean the two databases and merged them. 

## Solution

### Part 1
- **Step 1**: Using the New York Times API, create a reviews list to store reviews from 01/01/2013 to 05/31/2023 that contain the word “love” in the headline that will be stored in a DataFrame.  The New York Times API only returns 10 results at a time, and we were tasked with retrieving 200 reviews. Using the sleep function and loops the code performs a total of 20 calls to retrieve all of the results.
- **Step 2**: Using the json method we normalized the data and stored the results in a DataFrame.
### Part 2
- **Step 1**: Using the tmdb API I created an empty list to store the tmdb movies list.  
- **Step 3**: Using the titles list from Part 1, I looped through the titles, extracted the movie details that included - title, original_title, budget, original_language, homepage, overview, popularity, runtime, revenue, release_date, vote_average, vote_count, genres, spoken_languages, and production_countries, and stored them in a DataFrame.

### Part 3
- **Step 1**: The final step involved merging the two DataFrames on the title column and clean the data. This involved, removing characters, converting columns to strings, deleting duplicate rows, and resetting the index.
- **Step 2**: Take the cleaned and merged data and export to a .csv file without the DataFrame’s index.
## Resources:
- Coursera
- Datacamp
- Solved in class work and asking classmates for help
- ASK BCS
- Stack Overflow
- Pandas Documentation https://pandas.pydata.org/docs/user_guide/index.html#user-guide
- Tutoring Sessions