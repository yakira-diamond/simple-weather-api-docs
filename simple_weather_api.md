
# Simple Weather API Documentation

Welcome to the Simple Weather API. This API provides current weather information for cities around the world.

## Base URL
```
https://api.simpleweather.com/v1
```

## Authentication
To access the API, you need an API key.

Include the API key in the `Authorization` header:
```
Authorization: Bearer YOUR_API_KEY
```

---

## Endpoints

### 1. Get Current Weather

**Endpoint:**
```
GET /weather/current
```

**Description:** Retrieves current weather data for a given city.

**Query Parameters:**

| Name      | Type   | Required | Description                      |
|-----------|--------|----------|----------------------------------|
| `city`    | string | Yes      | Name of the city                 |
| `units`   | string | No       | Temperature units (`metric`, `imperial`) |

**Example Request:**
```
GET /weather/current?city=London&units=metric
```

**Example Response:**
```json
{
  "city": "London",
  "temperature": "16°C",
  "description": "Partly cloudy",
  "humidity": "72%",
  "wind_speed": "5 km/h"
}
```

---

### 2. Get Weather by Coordinates

**Endpoint:**
```
GET /weather/coordinates
```

**Description:** Retrieves weather data based on geographic coordinates.

**Query Parameters:**

| Name      | Type   | Required | Description                  |
|-----------|--------|----------|------------------------------|
| `lat`     | float  | Yes      | Latitude                     |
| `lon`     | float  | Yes      | Longitude                    |
| `units`   | string | No       | Units (`metric`, `imperial`) |

**Example Request:**
```
GET /weather/coordinates?lat=51.5074&lon=0.1278&units=imperial
```

**Example Response:**
```json
{
  "location": {
    "lat": 51.5074,
    "lon": 0.1278
  },
  "temperature": "61°F",
  "description": "Sunny",
  "humidity": "60%",
  "wind_speed": "10 mph"
}
```

---

## Error Responses

| Code | Message           | Description                    |
|------|-------------------|--------------------------------|
| 400  | Bad Request       | Missing or invalid parameters  |
| 401  | Unauthorized      | Missing or invalid API key     |
| 404  | Not Found         | City or coordinates not found  |
| 500  | Internal Error    | Server encountered an error    |

## Contact
For support, contact: `support@simpleweather.com`
