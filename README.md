# OpenWeatherMapPY
# Weather Forecast Fetcher

A simple Python script that fetches 5-day weather forecasts from OpenWeatherMap and saves them to JSON files.

## Features

- Fetches 5-day weather forecasts (3-hour intervals)
- Tracks precipitation (rain and snow) accumulation
- Monitors maximum humidity levels
- Counts major weather transitions (weather changes + temperature variations >3°C)
- Exports data to formatted JSON files

## Requirements

- Python 3.6+
- requests library

## Installation

1. Clone or download this repository

2. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Run the script:
```bash
python weather_forecast.py
```

You'll be prompted to enter:
- Your OpenWeatherMap API key
- City name (e.g., Paris, London)
- Country code (2 letters, e.g., FR, US)

The script will generate a JSON file named `forecast_[city]_[country].json` with the weather data.

**Note:** The API key is requested each time for security purposes and is not stored anywhere.

## Output Format

The JSON output includes:
- Location name and country code
- Total precipitation for the forecast period
- Maximum humidity recorded
- Daily breakdown with:
  - Date
  - Rain accumulation
  - Snow accumulation
  - Major weather transition count

## Example

```
OpenWeatherMap API key: your_api_key_here
City: Paris
Country code (e.g., US, FR): FR

Fetching forecast for Paris, FR...

==================================================
  Summary
==================================================
Location: Paris, FR
Total rain: 12.3 mm
Total snow: 0.0 mm
Max humidity: 89%
Saved to: forecast_paris_fr.json
==================================================
```

## API Key

This script requires an OpenWeatherMap API key. You can get a free API key by signing up at https://openweathermap.org/api

For security, the API key is requested at runtime and is never stored in the code or configuration files.

## License

MIT
