Home Price Prediction Model
This project aims to build a data science model to predict the U.S. home price index using publicly available economic and housing data over the last 20 years. The model uses Linear Regression to analyze the factors that influence home prices, such as mortgage rates, unemployment rates, consumer price index (CPI), GDP, and housing starts.

Project Overview
The model is built using data from the S&P Case-Shiller Home Price Index and other key economic indicators from FRED (Federal Reserve Economic Data). The goal is to predict how these factors have historically impacted home prices over a period of time.

Data Sources
S&P Case-Shiller Home Price Index: Represents the U.S. home prices.

Mortgage 30-Year Rate: Interest rate for 30-year fixed-rate mortgages.

Unemployment Rate: National unemployment rate.

Consumer Price Index (CPI): Measures the change in the average prices of a basket of goods and services.

GDP: Gross Domestic Product at constant prices.

Housing Starts: The number of new residential construction projects that have begun.

The data is sourced from the Federal Reserve Economic Data (FRED) API.

Requirements
To run the code, you will need the following Python libraries:

pandas

pandas_datareader

matplotlib

scikit-learn

You can install the necessary libraries using pip:

nginx
Copy
Edit
pip install pandas pandas_datareader matplotlib scikit-learn
Steps
1. Data Collection
Data is pulled from FRED for home prices, mortgage rates, unemployment rate, CPI, GDP, and housing starts, using the pandas_datareader library.

The data is retrieved from the following FRED series:

CSUSHPISA: Home Price Index

MORTGAGE30US: 30-Year Mortgage Rate

UNRATE: Unemployment Rate

CPIAUCSL: Consumer Price Index for All Urban Consumers

GDP: U.S. GDP (Constant Prices)

HOUST: Housing Starts

2. Data Cleaning
Missing values are handled by interpolation and any remaining missing data is dropped.

The dataset is prepared for analysis with all necessary columns and cleaned data.

3. Model Building
Independent variables (X) include Mortgage30YRate, UnemploymentRate, CPI, GDP, and HousingStarts.

The dependent variable (y) is the HomePriceIndex.

A Linear Regression model is trained using scikit-learn.

4. Model Evaluation
The model’s performance is evaluated using R2 Score and Mean Squared Error.

Feature importance (coefficients) is displayed to understand how each factor influences home prices.

5. Visualization
A scatter plot is generated to compare the Actual vs Predicted Home Price Index.

Steps in the Code
Define Data Period: The analysis starts from January 2000 to January 2025.

Data Retrieval: Using pandas_datareader, data is fetched from the FRED API.

Data Cleaning: Missing values are interpolated and cleaned.

Model Training: A Linear Regression model is trained with the data.

Model Evaluation: The performance of the model is assessed using R2 score and Mean Squared Error.

Visualization: A scatter plot is generated to compare predicted and actual values.

Model Performance
R2 Score: This score tells how well the model explains the variance in the data. A higher value indicates a better fit.

Mean Squared Error: Measures the average squared difference between actual and predicted values. Lower values are better.

Example Output
After running the model, the following outputs are generated:

R2 Score and Mean Squared Error for model evaluation.

Feature importance (coefficients) indicating the impact of each factor.

A plot comparing the actual vs predicted home price index.

Conclusion
This project provides insights into the factors affecting U.S. home prices, with a predictive model based on key economic indicators. The results can be used for further research or to aid decision-making in real estate and finance.
