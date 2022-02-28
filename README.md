# Data Science Certificate Teaching Assistant
Machine learning project for the TA position at Georgetown.

### Author:
Greg Barbieri - [@gfbarbieri](https://github.com/gfbarbieri)  

## Description of Task
The goal of this project is to demonstrate knowledge and use of the data science pipeline, as well as machine learning models and the [Yellowbrick](https://www.scikit-yb.org/en/latest/) library. I accomplish these goals by predicting the income categories of households participating in the [Consumer Expenditure (CE)](https://www.bls.gov/cex/home.htm) Interview survey, a survey conducted by the Census Bureau on behalf of the Bureau of Labor Statistics (BLS).

Three notebooks were drafted, each covering distinct portions of the data science pipeline: (1) [ingestion and wrangling](notebooks/Part_1_Ingest_Wrangle_Data.ipynb), (2) [feature selection](notebooks/Part_2_Exploration_Feature_Selection.ipynb), and (3) [model selection and evaluation including hyper-parameter tuning](notebooks/Part_3_Model_Selection_Evaluation.ipynb). The request was for a single notebook that covers the entire pipeline and demonstrates competency with ML models and the Yellowbrick library, so I created an [abridged version](notebooks/Predicting_Household_Income.ipynb) of the three parts.

### Part 1:
Part 1 demonstrates ingesting data over the web, using preprocessing techniques to encode a target variable, aggregating data to create features, using visual techniques to assess the quality of the data, and storing the data using WORM methodology.

### Part 2:
Part 2 demonstrates assessing the relationship between features, specifically utilizing the Yellowbrick library to assess [colinearity](https://www.scikit-yb.org/en/latest/api/features/rankd.html#rank-2d) and [class separation](https://www.scikit-yb.org/en/latest/api/features/radviz.html). This part demonstrates multiple approaches to scaling features using the sklearn library. Lastly, this notebook covers feature selection using [feature importance](https://www.scikit-yb.org/en/latest/api/model_selection/importances.html) and [feature elimination](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.RFECV.html) techniques.

### Part 3:
Part 3 demonstrates preprocessing, modeling using multiple classifiers, model evaluation using Yellowbrick's classification model visualizers, hyper-parameter tuning, and model output.

### Contents
**data**: Data resulting from ingestion and wrangling process. Data is ingested from the [CE PUMD website](https://www.bls.gov/cex/pumd_data.htm) and stored in a SQLite database table.  
**notebooks**: The final notebook covering all competencies is [Predicting_Household_Income.ipynb](notebooks/Predicting_Household_Income.ipynb). Groups of topics are covered in three parts: ingestion and wrangling, feature selection, and model selection and evaluation.  
**model**: Encoding, scaling, and model parameters.  

## Data Sources
1. [CE PUMD Website](https://www.bls.gov/cex/pumd.htm)

*Note on Prediction*: Prediction typically means using past data to estimate future data, where past, present, and future take their usual place in time. Since the data I am using to predict household income (expenditures) was created chronologically after the household income was earned or expected to be earned, a better phrase is that I am _explaining, inferring, or imputing_ household income. In fact, using data produced choronologically after the data one is trying to predict may become a source of data leakage. That said, in the real world, data leakage is more concerned about when the data is available to the model, not when it is theoretically generated by the user. That is, "future data" is simply the data you wish you had and "current" or "past" data are the data you have available now to make a prediction.
