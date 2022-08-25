# World_Weather_Analysis

This analysis was performed by interacting with two APIs: citipy and Google Maps.

First, a series of 2,000 latitudes and longitudes were randomly generated. Using these latitude and longitude pairs and the citipy module, the city closest to each of these pairs was identified. Using pandas, after calling the API repeatedly, the resulting cities and weather data regarding those cities were placed into a DataFrame. Try/except error handling was also used to account for those latitude/longitude pairs resulted in errors. Then, once a DataFrame was generated, this DataFrame was read into a .csv file entitled "WeatherPy_Database.csv". 

After generation of the original .csv file that included all cities looked up from the citipy API, the cities in the .csv were filtered for certain user inputs, simulating a customer stipulating the desired weather of their travel destination. This included a minimum and maximum temperature input. Using pandas, the DataFrame of cities was filtered for those cities with weather conditions that aligned with these inputs. After cleaning this resultant DataFrame to ensure it was free of null values, the Google Maps API was used to look up the nearest lodging to each of these cities. Again, using try/except error handling, cities for which a hotel was able to be looked up were included in a resultant DataFrame along with a new column for Hotel Name. This DataFrame of hotels was saved to a .csv file entitled "WeatherPy_vacation.csv".   

The hotels in the resultant DataFrame and .csv file were plotted on a world map using a marker layer along with a heat layer indicating temperature. This showed all hotels that were looked up from the Google Maps API. 
