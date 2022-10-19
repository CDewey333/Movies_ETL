Movies ETL

Movie data from Wikipedia, Kaggle, and aggregated ratings were utilized to assemble a movie database from a clean dataset.
The ETL process was used to extract the Wikipedia and Kaggle data from their respective files, transform the datasets by cleaning rows and formatting datatypes, preforming joins, and loading the cleaned dataset into a SQL database.
Overview
The goal of this analysis is to create an automated pipeline that extracts, transforms and loads data. This analysis consists of four parts, where each step is building up from: the beginning of extracting data and function testing, transformation, cleaning process, to its final step of connect and load to the database. The entire process of ETL can be executed with a single function extract,_transform, and_load in the final step ETL_create_database.ipynb. The ETL process is broken down into four jupyter notebook files:
ETL_function_test.ipynb
•	Data is extracted from the website in JSON and CSV formats.
•	Data is transformed into Pandas data frames.
•	JSON file requires extra step – loading file first and then transforming into data frame.
ETL_clean_wiki_movies.ipynb
•	Function clean_movie combines scattered data of alternative languages into one column alt_titles.
•	Its subfunction change_column_name organizes column names into consistent pattern.
•	In the function extract_transform_load the transformation process of wiki movies data begins and includes:
- Python list comprehensions.
- apply() and map() methods in combination with lambda functions.
- regular expressions or RegEx.
ETL_clean_kaggle_data.ipynb
•	Function extract_transform_load gets new tasks for cleaning Kaggle data and includes:
- Changing datatypes, using methods pd.to_numeric, astype() and python comparison operators for Boolean types.
- Filling missing values and filtering unwanted columns.
- Merging data frames using pd_merge method.
ETL_create_database.ipynb
•	The function in its final step connects to the database by sqlalchemy library and to_sql method.
•	Complete ETL process can be executed with a single function extract_transform_load call.
