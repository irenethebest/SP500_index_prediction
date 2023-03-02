# S&P 500 index prediction

## Project/Goals 
Predicting following month's S&P index return based on current month's macro-economic information. 

Date of the project : September 2022 (Data used for the prediction is up to August 2022)

## Features used:
 - Consumer_sentiment_index
    - Source : University of Michigan Consumer Surveydata.nasdaq.com/data/UMICH/SOC1 university of michigan consumer surveyindex of consumer sentiment

- S&P Put/Call Ratio
    - The SPX Put/Call Ratio is an indicator that is used to gauge market sentiment. This is calculated as the ratio between trading S&P 500 put options and S&P call options. A high put/call ratio can indicate fear in the markets, while a low ratio indicates confidence. For example, in 2015, the Put-Call ratio was as high as 3.77 because of market fears stemming from various global economic issues like a GDP growth slowdown in China and a Greek debt default.  
    - Source: CBOE (Chicago Board Options Exchange) website 

- SP500_PE_RATIO_MONTH
    - The S&P 500 PE Ratio is the price to earnings ratio of the constituents of the S&P 500. The S&P 500 includes the 500 largest companies in the United States and can be viewed as a gauge for how the United States stock market is performing. The price to earnings ratio is a valuation metric that gives a general idea of how a company's stock is priced in comparison to their earnings per share. Historically, the S&P 500 PE Ratio peaked above 120 during the financial crisis in 2009 and was at its lowest in 1988.  
    - Source: Nasdaq website
    
- CBOE_volatility_index ('vo')
    - a popular measure of the stock market's expectation of volatility based on S&P 500 index options. It is calculated and disseminated on a real-time basis by the CBOE, and is often referred to as the fear index or fear gauge.
    - Source:  Chicago Board Options Exchange

- Treasury Note (10 year) and Treasury Bill (3 month) rate
    - Many analysts will use the 10 year yield as the "risk free" rate when valuing the markets or an individual security. Historically, the 10 Year treasury rate reached 15.84% in 1981 as the Fed raised benchmark rates in an effort to contain inflation.
    - The 3 month treasury yield hovered near 0 from 2009-2015 as the Federal Reserve maintained its benchmark rates at 0 in the aftermath of the Great Recession.
    
- Other indices such as Nikkei('Nk')/Russell2000('R')/Nasdaq('Nas')


This repository contains a classification model to predict the following month's S&P index return based on current month's macro-economic information.

## Dataset
The dataset used for training and testing the model contains macro-economic data for various factors, such as interest rates, inflation, GDP growth, and other economic indicators, along with the S&P index return for each month. The dataset can be found in the data directory, and it is divided into training and testing sets.

## Model
The classification model used in this project is a Random Forest classifier, which is a type of ensemble learning method that builds multiple decision trees and combines their predictions to produce a final output. The implementation of the model can be found in the model.ipynb notebook.

## Evaluation
The performance of the model is evaluated using the accuracy score, which measures the proportion of correct predictions made by the model. The accuracy score is calculated using the testing set and can be found in the evaluation.ipynb notebook.

## Usage
To use the model to make predictions, simply run the model.ipynb notebook and input the macro-economic data for the current month. The output of the model will be the predicted classification for the following month's S&P index return.

## Requirements
The following libraries are required to run the notebooks in this repository:

Pandas
NumPy
Scikit-learn
These libraries can be installed using pip:

`pip install pandas numpy scikit-learn` 

## License
This project is licensed under the MIT License - see the LICENSE file for details.
