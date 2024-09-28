# Movie Recommendation System

## Overview
This Movie Recommendation System utilizes collaborative filtering techniques to provide personalized movie recommendations based on user preferences and past interactions. The system aims to enhance user experience by suggesting movies that align with their tastes.

## Table of Contents
1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Installation](#installation)
4. [How It Works](#how-it-works)

## Features
- Provides personalized movie recommendations based on user ratings.
- Supports multiple recommendation algorithms, including SVD, NMF, and KNN.
- Ability to fine-tune recommendation algorithms through hyperparameter tuning.

## Technologies Used
- **Python**: Main programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **scikit-surprise**: Library for building and evaluating recommender systems
- **Matplotlib** / **Seaborn**: Data visualization
- **Jupyter Notebook**: For development and analysis

## Installation
To run this project locally, follow these steps:

1. Clone the repository: Open your terminal (or command prompt) and run the following command to clone the repository to your local machine:
   ```bash
   git clone https://github.com/EchoEvelyn/Movie_Recommendation_System.git

2. Change Directory: Navigate into the cloned repository:
   ```bash
   cd Movie_Recommendation_System

3. Set Up a Virtual Environment (Optional but Recommended): It’s a good practice to use a virtual environment to manage dependencies for your project. You can create and activate a virtual environment using the following commands:

 - For Windows:
   ```bash
   python -m venv venv
   venv\Scripts\activate
   
 - For macOS/Linux:
   ```bash
   python3 -m venv venv
   source venv/bin/activate

4. Install required packages: Make sure you have pip installed, and then run the following command to install the necessary libraries:
   ```bash
   pip install -r requirements.txt

5. Load the data: Ensure you have the required datasets in the correct format. You can either download them from the internet or place them in the data directory if your project structure requires it.

6. Run the application:
   ```bash
   jupyter notebook

## How it works
The Movie Recommender System project aims to provide personalized movie recommendations based on user preferences. The system utilizes a combination of algorithms, including Singular Value Decomposition (SVD), Non-Negative Matrix Factorization (NMF), and K-Nearest Neighbors (KNN), to generate accurate suggestions. The project is structured into the following phases:

   - Set-Up and Data Loading: The environment is configured, and the necessary data for building the recommendation model is loaded.
   - Data Exploration: A thorough exploratory data analysis (EDA) is conducted to understand user behavior, movie ratings, and patterns in the dataset.
   - Model Building: Various recommendation algorithms such as SVD, NMF, and KNN are explored. Hyperparameter tuning of SVD is performed to optimize model performance. The models are        trained and tested using evaluation metrics.
   - Model Evaluation: The models are evaluated based on metrics like precision, recall, and accuracy to assess the recommendation quality.
   - Recommendation Generation: Thresholds are determined to find optimal K recommendations, which are then evaluated to refine and make recommendations for users.
