# Thesis: Time Series Forecasting Project

## Overview
This repository contains the code and results of my thesis project focused on time series forecasting for the price of wood waste in Germany. The project explores and compares several machine learning models, including ARIMA, Decision Trees, Random Forests, XGBoost, and Prophet, to predict the prices and analyze their performance.

## Requirements

To run the code in this project, you'll need:

- Python 3.x
- Jupyter Notebook
- Required Python libraries (NumPy, Pandas, Scikit-learn, Statsmodels, Prophet, Plotly etc.)

## Table of Contents
- [Thesis: Time Series Forecasting Project](#thesis-time-series-forecasting-project)
  - [Overview](#overview)
  - [Requirements](#requirements)
  - [Table of Contents](#table-of-contents)
  - [Data](#data)
  - [Models](#models)
    - [ARIMA](#arima)
    - [Decision Trees](#decision-trees)
    - [Random Forests](#random-forests)
    - [XGBoost](#xgboost)
    - [Prophet](#prophet)
  - [Evaluation Metrics](#evaluation-metrics)
  - [Results](#results)
  - [Visualizations](#visualizations)
  - [Usage](#usage)
  - [Contributing](#contributing)
 
## Data
The dataset used in this project consists of historical prices of wood waste in Germany. The data is divided into different clusters and categories for detailed analysis.

- **Raw Data:** Contains the original dataset.
- **Processed Data:** Contains the cleaned and preprocessed data used for modeling.

## Models
### ARIMA
- **Model Overview:** Autoregressive Integrated Moving Average (ARIMA) is used for time series data with trend and seasonality.
- **Configuration:** ARIMA(1,1,1) was chosen based on the lowest AIC.
- **Performance:** Compared using static and walk-forward validation.

### Decision Trees
- **Model Overview:** Non-linear model that splits data based on feature values.
- **Configuration:** Used static, rolling, and walk-forward validations.
- **Performance:** Evaluated using RMSE and direction accuracy.

### Random Forests
- **Model Overview:** Ensemble method combining multiple decision trees to reduce overfitting.
- **Configuration:** Parameters include the number of trees and max depth.
- **Performance:** Compared across static, rolling, and walk-forward validations.

### XGBoost
- **Model Overview:** Efficient and scalable implementation of gradient boosting.
- **Configuration:** Parameters include learning rate and max depth.
- **Performance:** Evaluated using RMSE and direction accuracy.

### Prophet
- **Model Overview:** Developed by Facebook for handling seasonality and holidays in time series data.
- **Configuration:** Used for static and walk-forward validations.
- **Performance:** Compared using RMSE and direction accuracy.

## Evaluation Metrics
- **RMSE (Root Mean Squared Error):** Measures the average magnitude of the errors.
- **Direction Accuracy:** Measures the accuracy of the model's ability to predict the direction of price movement.

## Results
The results from each model are stored in the `results` file. It contains the RMSE and direction accuracy for static, rolling, and walk-forward validations.

## Visualizations
Visualizations are created to compare the actual and predicted values, as well as the RMSE and direction accuracy across different models and validations.

## Usage
To run the project, follow these steps:
1. Clone the repository: `git clone https://github.com/yourusername/timeseries-forecasting.git`
2. Install the required packages:  

Since I used different notebooks, I had to call some dataframes from one notebook to another. 

For this, I first “stored” the dataframes using the command “%store <dataframe> in their own notebooks and called them from the results notebook using %store -r <dataframe>. This shouldn’t make a difference as long as you run the notebooks in this order:

3. First run 0_Cleaning_exploration.ipynb so that the cleaned dataframe is stored for the following notebooks to use
4. Then run 0_ACF_PCF.ipynb
5. Then run in the order as per the filename: 1_ARIMA, 2_DecisionTree, 3_RandomForest, 4_XGBoost and 5_Prophet
6. Then finally run the results notebook.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.
