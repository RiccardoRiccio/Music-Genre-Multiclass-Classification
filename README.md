# Music Genre Multi-class Classification

This project leverages Machine Learning techniques to perform multi-class classification on musical tracks, effectively categorizing them into distinct genres.

## Table of Contents
1. [Project Structure](#project-structure)
2. [Getting Started](#getting-started)
3. [Introduction](#introduction)
4. [Problem Statement](#problem-statement)
5. [Dataset](#dataset)
6. [Exploratory Data Analysis](#exploratory-data-analysis)
7. [Preprocessing and Feature Engineering](#preprocessing-and-feature-engineering)
8. [Model Selection](#model-selection)
9. [Model Optimization](#model-optimization)
10. [Ensemble Methods](#ensemble-methods)
11. [Evaluation Metrics](#evaluation-metrics)
12. [Contributors](#contributors)

## Project Structure

- `/notebooks`:
  - `RiccardoRiccio_506483_Exam22_02.ipynb`: The main Jupyter notebook containing the analysis and machine learning model.
  
- `/data`:
  - (You may want to include your data files here, or provide instructions on how to obtain the data)
  
- `requirements.txt`: List of Python libraries required for this project.

## Getting Started

### Prerequisites

- Ensure you have Python installed on your machine.
- It's advisable to create a virtual environment to manage dependencies for this project.

### Installation

1. Clone this repository to your local machine.
   ```bash
   git clone https://github.com/RiccardoRiccio/Music-Genre-Multiclass-Classification.git


## Introduction

This project aims to classify music tracks into 11 different genres using machine learning techniques. The project is implemented in Python and uses various libraries for data manipulation, visualization, and machine learning.

## Problem Statement

The goal is to classify music tracks into 11 different genres (e.g., rock, pop, etc.) based on various features like artist name, track name, popularity, danceability, etc. The problem is a multiclass classification problem.

## Dataset

The dataset used for this project is available on Kaggle and consists of 17996 rows and 17 columns. The target variable is 'Class'. The dataset can be downloaded [here](https://www.kaggle.com/datasets/purumalgi/music-genre-classification).

## Exploratory Data Analysis

- Checked the shape of the dataset.
- Inspected the first and last few rows.
- Checked for missing values.
- Obtained summary statistics.
- Visualized missing values, numerical and categorical features, and feature correlations.

## Preprocessing and Feature Engineering

- Handled high cardinality in 'Artist Name' and 'Track Name' using frequency encoding.
- Imputed missing values for 'Popularity' and 'Instrumentalness' using mean imputation.
- Scaled features like 'key' using MinMaxScaler.
- Applied OneHotEncoding to 'time_signature'.
- Custom transformation to unify the scale of 'duration_in min/ms'.

## Model Selection

- Used a pipeline that includes preprocessing, SMOTE for handling class imbalance, and a classifier.
- Tried various configurations for transformations and classifiers.
- Used RandomizedSearchCV for hyperparameter tuning.
- Evaluated models using cross-validation and F1-weighted score.

## Model Optimization

- Optimized the CatBoostClassifier using RandomizedSearchCV.
- Tried different hyperparameter configurations.
- The best model used default hyperparameters.

## Ensemble Methods

- Experimented with AdaBoost and Gradient Boosting.
- Used base estimators like RandomForestClassifier, LGBMClassifier, and CatBoostClassifier.
- Evaluated ensemble methods using accuracy, precision, recall, and F1-score.

## Evaluation Metrics

- The best-performing model was CatBoostClassifier with the following metrics on the test set:
  - Accuracy: 0.6381
  - Precision: 0.6349
  - Recall: 0.6381
  - F1-score: 0.6244
  - ROC-AUC score: 0.9399
