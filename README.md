# Teaching Assistant for the Data Science Certificate
Machine learning project for TA position at Georgetown. The goal is to demonstrate knowledge and use of the data science pipeline, as well as machine learning models and the Yellowbrick library.

### Author:
Greg Barbieri - [@gfbarbieri](https://github.com/gfbarbieri)  

### Folder Organization
**ing-wr-progs**: Programs used to ingest and wrangle CE Public-Use Microdata (PUMD). Data is ingested from the [CE PUMD website](https://www.bls.gov/cex/pumd.htm) and stored in a SQLite database table. Wrangling programs focus on missing data and data integrity, standardization and feature generation.  
**data**: Data resulting from ingestion and wrangling process.  
**notebooks**: Notebooks versions of ingestion and wrangling process, including target generation. Notebooks on exploratory data analysis (EDA), feature standardization, feature selection, machine learning models and output.
**model**: Model output.   

## Description of Task
The goal of this project is to predict income categories of households participating in the Consumer Expenditure (CE) Interview survey, a survey conducted by the Census Bureau on behalf of the Bureau of Labor Statistics (BLS). While combining data may enhance the model's predictive capability, for the sake of time both the target and features will come entirely from the CE survey.

*Caveat*: Methodologically, prediction involves using current or past data to predict future data, where current, past, and future take their usual place in time. In machine learning, using data as a predictor that is generated chronologically after the target (predicting) can be a source of data leakage, a problem in starting the ML process. This is relevant since the data I am using to predict household income is almost certainly an activity that takes place chronologically after the household income has already been earned (albiet, future income may be similar to past income when paid bi-weekly). This is built into the design of the survey, since any expenditure behaviors are a function of income (at least under any rational theory of consumption where income determines lifestyle, not the other way around). That said, my final take on topic: in real-life it may be that future data is simply the data you wish you had and the current or past data is simply the data you have now--meaning the chronology of the data refers to the time you receive the data, not when it is theoretically generated by a the user. That is, for this task we are *inferring* income (past) using currently available data (present).

## Project Overview
**Purpose**: Predict household income.  
**Target**:  CE household-level income classifications.  
**Features**: TBD  

## Data Sources
1. [CE PUMD website](https://www.bls.gov/cex/pumd.htm)
