# ML-Based-Phishing-Website-Detection

This repository contains the implementation of various machine learning models to classify websites as legitimate or phishing. The analysis involves data preprocessing, model training, evaluation, and comparison of multiple classifiers including Decision Tree, Naïve Bayes, Bagging, Boosting, Random Forest, ANN, and SVM.

## Table of Contents
- [Dataset](#dataset)
- [Preprocessing](#preprocessing)
- [Models](#models)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)

## Dataset

The dataset contains 2000 rows and 26 columns with the following characteristics:
- All columns are of integer or numerical data types.
- The dataset includes NA values ranging from 11 to 27 across columns, except for the predictor `A01` and the target variable `Class`.
- The target variable `Class` has two values: "0" (legitimate) and "1" (phishing), with an uneven distribution.

## Preprocessing

1. **Handling NA values**: Removed rows with NA values, retaining 1556 rows and 26 columns.
2. **Removing Low Variance Predictors**: Dropped predictors with more than 99% values in a single category.
3. **Encoding Categorical Variables**: Converted predictors with less than 10 unique values to factor columns.
4. **Data Splitting**: Split data into training (70%) and testing (30%) sets.

## Models

The following models were implemented:

1. **Decision Tree**
2. **Naïve Bayes**
3. **Bagging**
4. **Boosting**
5. **Random Forest**
6. **Artificial Neural Network (ANN)**
7. **Support Vector Machine (SVM)**

## Results

- **Random Forest**: Highest accuracy and AUC, demonstrating robust performance in distinguishing between legitimate and phishing websites.
- **Naïve Bayes**: Lowest accuracy, primarily due to the assumption of independence between predictors.
- **ROC Curve**: All models performed better than a random classifier, with Random Forest showing the best performance.

## Installation

To run the code in this repository, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/sarviin-hari/ML-Based-Phishing-Website-Detection.git
    ```

2. Navigate to the project directory:
    ```bash
    cd ML-Based-Phishing-Website-Detection
    ```

3. Open the R Markdown file in RStudio:
    - Open RStudio and load the project directory.
    - Open the file `ML-Based-Phishing-Website-Detection.Rmd` in RStudio.

4. Install the required packages and run the R Markdown file:
    - Install necessary packages by running:
      ```r
      install.packages(c("data.table", "dplyr", "ggplot2", "caret", "e1071", "randomForest", "xgboost", "nnet"))
      ```
    - Render the R Markdown file to execute the code and generate the results:
      ```r
      rmarkdown::render("ML-Based-Phishing-Website-Detection.Rmd")
      ```

This will execute the code in the R Markdown file and produce the output, including model training and evaluation results.

## Usage

1. **Preprocess the Data**: Run the preprocessing script to clean and prepare the data.

2. **Train Models**: Run the training script to train all the models.

3. **Evaluate Models**: Run the evaluation script to generate performance metrics and comparison plots.

