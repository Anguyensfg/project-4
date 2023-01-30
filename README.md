# project-4
## Introduction
Property market has great movement everyday. Buyers are always wondering:
 If this is the right values? 
 Should I be waiting? or 
 Am I late to enter the market?

 In this Project, we are attempting a model  to predict a property price based on data related to the house (type of the property). 
 During the development and evaluation of our model, we will show the code used for each step followed by its output. This will facilitate the reproducibility of our work. 
 In this study, number of Python packages and libraries are used.

## Goals of the Study
The main objectives of this study are as follows:

Clean and tame the data to bring the most consistent for of it.
To build machine learning models able to predict house price based on house features
To analyze and compare models performance in order to choose the best model

### Assumptions
Even though we are trying to train model closest to the perfect the important decision of one's mabe biggest investment of the life can't be based on few factors. Hence we would like to clarify few assumptions of the project.

1) No pandemic- This model is not designed with the consideration of the panademic. 
2) No first home buyer boom- we have not added a consideration for the government supports for the first home buyers.
3) No banks - Interest rates, tax savings and ease of lending these factors are not considered in the model.

## Models Used
* Model 1: Linear regression model
* Model 2: Deep learning model using Keras 

## Model Preparation
* Renamed columns
* Dropped null records
* Filtered to ACT properties
* Dropped unneccessary columns
* Converted Date Sold to Month and Year sold columns
* Converted property type column from string to numerical value
* Split, scale the preprocessed data
* For Keras model, utilised 5 hidden layers and 1 output layer, with 8 neurons on the hidden layers
* Used ADAM optimisation algorithm for optimising the loss function (mean squared error)

## Model Performance Evaluation

| | Linear Regression | Keras Regression |
|---|---|---|
|Mean Absolute Error | 132944.42 | 105160.75 |
|Mean Squared Error | 37424819461.94 | 26696349075.46|
|Root Mean Squared Error | 193454.95 | 163390.17 | 
|Variance Score | 57.52 | 69.71 |

## Model Result Comparison
* Showing first 10 rows only

| | | Linear Regression | Keras Regression |
|---|---|---|---|
| | Actual Sold Price | Model Predicted Price| Model Predicted Price |
|1|500000|556277|502713|
|2|415000|555837|499446|
|3|1700000|1031199|1285180|
|4|680000|831717|731213|
|5|355000|385473|379196|
|6|400000|395733|361695|
|7|460000|520468|417202|
|8|330000|392015|497613|
|9|609000|770292|711002|
|10|530000|483061|533381|

## Limitations & Further Improvements
* Bigger dataset with more parameters would be ideal, with parameters such as:
   * Size of the property (sqm)
   * No of floors
   * No of bathrooms
   * Condition (scale of 1-10)
   * Year built
* Perhaps manually splitting the dataset into 3 distinct datasets according to the property type before training and running the neural network model may improve the variance score 

