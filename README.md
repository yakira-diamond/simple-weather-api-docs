#  Simple Weather API Docs

This project contains detailed documentation for a Simple Weather API that allows developers to fetch real-time weather information based on city or location input. It is designed to help developers understand how to use the API effectively, including endpoint structure, request parameters, and expected responses.

##  Overview

The Simple Weather API provides the following data:
- Current weather conditions
- Temperature (in Celsius and Fahrenheit)
- Humidity
- Wind speed
- Weather descriptions (e.g., Cloudy, Sunny, Rainy)

##  API Endpoints

###  GET `/api/weather?city={city_name}`

**Description:** Fetches current weather data for a given city.

**Example Request:**
```bash
GET /api/weather?city=Lagos

{
  "city": "Lagos",
  "temperature_celsius": 30,
  "temperature_fahrenheit": 86,
  "humidity": 70,
  "description": "Sunny",
  "wind_speed": 12
}
```

## Tech Stack
- Markdown for documentation
- Swagger/OpenAPI format (if applicable)
- Deployed using GitHub Pages or local preview tools

- 
