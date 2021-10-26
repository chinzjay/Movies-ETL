# Movies-ETL

## Overview
The purpose of this project is to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. The code is the refactored to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.

## Results
- ETL Function to Read Three Data Files
    An ETL function was written to read in the three data files - Wikipedia data, Kaggle metadata, and the MovieLens rating data (https://github.com/chinzjay/Movies-ETL/blob/main/ETL_function_test.ipynb).

- Extract and Transform the Wikipedia Data
    Using Python, Pandas, the ETL process, and code refactoring, the Wikipedia data was extracted and transformed to be merged with the Kaggle metadata (https://github.com/chinzjay/Movies-ETL/blob/main/ETL_clean_wiki_movies.ipynb). The IMDb IDs was extracted using regular expression string and duplicates were dropped and a try-except block was used to catch errors.

- Extract and Transform the Kaggle data
    The Kaggle metadata and MovieLens rating data was extracted and transformed, then the transformed data was coverted into separate DataFrames (https://github.com/chinzjay/Movies-ETL/blob/main/ETL_clean_kaggle_data.ipynb). The Kaggle metadata DataFrame was merged with the Wikipedia movies DataFrame to create the movies_df DataFrame. The MovieLens rating data DataFrame was merged with the movies_df DataFrame to create the movies_with_ratings_df.

- Create the Movie Database
    The movies_df DataFrame and MovieLens rating CSV data were added to a SQL database (https://github.com/chinzjay/Movies-ETL/blob/main/ETL_create_database.ipynb).

## Summary
As per Britta's requirement, an automated pipeline was created to take in Wikipedia data, Kaggle metadata and MovieLens rating data. The appropriate transformations were performed using variuos functions and the final cleaned data was loaded to PostgreSQL database.
