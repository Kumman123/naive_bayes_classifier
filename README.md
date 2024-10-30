# Naive Bayes Classification on the Haberman Dataset

This repository contains a project that implements a Naive Bayes classifier to predict the survival status of patients with breast cancer using the [Haberman dataset](https://archive.ics.uci.edu/ml/datasets/Haberman%27s+Survival). The Naive Bayes algorithm is a simple yet powerful probabilistic classifier, commonly used for categorical classification tasks.

## Table of Contents

- [Dataset Overview](#dataset-overview)
- [Project Overview](#project-overview)
- [Implementation Details](#implementation-details)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Results and Evaluation](#results-and-evaluation)
- [Project Structure](#project-structure)
- [Additional Resources](#additional-resources)
- [License](#license)
- [Contact](#contact)

## Dataset Overview

The Haberman dataset is widely used in medical and machine learning research to study patient survival prediction. It contains information on patients who underwent breast cancer surgery, with data collected at the University of Chicago’s Billings Hospital from 1958 to 1969.

### Features

The dataset contains 306 instances, each with three input features and one target variable:

- **Age**: Age of the patient at the time of surgery (integer).
- **Year of Operation**: Year of the surgery (1958-1969).
- **Positive Axillary Nodes**: Number of positive axillary lymph nodes detected (integer).
- **Survival Status**:
  - 1 = Patient survived 5 years or longer.
  - 2 = Patient did not survive for 5 years.

## Project Overview

The objective of this project is to build a Naive Bayes classifier using the Haberman dataset to classify patients into two categories based on survival status. The steps include data preprocessing, training the model, and evaluating its performance through various metrics.

## Implementation Details

This project uses Python’s `scikit-learn` library, specifically the `GaussianNB` class, which assumes that the likelihood of the features follows a Gaussian (normal) distribution. 

### Steps in the Implementation

1. **Data Loading and Exploration**:
   - The data is loaded using `pandas`.
   - Exploratory Data Analysis (EDA) is performed to understand the distribution of the features and target variable.

2. **Data Preprocessing**:
   - **Handling Missing Values**: Though the dataset has no missing values, this step would ensure data integrity if needed.
   - **Feature Scaling**: Standardization is applied to bring all feature values to a similar scale, which can improve Naive Bayes performance.

3. **Model Training**:
   - The `GaussianNB` classifier from `scikit-learn` is used.
   - The training data is divided into training and testing sets to validate model performance.

4. **Model Evaluation**:
   - **Accuracy**: The percentage of correct predictions.
   - **Precision, Recall, and F1 Score**: Provides insight into how well the model is predicting each class.
   - **Confusion Matrix**: Gives a breakdown of true positives, false positives, true negatives, and false negatives for a more detailed performance analysis.

## Requirements

This project requires the following Python packages:

- `pandas` for data manipulation
- `numpy` for numerical operations
- `scikit-learn` for model training and evaluation

### Installation

You can install the required packages using:

```bash
pip install pandas numpy scikit-learn
