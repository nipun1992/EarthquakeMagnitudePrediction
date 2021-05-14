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

As part of Data Processing to clean the data, the duplicate rows were removed, univariate and multivariate outliers were removed, the skewness in the data was handled using square root transformation, nominal categorical column **color** was one hot encoded

## Findings

#### Count vs Quality

The count plot reveals that there are more average quality wines in comparison to the low and high quality ones.

![Count Vs Quality](https://github.com/nipun1992/Predicting-Wine-Quality/blob/main/pics/count%20vs%20quality.png)

#### Pie Chart

The pie chart highlights the percentage wise distributions of the wines of respective quality levels.

![Pie Chart](https://github.com/nipun1992/Predicting-Wine-Quality/blob/main/pics/Pie%20Chart.png)

### Correlation with Heatmap

In the heatmap, if there are any 2 independent features that are highly correlated i.e. 80% or more, then we can drop 1 of those 2 features because both those features are serving the same purpose. We can see that density and 'residual sugar' features have a `pearson correlation coefficient of 0.83` i.e. *83% and thus we can drop 1 of these 2 features*. 

But in the dataset of red wines, these 2 features are not strongly correlated and thus we cannot drop any amongst these 2 features from the red wine dataset. 

![Heatmap](https://github.com/nipun1992/Predicting-Wine-Quality/blob/main/pics/heatmap.png)

## Model Building

Built a Logistic Regression model having an accuracy of 98.97%.

Built a Random Forest classifier model having an accuracy of 99.10%.

Built a Support Vector Machine model having an accuracy of 99.04%.
