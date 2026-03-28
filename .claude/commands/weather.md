Fetch real-time and forecast weather data for a given location and present it in a military-formatted weather estimate.

## Instructions

The user will provide a location (city name, grid, or coordinates). If no location is provided, default to **Riga, Latvia** as the primary AO reference point for OPERATION BALTIC BASTION.

### Step 1 — Geocode the location

If a city name is provided (not raw coordinates), resolve it to latitude/longitude using the Open-Meteo geocoding API:

```
https://geocoding-api.open-meteo.com/v1/search?name={CITY_NAME}&count=1&language=en&format=json
```

Extract `latitude` and `longitude` from the first result.

### Step 2 — Fetch weather data

Call the Open-Meteo forecast API with the resolved coordinates:

```
https://api.open-meteo.com/v1/forecast?latitude={LAT}&longitude={LON}&current=temperature_2m,relative_humidity_2m,precipitation,wind_speed_10m,wind_direction_10m,cloud_cover,visibility,weather_code&hourly=temperature_2m,precipitation_probability,precipitation,wind_speed_10m,wind_direction_10m,visibility,cloud_cover&daily=temperature_2m_max,temperature_2m_min,precipitation_sum,precipitation_probability_max,wind_speed_10m_max,wind_direction_10m_dominant,sunrise,sunset&wind_speed_unit=kmh&temperature_unit=fahrenheit&precipitation_unit=inch&forecast_days=7&timezone=auto
```

### Step 3 — Format the output

Present the results as a military weather estimate with the following sections:

---

**WEATHER ESTIMATE — [LOCATION] — [DATE/TIME]**

**1. CURRENT CONDITIONS**
- Temp, wind (speed + direction in cardinal), cloud cover (%), visibility (km), precipitation

**2. TACTICAL WEATHER EFFECTS (Current)**
- Aviation: rotary-wing/UAV impact
- Ground mobility: on-road / off-road trafficability
- CBRN: downwind hazard assessment based on wind direction
- Observation / fields of fire: visibility impact on direct fire engagements

**3. 7-DAY FORECAST TABLE**
Columns: Date | High/Low (°F) | Precip (in) | Precip Probability | Max Wind (km/h + direction) | Tactical Impact

**4. CRITICAL WEATHER WINDOWS**
Flag any days with:
- Precipitation > 0.5 inches (significant trafficability degradation)
- Wind > 40 km/h (aviation degradation)
- Cloud cover > 80% (sustained) (aviation / UAV degradation)
- Sunrise / Sunset times (BMNT/EENT planning reference)

**5. S2 WEATHER ASSESSMENT**
Brief narrative on how forecast conditions affect enemy and friendly operations in the AO. Call out any windows that favor enemy offensive action (poor weather degrading NATO air superiority) or friendly defensive preparation.

---

### Notes
- Label all data as **FACT (Open-Meteo forecast)** in the S2 context.
- Use cardinal directions for wind (e.g., NE, SW) not degrees alone.
- If the location cannot be geocoded, state it plainly and ask the user to provide coordinates.
- For BALTIC BASTION scenario use, key reference cities are: Riga (Latvia), Jekabpils (Latvia), Panevezys (Lithuania), Daugavpils (Latvia), Birzai (Lithuania).
