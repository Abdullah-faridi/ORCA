
# Project Canary

### AQI Sentinel – Hyper-Local Air Quality Intelligence System

---

## 🌍 Overview

Air quality monitoring systems generally report pollution levels at the city scale, which hides significant variation across neighborhoods or wards. This limits the ability of authorities to detect localized pollution sources and implement targeted mitigation strategies.

AQI Sentinel is a hyper-local air quality intelligence platform designed to convert environmental data into actionable insights. The system integrates satellite observations, ground monitoring stations, meteorological data, and urban activity signals to forecast air pollution and identify probable emission sources.

Instead of only displaying AQI values, AQI Sentinel performs a complete forecast-to-action pipeline:

1-Collect environmental data from multiple sources
2-Forecast pollutant concentrations for the next 24 hours
3-Identify the most probable pollution sources
4-Generate mitigation recommendations for administrator
4-Provide health advisories for citizens

## 🚀 Key Highlights
Hyper-Local AQI Forecasting

The system predicts pollutant concentrations at fine spatial resolution, allowing early detection of localized pollution spikes.

>>Predicted pollutants include:
>PM2.5
>PM10
>NO₂
>O₃
Predictions are generated for the next 24 hours, enabling early warning systems for urban authorities.

## Multi-Source Environmental Data Fusion
AQI Sentinel integrates environmental signals from multiple domains:
>satellite atmospheric measurements
>ground monitoring stations
>meteorological datasets
>urban activity indicators

Combining these sources allows the model to capture both regional pollution transport and local emission events.

## Pollution Source Attribution
The system identifies the most probable pollution sources responsible for air quality deterioration.

>>Typical source categories include:
>traffic emissions
>construction dust
>biomass burning
>industrial activity
>regional pollutant transport
This allows authorities to implement targeted mitigation strategies instead of broad city-wide restrictions.

## Automated Policy Recommendations
AQI Sentinel translates pollution forecasts into actionable interventions, such as:
>traffic diversion during NO₂ spikes
>dust suppression near construction zones
>alerts during biomass burning events
These recommendations assist urban administrators in implementing data-driven environmental policies.

## Citizen Health Advisory System

The platform also provides public health guidance based on predicted pollution levels.
>>Citizens receive alerts including:
>air quality status in their ward
>pollution forecasts
>recommended protective measures
This helps reduce exposure during severe pollution episodes.

## Data Source
AQI Sentinel integrates several environmental datasets to produce reliable predictions.
*Satellite Observations*
>Satellite data provides large-scale atmospheric monitoring.
>>Sources include:
>Sentinel-5P atmospheric monitoring dat
>MODIS aerosol optical depth measurements
These datasets capture regional pollution plumes and atmospheric composition.

## Ground Monitoring Stations
Ground sensors provide accurate measurements of local air quality.
*Measured pollutants include:*
>PM2.5
>PM10
>NO₂
>O₃
>SO₂
>CO
These readings are used for model calibration and validation.

## Meteorological Data
Weather conditions strongly influence pollutant dispersion.
*Key meteorological features:*
>wind speed
>wind direction
>temperature
>humidity
>atmospheric boundary layer height

These variables help model pollution transport and accumulation.

## Data Pipeline
*Data Ingestion*
Environmental data is collected from satellite platforms, monitoring stations, and weather datasets.

*Preprocessing*
Missing values are handled using KNN imputation, and datasets are temporally aligned.

*Spatial Mapping*
Data is mapped to a city grid representation for spatial modeling.

*Feature Engineering*
Additional features such as wind transport indicators and temporal cycles are generated.

## Model Architecture
AQI Sentinel uses a hybrid deep learning architecture combining spatial and temporal modeling.
*CNN (Spatial Encoder)*
Extracts spatial pollution patterns from satellite grid data.
*MLP (Tabular Encoder)*
Processes meteorological variables and ground sensor measurements.
*Feature Fusion*
Spatial and tabular embeddings are combined into a unified representation.
*BiLSTM (Temporal Model)*
Captures time-dependent pollution trends.
*Attention Layer*
Highlights the most influential historical data points for prediction.
*Outputs*
24-hour pollution forecas
probable pollution source classification


## Tech Stack
*Programming & Data Processing*
Python
Pandas
NumPy
GeoPandas
Scikit-learn
*Machine Learning*
PyTorch
CNN + BiLSTM + Attention architecture
*Backend*
FastAPI / Flask
Celery
Redis
*Database*
Django
Django REST Framework
*Frontend & Visualization*
React js
D3.js

## Model Performance
| Metric                    | Value      |
| ------------------------- | ---------- |
| PM2.5 MAE                 | < 12 µg/m³ |
| NO₂ MAE                   | < 10 µg/m³ |
| Source Detection Accuracy | ~80%       |
