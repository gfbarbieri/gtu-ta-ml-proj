# Data Science Certificate Teaching Assistant
Machine learning project for the TA position at Georgetown.

### Author:
Greg Barbieri - [@gfbarbieri](https://github.com/gfbarbieri)  

## Description of Task
The goal of this project is to demonstrate knowledge and use of the data science pipeline, as well as machine learning models and the Yellowbrick library. I will accomplish these goals by predicting income categories of households participating in the Consumer Expenditure (CE) Interview survey, a survey conducted by the Census Bureau on behalf of the Bureau of Labor Statistics (BLS).

Three notebooks were drafted, each covering distinct portions of the data science pipeline: (1) ingestion and wrangling, (2) feature selection, and (3) model selection and evaluation including hyper-parameter tuning. The request was for one single notebook to cover the data science pipeline and demonstrate competency with ML models and the Yellowbrick library, so I compiled an abridged version of the three parts.

#### Part 1:
Part 1 demonstrates beginning the data pipeline, ingesting data over the web, using preprocessing techniques to encode a target variable, aggregating data to create features, using visual techniques to assess the quality of the data, and storing the data using WORM methodology.

#### Part 2:
Part 2 demonstrates assessing the relationship between features, specifically utilizing the Yellowbrick library to assess colinearity and class separation. This part demonstrates multiple approaches to scaling features using the sklearn library. Lastly, this notebook covers feature selection using feature importance and feature elimination techniques.

#### Part 3:
Part 3 demonstrates preprocessing, modeling using multiple classifiers, model evaluation using Yellowbrick's classification model visualizers, hyper-parameter tuning, and model output.

### Folder Organization
**data**: Data resulting from ingestion and wrangling process. Data is ingested from the [CE PUMD website](https://www.bls.gov/cex/pumd_data.htm) and stored in a SQLite database table.  
**notebooks**: The final notebook covering all competencies is called Predicting_Household_Income. Groups of topics are covered in three parts: ingestion and wrangling, feature selection, and model selection and evaluation.
**model**: Encoding, scaling, and model parameters.  

## Data Sources
1. [CE PUMD Website](https://www.bls.gov/cex/pumd.htm)

*Note on Prediction*: Methodologically, prediction involves using current or past data to predict future data, where current, past, and future take their usual place in time. In machine learning, using data as a feature (predictor) that is generated chronologically after the target (predicted) can be a source of data leakage. This is relevant since the data I am using to predict household income is almost certainly an activity that takes place chronologically after the household income has already been earned. This is built into the design of the survey, since any expenditure behaviors are a function of income (under any decent theory of consumption where income determines lifestyle). My final word on the topic: in real-life it may be that future data is the data you wish you had and the current or past data is the data you have now--meaning the chronology of the data refers to the time you receive the data, not when it is theoretically generated by a the user. That is, for this task we are *inferring* income earned (past) using currently available data (present).
