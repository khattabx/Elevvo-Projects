# Titanic Exploratory Data Analysis (EDA)

## Overview

This project performs an Exploratory Data Analysis (EDA) on the classic Titanic dataset. The goal is to understand the dataset's structure, identify missing values, clean the data, and visualize key patterns and correlations related to passenger survival. This analysis is a foundational step in machine learning projects, providing insights that can inform feature engineering and model selection.

## Project Structure

The project is implemented in a Jupyter Notebook (`titanic_report.ipynb`) and utilizes Python libraries such as Pandas for data manipulation and Seaborn/Matplotlib for data visualization.

## Main Topics Covered

### 1. Data Loading and Initial Exploration

- Loading the `train.csv` dataset into a Pandas DataFrame.
- Checking the dimensions of the dataset (rows and columns).
- Viewing the first and last few rows to get a glimpse of the data.

### 2. Data Types and Missing Data Handling

- Examining the data types of each column to ensure they are appropriate for analysis.
- Identifying and quantifying missing values across all columns. This is crucial for data cleaning.

### 3. Data Visualization

- Generating various plots to understand the distribution of key features and their relationship with survival.
- Visualizations include:
    - **Death vs. Survival Count**: A bar plot showing the number of passengers who survived versus those who did not.
    - **Passenger Class Counts**: A bar plot illustrating the distribution of passengers across different classes (1st, 2nd, 3rd).
    - **Gender Counts**: A bar plot displaying the distribution of male and female passengers.
    - **Embarked Counts**: A bar plot showing the number of passengers who embarked from different ports.
    - **Age Histogram**: A histogram to visualize the distribution of passenger ages.

## Bonus: Survival Rate Visualizations

- Further analysis includes visualizing survival rates based on different categorical variables such as gender and passenger class using bar plots and potentially heatmaps to show correlations.

## How to Run the Project

1. Clone the repository:

   ```bash
   git clone git@github.com:khattabx/Titanic-Report.git
   cd Titanic-Report
   ```

2. Ensure you have Python and Jupyter Notebook installed. If not, you can install Anaconda, which includes both.
3. Install the required libraries:

   ```bash
   pip install pandas numpy pylab seaborn
   ```

4. Open the Jupyter Notebook:

   ```bash
   jupyter notebook titanic_report.ipynb
   ```

5. Run all cells in the notebook to reproduce the analysis and visualizations.

## Dataset

The dataset used is the classic Titanic: Machine Learning from Disaster dataset, commonly found on Kaggle. It contains various information about the passengers on the Titanic, including their age, gender, passenger class, and whether they survived the disaster.
