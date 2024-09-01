# Project Title: Fraudulent E-Commerce Transactions Analysis

## Overview

This project involves analyzing a large dataset of e-commerce transactions to detect and predict fraudulent activities. The dataset is composed of over 1.49 million records containing various features related to transactions, customers, and the context in which the transactions were made. The goal is to preprocess the data, perform exploratory data analysis (EDA), and build machine learning models to identify fraudulent transactions.

## Project Structure

### 1. Data Loading
The dataset is loaded from CSV files, either directly from local storage or by fetching from the internet using provided URLs. Due to the size of the dataset, the loading process is optimized using parallelization with the ThreadPoolExecutor for faster execution.

### 2. Data Preprocessing
Cleaning Column Names: The column names are cleaned by converting them to lowercase, replacing spaces with underscores, and stripping any extra spaces.
Handling Missing and Erroneous Data: The project includes methods to handle any missing or erroneous data, such as replacing negative ages with the median age.
Date and Time Features: The transaction_date column is converted to a datetime format, and additional features such as the day of the week and month are extracted.
One-Hot Encoding: Categorical variables like payment_method, product_category, and device_used are transformed into numerical features using one-hot encoding.
### 3. Exploratory Data Analysis (EDA)
Descriptive Statistics: The dataset's basic statistics are computed, including mean, median, standard deviation, and more.
Distribution Visualization: Histograms and boxplots are used to visualize the distribution of numerical features, helping to identify outliers and data imbalances.
Correlation Analysis: A correlation heatmap is generated to understand the relationships between numerical features and to guide feature engineering.
### 4. Handling Imbalanced Data
The dataset is highly imbalanced, with the majority of transactions being non-fraudulent. To address this, undersampling is performed to create a balanced dataset with an equal number of fraudulent and non-fraudulent transactions for training the models.

### 5. Feature Engineering
Numerical Features: Key features include transaction_amount, customer_age, account_age_days, and transaction_hour.
Categorical Features: Categorical features are converted to numerical values using one-hot encoding.
Additional Features: New features, such as the day of the week, are created to capture potential patterns in fraudulent activities.
### 6. Model Building
The project includes several machine learning models from the sklearn library:

RandomForestClassifier
AdaBoostClassifier
DecisionTreeClassifier
BaggingClassifier
GradientBoostingClassifier
These models are trained on the processed and balanced dataset. Hyperparameter tuning is performed using GridSearchCV and RandomizedSearchCV.

### 7. Model Evaluation
The performance of the models is evaluated using metrics such as:

#### R2 Score
#### Mean Absolute Error (MAE)
#### Mean Squared Error (MSE)

### 8. Visualization
Visualization is a crucial part of the analysis, with plots generated using matplotlib and seaborn to illustrate:

#### Distribution of features
Correlation between variables
The performance of machine learning models

## Requirements

- matplotlib
- seaborn
- sklearn
- pandas
- numpy
- concurrent.futures (for parallel processing)

## Usage

This project demonstrates a comprehensive approach to fraud detection in e-commerce transactions. By carefully preprocessing the data, addressing imbalances, and applying a range of machine learning techniques, we aim to build robust models capable of identifying fraudulent activities effectively.

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute the code as needed.

