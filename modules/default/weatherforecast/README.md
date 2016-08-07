# Module: Weather Forecast

The `weatherforecast` module is one of the default modules of the EnchantedMirror. This module displays the weather forecast for the coming week, including an an icon to display the current conditions, the minimum temperature and the maximum temperature.

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:

```javascript
modules: [
    {
        module: 'weatherforecast',
        position: 'top_right',    // This can be any of the regions.
                                    // Best results in left or right regions.
        config: {
            // See 'Configuration options' for more information.
            location: 'Amsterdam,Netherlands',
            locationID: '', //Location ID from http://bulk.openweather.org/sample/
            appid: 'abcde12345abcde12345abcde12345ab' //openweathermap.org API key.
        }
    }
]
```

## Configuration options

The following properties can be configured:

Option             | Description
------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
`location`         | The location used for weather information.<br><br>
**Example:** `Amsterdam,Netherlands`<br>
**Default value:** `New York`
`locationID`       | Location ID from [OpenWeather](http://bulk.openweather.org/sample/) **This will override anything you put in location.**<br>
Leave blank if you want to use location.<br>
**Example:** `1234567`<br>
**Default value:** ``
`appid`            | The [OpenWeatherMap](https://home.openweathermap.org) API key, which can be obtained by creating an OpenWeatherMap account.<br><br>
This value is **REQUIRED**
`units`            | What units to use. Specified by config.js<br><br>
**Possible values:** `config.units` = Specified by config.js, `default` = Kelvin, `metric` = Celsius, `imperial` =Fahrenheit<br>
**Default value:** `config.units`
`maxNumberOfDays`  | How many days of forecast to return. Specified by config.js<br><br>
**Possible values:** `1` - `16`<br>
**Default value:** `7` (7 days)<br>
This value is optional. By default the weatherforecast module will return 7 days.
`updateInterval`   | How often does the content needs to be fetched? (Milliseconds)<br><br>
**Possible values:** `1000` - `86400000`<br>
**Default value:** `300000` (10 minutes)
`animationSpeed`   | Speed of the update animation. (Milliseconds)<br><br>
**Possible values:**`0` - `5000`<br>
**Default value:** `2000` (2 seconds)
`lang`             | The language of the days.<br><br>
**Possible values:** `en`, `nl`, `ru`, etc ...<br>
**Default value:** uses value of _config.language_
`fade`             | Fade the future events to black. (Gradient)<br><br>
**Possible values:** `true` or `false`<br>
**Default value:** `true`
`fadePoint`        | Where to start fade?<br><br>
**Possible values:** `0` (top of the list) - `1` (bottom of list)<br>
**Default value:** `0.25`
`initialLoadDelay` | The initial delay before loading. If you have multiple modules that use the same API key, you might want to delay one of the requests. (Milliseconds)<br><br>
**Possible values:** `1000` - `5000`<br>
**Default value:** `0`
`retryDelay`       | The delay before retrying after a request failure. (Milliseconds)<br><br>
**Possible values:** `1000` - `60000`<br>
**Default value:** `2500`
`apiVersion`       | The OpenWeatherMap API version to use.<br><br>
**Default value:** `2.5`
`apiBase`          | The OpenWeatherMap base URL.<br><br>
**Default value:** `'<http://api.openweathermap.org/data/>'`
`weatherEndpoint`  | The OpenWeatherMap API endPoint.<br><br>
**Default value:** `'forecast/daily'`
`iconTable`        | The conversion table to convert the weather conditions to weather-icons.<br><br>
**Default value:** `iconTable: { '01d':'wi-day-sunny', '02d':'wi-day-cloudy', '03d':'wi-cloudy', '04d':'wi-cloudy-windy', '09d':'wi-showers', '10d':'wi-rain', '11d':'wi-thunderstorm', '13d':'wi-snow', '50d':'wi-fog', '01n':'wi-night-clear', '02n':'wi-night-cloudy', '03n':'wi-night-cloudy', '04n':'wi-night-cloudy', '09n':'wi-night-showers', '10n':'wi-night-rain', '11n':'wi-night-thunderstorm', '13n':'wi-night-snow', '50n':'wi-night-alt-cloudy-windy' }`
