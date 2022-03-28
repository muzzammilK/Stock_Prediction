# Stock_Prediction
Stock Open-price prediction model

This Jupyter notebook based HTML file contains a Python code, making use of Tensorflow Library to build a Bi-LSTM model which predicts the SBI stock open-price for any day provided the last 60-days stock open-price data. 

The code is pretty simple and self explanatory.

If the audience stills wants to understand the code logic, kindly refer the below description points.

Description Points:
1) Load the SBI stock data using nsepy.get_history class by passing the start-date, end-date and symbol parameters where symbol parameter is the Stock ID. Make sure to obtain pretty old stock data to consider for Model Training and pretty recent data for Model Evaluation.
2) Plot the open price data using Matplotlib.pyplot class 
3) Normalize the stock open-price data using MinMaxScaler class
4) Create Train-data with the logic that any day's stock open-price depends on its previous 60 days stock open-price data
5) Then re-shape the Train-data
6) Create/Build a Bi-LSTM model
7) Train the model with the re-structured Train-data
8) Obtain recent SBI stock data and keep them as Test-data
9) Re-structure the Test-data with similar logic as Train-data. So, in that aspect, last 60 data points of Train-data is to be used. Hence, logically, 1st data point of Test-data will depend on its previous 60 data points obtained from Train-data and so on
10) Now, re-structured Test-data is fed to the model for prediction and the predicted-values are stored
11) Now, the predicted stock price will be compared against the real stock price with a plot for evaluating the model performance.
12) Here, the real stock price would simply be the obtained raw Test-data's open-price data and Re-structured Test-data which includes last 60 data-points of Train-data is what we used to train the model.
13) Here, the comparison plot clearly indicates how well the model has performed.
