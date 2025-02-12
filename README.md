# Weather App
This is a simple weather application that fetches weather data using the OpenWeatherMap API.

## Features

- Fetches current weather data for a given city.
- Displays temperature, weather condition, and humidity.

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/weather-app.git


### index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weather App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        #weather {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Weather App</h1>
    <input type="text" id="city" placeholder="Enter city name">
    <button onclick="getWeather()">Get Weather</button>
    <div id="weather"></div>

    <script>
        function getWeather() {
            const city = document.getElementById('city').value;
            const apiKey = 'f0cdc9f0b5039240faf47f33f0df3fff';
            const url = `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}&units=metric`;

            fetch(url)
                .then(response => response.json())
                .then(data => {
                    const weatherDiv = document.getElementById('weather');
                    if (data.cod === 200) {
                        weatherDiv.innerHTML = `
                            <h2>${data.name}</h2>
                            <p>Temperature: ${data.main.temp}°C</p>
                            <p>Weather: ${data.weather[0].description}</p>
                            <p>Humidity: ${data.main.humidity}%</p>
                        `;
                    } else {
                        weatherDiv.innerHTML = `<p>City not found. Please try again.</p>`;
                    }
                })
                .catch(error => {
                    console.error('Error fetching weather data:', error);
                });
        }
    </script>
</body>
</html>
