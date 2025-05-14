# Coffee Production Predictor

This project analyzes weather trends in Brazil to understand how climate variability affects the yearly output of coffee. 

In this lab, two datasets were combined to investigate the relationship between weather metrics (rainfall, temperature, humidity, and wind speed) and crop output in Brazil. Exploratory data analysis were conducted on variables to predict optimal weather conditions for coffee harvesting.

## Installation Requirements

The following libraries should be installed: 

- Pandas
- Numpy
- Seaborn
- Matplotlib.pyplot

## Project Structure

data/
    crop/
        coffee_output.csv/ # Original dataset
    weather/
        weather_data.csv/ # Merged dataset
        weather_data1.csv/ # Original dataset
        weather_data2.csv/ # Original dataset
notebooks/
    analysis.ipynb
    explore_coffee.ipynb
    explore_weather.ipynb

## Data Dictionary

Descriptions for each column in the dataset is detailed below: 

**weather_data**
This csv dataset includes two csv data files of yearly weather outcomes for the coffee-growing months of Minas Gerais. Only weather data from January through May is considered.

* year: Year on which metrics were calculated. 
* rain_max: Average maximum millimeters of rain.
* temp_avg: Average temperature in celsius.
* temp_max: Average maximum temperature in celsius.
* temp_min: Average minimum temperature in celsius.
* hum_max: Average maximum humidity in percentage.
* hum_min: Average minimum humidity in percentage.
* wind_max: Average maximum wind speed in meters per second.
* wind_avg: Average wind speed in meters per second.
* subdivision: Name of Brazilian sub-division (all should be Minais Gerais)

**coffee_output** 
This csv dataset describes yearly features related to the coffee harvest that begins in June and ends in September in Minas Gerais.

* country: Country where harvest occurs (all should be Brazil).
* subdivision: Name of sub-division (all should be Minais Gerais)
* type: Type of coffee bean
* 60kgs_bag: 60 kg bags of coffee beans harvested (million bags)
* year: Year of harvest
* nonbearing_trees: Amount of nonbearing coffee trees (million trees)
* bearing_trees: Amount of bearing coffee trees (million trees)
* nonbear_hectares: Hectares of nonbearing coffee trees (thousand hectares)
* bearing_hectares_per_hectare: Average number of bearing trees per hectare
* nonbearing_trees_per_hectare: Average number of non-bearing trees per hectare

## Instructions

Three Jupyter notebooks are provided to perform exploratory data analysis: 

* notebooks/explore_weather.ipynb
* notebooks/explore_coffee.ipynb
* notebooks/analysis.ipynb

Open each Jupyter notebook and run the script in each cell to load, clean, analyze and generate outputs. At the end of each notebook a "write-up" section documents the results of the analysis conducted for each file.

## Analysis and Results

**explore_weather.ipynb**
Exploratory data analysis was performed on `weather_data1.csv` and `weather_data2.csv`' into a new csv called `weather_data.csv`. Univarate analysis showed temperature, minimum humidity and wind speed decreased over the years in Minas Gerais (MG). The highest recorded rainfall in MG was in 2006 with 6.67 inches.

**explore_coffee.ipynb**
Exploratory data analysis was conducted on the `coffee_output.csv` file for MG. Bearing trees and 60kgs bags of coffee showed an increase over the years, whereas bearing hectares showed a decrease in production. Bearing trees had a positive correlation with 60kgs bag count, however bearing hectares had a negative correlation.

**analysis.ipynb**
The `weather_data.csv` and `coffee_output.csv` files were merged on the `year` and `subdivision` columns to explore how weather patterns correlate with coffee harvest output. Bivariate analysis showed coffee production in MG was most influenced by wind speed average (R=0.92). To continue exploring the impacts of weather and coffee production, data collection on precipitation, atmospheric pressure, coffee prices, deforestation, coffee crop pests population (i.e. beetles, leaf rust) may be considered.

## Authors

- [@Alyssacobbs](https://www.github.com/Alyssacobbs)

