# Steelcase - RDC Team 2
GA Tech - OMSA - Analytics Practicum Spring 2023
##


**Regional Distribution Center - Inventory Management and Forecasting**

The primary objective of this practicum was to optimize the utilization of Steelcase’s inventory through a comprehensive analysis of historical data and the identification of future trends. The code base provides an overview of the company’s current inventory management and the methodology used in the practicum as well as the results of the analysis. The analysis was carried out using various tools, including Excel, Python, SQL Lite, and Tableau. The results of the analysis provided insights into the historical performance of inventory and identified trends that could affect future inventory levels. The findings and recommendations presented in this report can be used by Steelcase to develop strategies for optimizing inventory levels and floor space utilization, thereby improving the company’s supply chain management.

**Getting Started**

To run the code, you will need Python 3 and the following libraries (and more) installed:

- Pandas
- Scikit-learn
- sqlite3
- fbprophet
- plotly
- etc.,

**Usage**

The repository contains several Python files that implement different parts of the inventory forecasting pipeline:
1. Step 1 - Combine_PiecesinNetworkData_SixMonths.ipynb : Contains code logic to combine all the daily 'Network in pieces' file in to one sigle dataframe, we leverage google colab pro and file formats like .parquet files to optimize this step of the process.
2. Step 2 - Network_Scripts_FinalData.ipynb : Contains many functions to clean and aggregate the data step by step to arrive at a daily data that has new attributes for each RDC like dwell time, age of the inventory, inventory turn around time etc.,
3. Step 3 - Forecasting_Final_wTuning.ipynb : Contains functions to prepare the data for fbprohet model and also has fucntions to find the best fit model based on hyper parameter tuning for the two main metrics Incoming and Outgoing inventory
4. Step 4 - TwoYear_Inventory_Vol_Sql_DataCleaning.ipynb : This code contains series of steps to pull the archive data from the latest 'pieces in network scripts' and convert that in to a clean dataframe and also a sqllite DB. In our project we have use this dataset to build prediction models for the In building total inventory and the squarefeet used for each RDC on a daily basis
5. Step 5 - Forecasting_Final_Total_Inv_sqft_w_tuning.ipynb: Contains functions to prepare the data for fbprohet model and also has fucntions to find the best fit model based on hyper parameter tuning for the two main metrics Total In building Inventory and Square feet usage
6. Step 6 - Combine_Forecast and Actuals_0329.ipynb: Finally this file contains the code to combine all the actuals and the forecasting data into one dataset

The files path needs to be changed as per your requirements based on where the user of this code base choses to save the raw files and the output files

Each of these scripts generates output files that can be used as inputs for the subsequent steps in the pipeline.


**License**

This code is released under the MIT License.
