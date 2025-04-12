# Prediction Assignment: Activity Recognition Using Accelerometers  
**Author:** Putri SN  

## Introduction  
In this assignment, we use data collected from accelerometers on the belt, forearm, arm, and dumbbell of six participants to build a machine learning model that predicts the manner in which they performed barbell lifts. The target variable is `classe`.

Please reference the links below for the data sources:

https://d396qusza40orc.cloudfront.net/predmachlearn/pml-training.csv

https://d396qusza40orc.cloudfront.net/predmachlearn/pml-testing.csv

## Load Required Packages  
We use the following R packages:
- `caret` for data splitting, cross-validation, and modeling
- `randomForest` for the Random Forest model
- `rpart`, `ggplot2`, and `dplyr` for data manipulation and visualization

## Load and Clean Data  
The training and test datasets are loaded from Coursera links. We remove variables with near-zero variance and columns that contain mostly NA values. Additionally, we remove non-relevant ID columns.

## Data Partitioning  
We split the training set into 70% training and 30% validation using `createDataPartition`.

## Model Building: Random Forest  
We train a Random Forest model using 5-fold cross-validation to predict the target variable `classe`.

## Prediction and Accuracy  
We predict the `classe` variable on the validation set and evaluate the accuracy using a confusion matrix.

## Out-of-Sample Error  
The out-of-sample error is calculated as `1 - Accuracy`.

## Final Prediction  
We apply the model to the 20-case test set provided by Coursera to generate final predictions.

## Conclusion  
A Random Forest model was successfully built and validated. The model shows high accuracy with a low out-of-sample error, indicating strong performance on unseen data.
