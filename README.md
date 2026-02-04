# Heat Wave Analysis over Australia Using ERA5 Daily Data
## Overview
Heat waves are among the most impactful climate extremes, affecting human health, ecosystems, agriculture, and infrastructure. Understanding their spatial and temporal patterns is essential for climate risk assessment and long-term adaptation planning, particularly in regions such as Australia that are highly vulnerable to extreme heat.

This project demonstrates a heat wave index analysis over Australia and surrounding regions using ERA5 daily maximum air temperature data and the xclim climate indicators framework. By integrating Google Earth Engine (GEE) with Python-based climate analytics, the workflow enables scalable heat wave detection, mapping, and time-series analysis over a user-defined region of interest (ROI).

The analysis focuses on:
1. Computing annual heat wave metrics from daily maximum temperature
2. Visualizing spatial patterns of heat wave intensity
3. Extracting point-based heat wave trends for local-scale interpretation

## Study Area
- Region: Australia and surrounding areas
- ROI: Custom-drawn region using geemap interactive tools

## Dataset
1. ERA5 Daily Reanalysis
- Source: ECMWF ERA5 Daily Dataset
- Collection: ECMWF/ERA5/DAILY (via Google Earth Engine)
- Variable Used:maximum_2m_air_temperature (converted from Kelvin to °C)
- Temporal Coverage: 2010–2020
- Spatial Resolution: ~0.3° (reanalysis grid)
ERA5 provides physically consistent, globally complete temperature records suitable for climate extremes analysis.

### Figure 1. Annual Heat Wave Index over Australia (2010–2020)
Spatial distribution of annual heat wave days derived from ERA5 daily maximum air temperature using the xclim heat wave index (threshold: 25 °C; minimum duration: 5 consecutive days). Warmer colors indicate higher heat wave frequency, highlighting regional variability in extreme heat exposure across Australia and surrounding areas.
<img width="1501" height="590" alt="image" src="https://github.com/user-attachments/assets/410af49d-64fc-447f-a97b-55dadfbdaeb7" />

### Figure 2. Heat Wave Days Time Series at a Selected Location (2010–2020)
Annual number of heat wave days extracted at a representative point within the study area. The time series illustrates interannual variability in heat wave occurrence, supporting localized assessment of extreme temperature trends.
<img width="712" height="215" alt="image" src="https://github.com/user-attachments/assets/c05f62b0-01a3-4f3f-85f1-775a643b91fc" />


## Tools & Libraries
1. Google Earth Engine (GEE) – Climate data access
2. geemap – Interactive mapping and ROI selection
3. xee – GEE–xarray bridge
4. xarray – Multi-dimensional climate data handling
5. xclim – Climate indices and extremes computation
6. matplotlib – Visualization
7. Python – Core analysis environment

## Notes & Limitations
- ERA5 is a reanalysis product and may smooth local extremes, particularly in complex terrain or coastal zones.
- Heat wave identification is sensitive to the selected temperature threshold and duration criteria.
- No station-based observations were used for validation.
- Results should be interpreted as climate-scale indicators, not site-specific extremes.

## Future improvements could include:
- Bias correction using station data
- Sensitivity testing with multiple thresholds
- Seasonal or regional heat wave classification
