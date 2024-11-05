
# Predicting StackOverflow Answer Times Using Machine Learning

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Requirements](#requirements)
- [Installation](#installation)
  - [1. Clone the Repository](#1-clone-the-repository)
  - [2. Set Up the Environment](#2-set-up-the-environment)
  - [3. Download the Dataset](#3-download-the-dataset)
- [Usage](#usage)
  - [Running the Project](#running-the-project)
  - [Project Workflow](#project-workflow)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction
This project aims to predict the time it takes for a question on StackOverflow to receive an answer using machine learning techniques. The project involves data preprocessing, exploratory data analysis (EDA), and implementing various machine learning models to find the best predictor.

## Dataset
The dataset is sourced from the UCI Machine Learning Repository, specifically the `answers.csv` file.

- **Download Link**: [answers.csv](#)
- **Description**: Contains StackOverflow questions, their associated answers, and metadata such as question score, views, tags, and timestamps.

## Requirements
- Python 3.x
- Apache Spark 3.3.1
- Java JDK 8
- Required Python packages:
  - `findspark`
  - `pyspark`
  - `numpy`
  - `matplotlib`

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

### 2. Set Up the Environment
Since the project is designed to run on Google Colab with Spark, you can set it up as follows:

- **On Google Colab**:
  - Open the `.ipynb` notebook in Colab.
  - Run the cells to install Java JDK 8, download and set up Apache Spark, and install `findspark`.

- **Locally**:
  - Install Java JDK 8.
  - Download and install Apache Spark 3.3.1.
  - Set the `JAVA_HOME` and `SPARK_HOME` environment variables.
  - Install the required Python packages using pip:
    ```bash
    pip install findspark pyspark numpy matplotlib
    ```

### 3. Download the Dataset
The code automatically downloads the dataset. Ensure you have an internet connection, or manually download `answers.csv` and place it in the project directory.

## Usage

### Running the Project
- **On Google Colab**:
  - Upload the notebook and run all cells sequentially.
- **Locally**:
  - Run the Python script:
    ```bash
    python your_script_name.py
    ```
  - Make sure Spark is properly configured.

### Project Workflow
1. **Spark Setup**:
   - Install Java JDK 8.
   - Download and extract Apache Spark.
   - Install `findspark` and initialize Spark.
   
2. **Exploratory Data Analysis**:
   - Load and preprocess the data.
   - Extract necessary fields and perform data cleaning.
   - Convert tags into numerical form using the top 20 tags.
   - Remove outliers based on the answer time.

3. **Machine Learning Models**:
   - Implement Linear Regression models with and without tags.
   - Experiment with polynomial features.
   - Use a Random Forest model for comparison.
   - Evaluate models using RMSE (Root Mean Square Error).

## Results
The best model was a Linear Regression model without tags, achieving the lowest RMSE. Plots comparing actual vs. predicted answer times are included in the notebook/script.
