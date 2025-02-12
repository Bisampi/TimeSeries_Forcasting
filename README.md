# TimeSeries_Forcasting

# **Time Series Analysis Using SARIMA Model**

## **Project Overview**  
This Python-based project demonstrates the process of performing time series forecasting using the **Seasonal Autoregressive Integrated Moving Average (SARIMA)** model. The dataset used contains **historical time series data**, and the primary objective is to build a SARIMA model that accurately predicts future values based on past observations. Additionally, this project includes the analysis of **Amazon rating counts** over the years and their forecasting.

## **Code Description**  
### **Importing Required Libraries**  
We begin by importing essential Python libraries such as **pandas, numpy, matplotlib**, and **statsmodels** for data manipulation, visualization, and time series analysis.

### **Reading the Dataset**  
We load the dataset from a CSV file and inspect the first few rows to understand its structure and contents.

### **Exploratory Data Analysis (EDA)**  
We perform exploratory data analysis to understand the dataset, including:  
- Checking data types and missing values  
- Computing summary statistics  
- Visualizing the time series data  

### **Data Preprocessing**  
We convert the **time column** to a datetime object and set it as the index for proper time series handling. Additionally, we ensure that the dataset has a consistent frequency for accurate analysis.

### **Seasonality and Trend Check**  
We plot the time series data to identify **trends and seasonality patterns** by marking key points and using moving averages for smoothing.

### **Decomposing the Time Series**  
The time series is decomposed into **observed, trend, seasonal, and residual** components to better understand its structure.

### **Stationarity Check**  
We use the **Augmented Dickey-Fuller (ADF) test** to determine whether the time series is stationary. If the test suggests non-stationarity, differencing is applied to make the data stationary.

### **Automating Stationarity Conversion**  
A function is implemented to iteratively apply **differencing** until the time series achieves stationarity based on the **ADF test results**.

### **Splitting the Data**  
The dataset is split into **training and test sets**, where the training set is used for model training and the test set for performance evaluation.

### **Auto ARIMA Model Selection**  
We use the **pmdarima library** to automatically select the optimal SARIMA model parameters by minimizing the **Akaike Information Criterion (AIC)**.

### **Fitting the SARIMA Model**  
The selected **SARIMA model** is trained on the training dataset.

### **Predicting with the SARIMA Model**  
The trained model is used to **forecast** values for the test dataset.

### **Model Evaluation**  
The model's performance is evaluated using:  
- **Mean Squared Error (MSE)**  
- **Root Mean Squared Error (RMSE)**  
- **Mean Absolute Error (MAE)**  
- **Mean Absolute Percentage Error (MAPE)**  

### **Retraining with the Entire Dataset**  
To make future predictions, the SARIMA model is **retrained** using the entire dataset.

### **Forecasting Future Values**  
The final trained model is used to generate **future forecasts**, and the results are visualized alongside historical data.

## **Amazon Rating Count Analysis and Forecasting**  
In addition to general time series forecasting, this project specifically analyzes **Amazon rating counts** over the years to predict future trends in user engagement and reviews. The following steps were performed:

### **1. Importing and Preprocessing the Rating Count Data**  
- The dataset contains a `Date` column and a `Rating_Count` column, representing the number of ratings over time.
- The dataset is converted to a time series format, ensuring a **monthly or yearly frequency**.

### **2. Trend and Seasonality Analysis**  
- The time series is plotted to visualize overall trends.
- A **seasonal decomposition** is performed to identify underlying seasonal patterns.

### **3. Stationarity Check and Differencing**  
- The **ADF test** is applied to check for stationarity.
- If necessary, differencing is applied to convert the series to a stationary form.

### **4. Model Selection and Training**  
- **Auto ARIMA** is used to find the best SARIMA model parameters.
- The model is trained using past Amazon rating counts.

### **5. Forecasting Future Amazon Rating Counts**  
- The trained SARIMA model is used to predict future rating counts.
- The predictions are visualized alongside historical data.

## **Output**  
The code generates various plots and statistical summaries, allowing for a clear understanding of the **time series trends, seasonality, decomposition, and model performance**. The **SARIMA model** forecasts future values, which are visualized for comparison with historical data. This includes:
- **Time series trends of Amazon ratings over time**
- **Seasonal variations in rating counts**
- **Future forecasted Amazon ratings for the next 12 months**

## **Conclusion**  
This project provides a comprehensive **time series analysis and forecasting workflow** using the **SARIMA model**. It covers essential steps such as **data preprocessing, stationarity conversion, model selection, training, evaluation, and forecasting**, making it a powerful tool for analyzing and predicting time series data. Additionally, the **Amazon rating count forecasting** highlights how SARIMA models can be leveraged to analyze customer engagement trends and predict future review behaviors on the platform.

