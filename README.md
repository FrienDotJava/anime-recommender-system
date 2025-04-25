# Anime Recommendation System

## Overview
This project implements a **collaborative filtering-based** anime recommendation system using deep learning. The system is designed to help users discover anime that aligns with their preferences based on historical ratings.

## Business Understanding
With the growing number of anime titles available, users often struggle to find content that matches their tastes. This project addresses that problem by building a recommendation system that:
- Provides personalized anime recommendations.
- Enhances user experience by suggesting relevant titles.

## Dataset
The project utilizes the [Anime Recommendation Database](https://www.kaggle.com/datasets/CooperUnion/anime-recommendations-database), consisting of two CSV files:
1. `anime.csv` - Metadata about anime titles, including **genre, type, rating, and number of members**.
2. `rating.csv` - User interactions in the form of **ratings**.

### Data Preprocessing
Before building the model, several preprocessing steps are applied:
- Handling missing values and duplicate records.
- Encoding categorical IDs.
- Normalizing rating data and preparing training and testing sets.

## Modeling Approach
The recommendation system is built using **Matrix Factorization** with **neural network embeddings**. Key components of the model include:
- **User Embedding**: Captures user preferences.
- **Anime Embedding**: Represents anime features.
- **Bias Terms**: Helps adjust for popularity effects.
- **Dot Product & Activation Functions**: Predicts user preferences.

The model is trained using **Mean Squared Error (MSE)** as the loss function and optimized using **Adam optimizer**.

## Evaluation
The system's performance is evaluated using standard recommendation system metrics:
- **MSE**: 0.1356
- **RMSE**: 0.3239

These results indicate high accuracy in predicting user preferences.

## Example Recommendations
Given a user’s past interactions, the system suggests **top-N** anime titles. Example recommendations:
1. *Kimi no Na wa.* (Drama, Romance, School, Supernatural)
2. *Steins;Gate* (Sci-Fi, Thriller)
3. *Clannad: After Story* (Drama, Fantasy, Romance, Slice of Life, Supernatural)
