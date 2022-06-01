# MSCA-31006-Final-Project

This project will use the telecommunicaion dataset from kaggle, which contains the eletronic power consumption information from household in Sceaux, France . The project will focus on the prediction of time series data on variables: Global active power, sub_metering_1, sub_metering_2, and sub_metering_3 by various of time series prediction models using R. The meaning of the variables attached below.

1.date: Date in format dd/mm/yyyy
2.time: time in format hh:mm:ss
3.global_active_power: household global minute-averaged active power (in kilowatt)
4.global_reactive_power: household global minute-averaged reactive power (in kilowatt)
5.voltage: minute-averaged voltage (in volt)
6.global_intensity: household global minute-averaged current intensity (in ampere)
7.sub_metering_1: energy sub-metering No. 1 (in watt-hour of active energy). It corresponds to the kitchen, containing mainly a dishwasher, an oven and a microwave (hot plates are not electric but gas powered).
8.sub_metering_2: energy sub-metering No. 2 (in watt-hour of active energy). It corresponds to the laundry room, containing a washing-machine, a tumble-drier, a refrigerator and a light.
9.sub_metering_3: energy sub-metering No. 3 (in watt-hour of active energy). It corresponds to an electric water-heater and an air-conditioner. 

Project starts with EDA and regrouping. Since the raw data is grouped by miniute, and the electricity power consumption is logically grouped by month, we regrouped it monthly for the modeling part. Then Holt Winter, ARIMA, SARIMA, BSTS, and Prophet is used to predict the global active power, and the best model is Holt Winter. For the three sub-meterings, ARIMA with error, Linear Regression, BSTS, and Prophet are used and the best model is listed below.
Sub_metering_1: BSTS with global active power as regressor.
Sub_metering_2: ARIMA with global active power and reactive power as regressors.
Sub_metering_3: ARIMA with global active power as regressor.
### The best model is evaluated by the RMSE, sMAPE, AICc, and BIC.
