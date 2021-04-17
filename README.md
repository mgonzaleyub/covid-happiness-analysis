# COVID19 Data Analysis Using Python
This project is based in the COVID19 dataset, published by John Hopkins University, which consists of the data related to the cumulative number of confirmed cases, per day, in each Country.
Also, we have another dataset consisting of various life factors, scored by the people living in each country around the globe.

This project was done through Coursera Project Network [here](https://www.coursera.org/projects/covid19-data-analysis-using-python)

# Objective from Part 1: COVID infection rate function
The objective is compare both models to inference if there is any relationship between COVID infections and happiness state of mind from population.

## Preprocessing
Preprocessing includes removing useless columns, such as latitude and longitude: they only describe where are the cities.
Additionally, I can group by region and country because they are clearly related.

## Visualization
I put an example comparing China and Spain. It's clearly visible that China keeps an infection rate more stable than Spain, which tends to raise exponentially.

It's interesting to plot the first derivative of the curve, for instance, in China, to see some maximum and minimum points through time.
As we already know, the first derivative of a function give us the slope of the function for all its points.
This can be easily done with diff() function implemented in DataFrame.

## Processing
If we propagate this first derivative to all contries in the dataset, we can get the maximum infection rate for all of them.
We can store this values as a new column in a new dataset, where rows are the countries and the only column is this maximum infection rate obtained before.

# Objective for Part 2: World Happiness
Now, we are using a new dataset which includes several featuers:;
- Overall rank
- Country or region
- Score	GDP per capita
- Social support
- Healthy life expectancy	
- Freedom to make life choices
- Generosity	
- Perceptions of corruption

## Preprocessing
The features "Overall rank", "Score", "Generosity", "Perceptions of corruption" can be dropped, and Country or region can be set as index,
so every row will refer to a country.
Then, we can join both datasets, and draw a correlation matrix to analyze this combination.

## Visualization
I provide some interesting plots to see if exists a linear correlation:
- GDP vs maximum Infection rate
- Social support vs maximum Infection rate¶
- Healthy life expectancy vs maximum Infection rate
- Freedom to make life choices vs maximum Infection rate

# Certificate
![alt text](https://github.com/mgonzaleyub/covid-happiness-analysis/blob/master/certificate.png "Completion certificate")
