# Movie Recommendation System

## Overview
This Movie Recommendation System utilizes collaborative filtering techniques to provide personalized movie recommendations based on user preferences and past interactions. The system aims to enhance user experience by suggesting movies that align with their tastes.

## Table of Contents
1. [Data](#data)
2. [Technologies Used](#technologies-used)
3. [Installation](#installation)
4. [How It Works](#how-it-works)

## Data
#### Movies Dataset
This dataset contains information about various movies. Each movie is identified by a unique movieId and includes its title and the genres it falls under.

- **movieId**: A unique identifier for each movie.
- **title**: The title of the movie, including the year of release.
- **genres**: A combination of genres associated with the movie, separated by a pipe (|), such as "Adventure|Animation|Children".

#### Ratings Dataset
This dataset contains user ratings for various movies. Each rating is associated with a user and a specific movie, along with the timestamp when the rating was given.

- **userId**: A unique identifier for each user.
- **movieId**: A unique identifier for the rated movie (corresponding to the movieId in the Movies dataset).
- **rating**: The rating given by the user, typically on a scale from 1 to 5.
- **timestamp**: The time when the rating was submitted, stored as a Unix timestamp.


## Technologies Used
- **Python**: Main programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **scikit-surprise**: Library for building and evaluating recommender systems
- **Matplotlib** / **Seaborn**: Data visualization
- **Jupyter Notebook**: For development and analysis

## Installation
#### Environment Setup

Ensure the following Python libraries are installed:
  
```bash
import numpy as np
import pandas as pd

import matplotlib.pyplot as plt
import seaborn as sns

from surprise.model_selection import KFold
from surprise.model_selection import cross_validate
from surprise import NormalPredictor
from surprise import KNNBasic
from surprise import KNNWithMeans
from surprise import KNNWithZScore
from surprise import KNNBaseline
from surprise import SVD
from surprise import SVDpp
from surprise import NMF
from collections import defaultdict
```

#### Authenticate with Google Drive:
Since I stored the dataset in Google Drive, I need to authenticate and access it using PyDrive and Google Colab:
```bash
from pydrive.auth import GoogleAuth
from pydrive.drive import GoogleDrive
from google.colab import auth
from oauth2client.client import GoogleCredentials
```
### Laod the Data From Google Drive
The dataset (e.g., watch_reviews.csv) is stored in Google Drive, and we use the file ID to retrieve it:
```bash
# Google Drive file ID
id_1 = 'your_google_drive_ratings_file_id_here'
id_2 = 'your_google_drive_movies_file_id_here'

# Download the dataset
file_1 = drive.CreateFile({'id': id_1})
file_1.GetContentFile('ratings.csv')
file_2 = drive.CreateFile({'id': id_2})
file_2.GetContentFile('movies.csv')

# Load the dataset into a Pandas DataFrame
ratings = pd.read_csv('ratings.csv')
movies = pd.read_csv('movies.csv')
```


## How it works
The Movie Recommender System project aims to provide personalized movie recommendations based on user preferences. The system utilizes a combination of algorithms, including Singular Value Decomposition (SVD), Non-Negative Matrix Factorization (NMF), and K-Nearest Neighbors (KNN), to generate accurate suggestions. The project is structured into the following phases:

   - Set-Up and Data Loading: The environment is configured, and the necessary data for building the recommendation model is loaded.
   - Data Exploration: A thorough exploratory data analysis (EDA) is conducted to understand user behavior, movie ratings, and patterns in the dataset.
   - Model Building: Various recommendation algorithms such as SVD, NMF, and KNN are explored. Hyperparameter tuning of SVD is performed to optimize model performance. The models are        trained and tested using evaluation metrics.
   - Model Evaluation: The models are evaluated based on metrics like precision, recall, and accuracy to assess the recommendation quality.
   - Recommendation Generation: Thresholds are determined to find optimal K recommendations, which are then evaluated to refine and make recommendations for users.
