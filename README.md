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

The code is stored as a jupyter notebook Wine **Earthquake Prediction.ipynb**. The data is present at **Earthquake.csv** file.

## Data Processing

As part of Data Processing to clean the data, the columns having high number of missing values and the unimportant column were dropped, the columns which had few missing values had the missing values replaced with mean/median, the features were weakly correlated to each on pearson correlation plot, there were no duplicate rows, univariate and multivariate outliers were removed, the skewness in the data was handled using square root transformation, date values were converted to datetime type, categorical variables were encoded.

## Findings


#### Correlation with Heatmap

In the heatmap, the features are weakly correlated to one another. The pearson correlation of all the featurs is between -0.31 to 0.25 

![Heatmap](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/heatmap.png)


#### Countplot, Pie chart and Catplot

From the plots, we can observe that most of the earthquakes are genuine earthquakes whereas very few earthquakes are due to explosions. 99.24% of the earthquakes are genuine earthquakes whereas 0.76% earthquakes are due to explosions. the magnitude of earthquake ranges from 2.35 to approx 2.70 for genuine earthquakes whereas the magnitude varies from 2.35 to 2.55 in the case of explosions

Magnitude Type glossary :

 MWC : centroid
 MWW : (Moment W-phase)(generic notation Mw)
 MB : short-period body wave
 MWB : body wave
 MS : 20 sec surface wave
 MWW : Moment W-phase)(generic notation Mw
 MWR : regional
 ML : local

![Variable_Type_Countplot_PieChart](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/Type_plot.png)

![Variable_Type_Catplot](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/Type_plot_catplot.png)

![Variable_MagnitudeType_Countplot_PieChart](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/MagnitudeType_plot.png)

![Variable_MagnitudeType_Catplot](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/MagnitudeType_catplot.png)

![Variable_MagnitudeSource_Countplot_PieChart](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/MagnitudeSource_plot.png)

![Variable_MagnitudeSource_Catplot](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/MagnitudeSource_catplot.png)

![Variable_LocationSource_Countplot_PieChart](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/LocationSource_plot.png)

![Variable_LocationSource_Catplot](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/LocationSource_catplot.png)

![Variable_Status_Countplot_PieChart](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/Status_plot.png)

![Variable_Status_Catplot](https://github.com/nipun1992/EarthquakeMagnitudePrediction/blob/main/pics/Status_catplot.png)

## Model Building

Built a Linear Regression model having **Mean absolute error :  0.25**, **Mean squared error :  0.107** and **Root mean squared error :  0.327**.

Built a Random Forest regressor model.
