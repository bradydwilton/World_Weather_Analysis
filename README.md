# Module 6: World Weather Visualization

### Description
This repository contains the files associated with the WeatherPy and VacationPy projects. These projects use Python and the requests module to pull and map world weather data based on a given set of inputs from a user (in this case, minimum and maximum desired temperatures for an upcoming vacation). Google's Maps and Places API's were then used to create maps to show the user cities falling within the given temperature range, and to create an itinerary of four destination cities.

### City List
* NumPy's random.uniform() function `np.random.uniform(min,max,2000)`) was used to create 2000 sets of latitude / longitude points.
* The random coordinates were then used with the [CitiPy](https://github.com/wingchen/citipy) module to create a list of the cities nearest to each random coordinate (`citipy.nearest_city(lat,long).city_name()`)

### WeatherPy
* Weather data was pulled from [OpenWeatherMap](https://openweathermap.org/)'s API. The requests module was used to pull the following data from each city:
    * Latitude & longitude
    * Country code
    * Maximum temperature
    * Humidity
    * Cloud level
    * Wind speed
    * Current weather description

### VacationPy
* The [Google Maps and Places API](https://developers.google.com/maps) took the location data of each city (provided by OpenWeatherMap's API), found a hotel within each city, and marked the cities on a map.
* Finally, four cities (selected by the user) were then mapped using the _directions_ API from Google and provided an itinerary of the four destination cities.
