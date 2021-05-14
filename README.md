# Earthquake Magnitude Prediction


- [Earthquake Magnitude Prediction](#Earthquake-Magnitude-Prediction)
  - [Introduction](#introduction)
  - [Directory structure](#directory-structure)
  - [Data Processing](#Data-Processing)
  - [Findings](#Findings)
      - [Count vs Quality](#count-vs-quality)
      - [Pie Chart](#pie-chart)
      - [Citric Acid Feature](#citric-acid-feature)
      - [Correlation with Heatmap](#correlation-with-heatmap)
  - [Model Building](#Model-Building)
  
## Introduction

Machine Learning project that determines the magnitude of an earthquake based on its various features including longitude, latitude, depth, earthquake type, magnitude type etc 

## Directory structure

The code is stored as a jupyter notebook Wine **quality Prediction-checkpoint.ipynb** inside **src** folder. To run the code, please open the file in jupyter and use run all command to run the code. The data is present at **src/data** location.

## Data Processing

As part of Data Processing to clean the data, the columns having high number of missing values and the unimportant column were dropped, the columns which had few missing values had the missing values replaced with mean/median, the features were weakly correlated to each on pearson correlation plot, there were no duplicate rows, univariate and multivariate outliers were removed, the skewness in the data was handled using square root transformation, date values were converted to datetime type, categorical variables were encoded.

## Findings

## Model Building

