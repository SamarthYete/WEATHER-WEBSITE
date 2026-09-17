# 🌤️ Interactive Weather Web Application

> A web application providing real-time weather forecasts, humidity, wind speeds, and temperature metrics.

![JavaScript](https://img.shields.io/badge/JavaScript-Fetch_API-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## ⭐ Star Schema (Weather Telemetry Analytics)

```
                            +-----------------------------------+
                            |           Dim_Location            |
                            +-----------------------------------+
                            | Location_Key (PK)                 |
                            | City_Name                         |
                            | Country_Code                      |
                            | Latitude                          |
                            | Longitude                         |
                            +-----------------+-----------------+
                                              | 1
                                              |
                                              | N
+-----------------------+   +-----------------+-----------------+   +-----------------------+
|  Dim_Calendar         | 1 |       Fact_WeatherReading         | 1 |  Dim_Condition        |
+-----------------------+---+-----------------------------------+---+-----------------------+
| DateKey (PK)          | N | Reading_Key (PK)                  | N | Condition_Key (PK)    |
| Date                  |   | DateKey (FK)                      |   | Weather_Main (Clear)  |
| Hour                  |   | Location_Key (FK)                 |   | Description           |
+-----------------------+   | Condition_Key (FK)                |   +-----------------------+
                            | Temp_Celsius (Measure)            |
                            | Humidity_Pct (Measure)            |
                            | Wind_Speed_Ms (Measure)           |
                            +-----------------------------------+
```
