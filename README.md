# Movie Recommendation System
## Overview
This project implements a content-based movie recommendation system using Python. It recommends movies based on their similarity to a user-selected movie, leveraging text features such as movie overviews and genres. The system uses the TMDB Top 10K Movies dataset and employs natural language processing techniques to generate recommendations.
Features

### Dataset: 
Utilizes the TMDB Top 10K Movies dataset, containing movie details like title, genre, and overview.
### Text Processing:
Combines movie genres and overviews into a single "tags" feature for analysis.
### Vectorization: 
Uses CountVectorizer to convert text data into numerical vectors, with a maximum of 10,000 features and English stop words removed.
### Similarity Calculation: 
Computes cosine similarity between movie vectors to identify similar movies.
### Recommendation Function: 
Recommends the top 5 movies similar to the user's input, with case-insensitive movie title matching.
###  User Interaction: 
Displays a list of available movie titles and prompts the user to select one for recommendations.

## Requirements
To run this project, you need the following Python libraries:
pandas
scikit-learn
You can install the dependencies using pip:
pip install pandas scikit-learn

## Dataset
id: Unique movie identifier
title: Movie title
genre: Movie genres
overview: Brief description of the movie

## How It Works

### Data Preprocessing:

Loads the TMDB dataset using pandas.
Selects relevant columns (id, title, genre, overview).
Combines overview and genre into a tags column for each movie.
Drops the overview and genre columns to create a streamlined dataset.


### Feature Extraction:

Uses CountVectorizer to transform the tags column into a matrix of word counts, ignoring English stop words.
The resulting matrix has a maximum of 10,000 features.


### Similarity Computation:

Calculates cosine similarity between all movie vectors to create a similarity matrix.


### Recommendation:

The recommend function takes a movie title as input.
Performs a case-insensitive search to find the movie in the dataset.
If found, retrieves the top 5 most similar movies based on cosine similarity scores.
If not found, informs the user that the movie is not in the dataset.


## User Interface:

Displays the first 20 movie titles from the dataset.
Prompts the user to input a movie title.
Outputs the top 5 recommended movie titles.

View the list of the first 20 movie titles displayed in the console.

Enter a movie title from the list when prompted.

Receive a list of 5 recommended movies similar to your selection.


### Example
Here are some movies you can choose from:
The Shawshank Redemption
The Godfather
The Godfather: Part II
The Dark Knight
12 Angry Men
...

### Enter a movie title from the list above: iron man

### Output:
Iron Man
Iron Man 3
Guardians of the Galaxy Vol. 2
Avengers: Age of Ultron
Star Wars: Episode III - Revenge of the Sith

## Limitations

The system relies on the TMDB dataset, so recommendations are limited to the movies included in top10K-TMDB-movies.csv.
The recommendation quality depends on the content of the overview and genre fields.
The system does not handle typos in user input; the movie title must match exactly (case-insensitive).
Only content-based filtering is used, without incorporating user ratings or collaborative filtering.

## Future Improvements

Add support for partial movie title matching or fuzzy search to handle typos.
Incorporate additional features like movie ratings or cast information for more accurate recommendations.
Implement a graphical user interface (GUI) for a more user-friendly experience.
Expand the dataset to include more movies or merge with other datasets.
Use advanced NLP techniques, such as TF-IDF or word embeddings, to improve feature extraction.


### The TMDB dataset is sourced from Kaggle.
### Built with Python, pandas, and scikit-learn.

