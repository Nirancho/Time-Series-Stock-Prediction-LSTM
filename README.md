# Time-Series-Stock-Prediction-LSTM
This solution proposes an LSTM solution for time series stock prediction

## 1 Introduction
This report presents a recurrent artificial neural network solution for time series
analysis. Each section contains details regarding data processing and model
development. Long-Short-Term-Memory (LSTM) is a powerful approach for
time series analysis which is capable of training through back propagation. The
task is performed using Python in Jupyter Notebook.

## 2 Data Processing
It is important to understand data before processing. Given data is available in
multiple files in .tex format. Each file contains data for the given date. A single
file contains data of ‘Ticker’,‘Date’,‘Open’,‘High’,‘Low’, ‘Close’ and ‘Volume’ for
the stocks that were traded. All files were imported and concatenated.

### 2.1 Processing Data to Required Format
Date in ‘Date’ is available in int64 format and was converted to datetime format
first. Then data was analysed to check if there are any records for duplicated
‘Ticker’s. According to the task requirements, data needs to be arranged in to
a pivot table. Seperate dataframes were created for ‘Open’,‘High’,‘Low’, ‘Close’
and ‘Volume’.

### 2.2 Creating New Features
Future close return calculation requires current and future data and close return
calculation requires current data and past data. This can be performed with
loops but the most efficient way to handle it is via shifting. Shifting the same
dataframe by -1 and 1 gives future and past data respectively.

## 3 Exploratory Data Analysis
It is important to check missing values before treating them. Missing values can
be trated in two ways,
• Removing the records with missing values,
• Imputing the records with missing values.

First missing data can be observed in matrix and bar format. For ease of
analysis, here onward only a portion of dataframe has been used. It can be seen
from the Figure 1, that some tickers have random missing values, some does not
have enough records for analysis and some have very frequent missing values.
Missing values can be imputed in many ways. The method we pick should
be based on the data. Some of the options for imputing missing values in time
series are,
• Last Observation Carried Forward
• Next Observation Carried backward
• Interpolation
### 3.1 Treating Outliers
### 3.2 Scaling Data
## 4 Building LSTM Model
## 5 Model Performance Evaluation
