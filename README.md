# 10708
Project for 10708

This is the repo of the code for the project of 10708. There are mainly 3 types of files in this repo.

1. .csv files
These are the data files we have for the project.

a. FEDFUNDS.csv contains all the Fed Fund Rate published by Fed: https://fred.stlouisfed.org/series/FEDFUNDS. It covers the entire timescape of our training and testing data. The data frequence is "monthly".

b. HMM.csv contains all the states generated by the HMM model. It is generated by HMM.py file. Note that running it different times will yield different results because of the randomness.

c. data.csv contains all the daily data of S&P 500 from 1990 to 2022. The orginal data was obtained by running the Stock_Data.py file where we pull the Open/High/Low/Close/Volume daily data from Yahoo Finance. We then extended new columns by extracting some features from the original data.


2. .py files
These are the script files for the project.

a. HMM.py is the python file that we use to generate the HMM data mentioned above.

b. LR.py is the baseline Linear Regression Model we implemented. 

c. NN_vol_xxx_yy.py are the baseline Neural Network model we implemented. Here "xxx" indicates if we include the HMM data and "yy" indicates the number of days to look back in the model.

d. LSTM_vol_xxx_yyy_zz.py are the RNN model using LSTM structure. Here "xxx" indicates if we include the HMM data; "yyy" indicates if the LSTM part is single directional or bi-directional; "zz" indicates the number of days to look back in the model.

e. GRU_vol_xxx_yyy_zz.py are the RNN model using GRU structure. Here "xxx" indicates if we include the HMM data; "yyy" indicates if the GRU part is single directional or bi-directional; "zz" indicates the number of days to look back in the model.

f. Stock_Data.py is the file we run to get data from Yahoo Finance.

3. Data analysis files (To fill by Mingjun)


Note:
1. Some model scripts would yield different results if you run it multiple times. For those Neural Network models, if you notice that the loss of the first 6 epoch is stuck at 0.7, then you might need to rerun it. Or you will find that the final result is a straight line. My hypothessi here is that we run into some local minimum and get stuck there.
2. The original scripts were writte on Google Collab. Thus, if you see some system oprations in the script, feel free to delete those. To replicate, you might need to get raw_data by running the Stock_Data.py file and then run the code in models as those code would use the variable raw_data to be the dataset.



