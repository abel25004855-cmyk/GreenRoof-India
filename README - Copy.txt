GREENROOF INDIA — ADVANCED WEBSITE QUICK START

FILES
- index.html: complete single-page dashboard
- README.txt: setup, data sources, and limitations
- DEMO_GUIDE.txt: suggested presentation flow and viva answers

RUN
1. Extract the ZIP to a folder.
2. Open index.html in Chrome or Edge.
3. Keep internet access enabled. Weather, forecast, map tiles, Leaflet, and Chart.js load from external services.
4. Click “Refresh data” to retrieve current readings for 15 representative Indian cities.
5. Use the top navigation to open “7-day temperature” and select a city to view forecast highs/lows.
6. Use the top navigation to open “Compare cities” and compare current temperature, humidity, precipitation, feels-like temperature, and the prototype score.

FEATURES
- Current temperature, relative humidity, current precipitation, apparent temperature, and daily precipitation total via Open-Meteo. These values are refreshed together when the dashboard loads or Refresh is clicked.
- Interactive city-marker map using Esri World Street Map tiles.
- Current temperature bar chart, ranking, and searchable city table.
- Seven-day forecast chart for daily maximum/minimum temperature; the API also supplies daily precipitation totals.
- Side-by-side comparison of two selected cities using the latest loaded readings.
- Top navigation separates Home dashboard, 7-day temperature, and Compare cities into distinct views.
- Refreshable data and responsive layout.

DATA AND LIMITATIONS
- Open-Meteo API: https://open-meteo.com/en/docs
- Leaflet: https://leafletjs.com/
- Chart.js: https://www.chartjs.org/
- Basemap: Esri World Street Map; requires internet and is subject to Esri terms/service availability.
- The 15 points are representative city locations, not state-wide averages.
- Current weather and short-term forecasts are not long-term climate records.
- The priority score is an educational heuristic: 60% heat score + 40% manually assigned urban proxy, minus a small current-precipitation adjustment. It is not a validated scientific or engineering rating.
- The urban proxy values are predefined in the source code and are not dynamically measured urban-density data.
- Forecast values are model outputs and can change. They should not be treated as guaranteed weather.
- No API key or backend is included. External service availability and internet access are required.

Humidity refresh update (latest version):
- The current-weather request explicitly fetches relative_humidity_2m alongside temperature and uses a no-cache browser request with a refresh timestamp.
- Humidity is displayed to one decimal place in the dashboard, city table, map popups, and city comparison.
- The main city table shows the daily precipitation total as “Rain today (mm)”, while map popups and the comparison section show both current precipitation and the daily total. These are different measures. The current precipitation field is used for the prototype score adjustment.
