# WeatherPy and VacationPy
World weather analysis challenge - using APIs

This repository contains two connected Jupyter notebooks: the first, **WeatherPy**, selects a group of random coordinates and finds the cities closest to those coordinates. I used OpenWeatherMap API to gather the current weather in all of those cities (as long as there was data to gather, of course). The data from all cities was saved in a CSV file to be used later.

I also looked at the distributions of max temperature, humidity, cloudiness, and wind speed by latitude. (I shared my observations in the Jupyter notebook.)

The second Jupyter notebook, **VacationPy**, takes the CSV I created in WeatherPy and plots the cities on a map. Next, I pare down the dataframe by various weather constraints. I chose max temp between 18C and 24C,, cloudiness between 20% and 80% coverage, humidity between 45% and 85%, and wind speed below 10 knots.

These constraints resulted in a dataset of 18 cities. Next, I created a table with those cities and proceeded to search for the nearest hotel within 10km of each city using Geoapify. Five of the 18 cities did not return a hotel. Finally, I printed another map containing just the cities that met my criteria.

Given that I pulled my data in early March, my final list of cities all lie between 40N and 40S latitude. I filtered warmer temperatures, so most of the northern latitudes got filtered out. If I were to run this script again in June, I imagine I would get a vastly different list of cities, probably further from the Equator.

I received starter code to get this project going, but the rest of the code in this repository was written by me.