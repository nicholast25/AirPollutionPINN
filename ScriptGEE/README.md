# ScriptGEE

This directory contains the Google Earth Engine (GEE) scripts used for extracting atmospheric pollutant and meteorological variables for the reconstruction experiments.

The scripts were designed to support large-scale spatiotemporal extraction across multiple regions, pollutants, and event scenarios between 2023–2025.

---

# Purpose of Using Google Earth Engine (GEE)

We primarily use Google Earth Engine because of its ability to efficiently process large spatial and temporal datasets with significantly higher computational capability compared to relying solely on APIs.

The extraction process involves:

- Large numbers of spatial grids
- Multi-year temporal observations
- Multiple atmospheric variables
- Different spatial resolutions for pollutants and meteorological variables

Using APIs alone may result in memory limitations, request overload, or computational bottlenecks during large-scale extraction. GEE enables scalable and efficient preprocessing for these experiments.

---

# Grid Resolution Configuration

The CO and NO₂ datasets use different spatial grid configurations following their respective Sentinel-5P Level-2 (L2) resolutions.

As a result:

- CO scripts and NO₂ scripts are generated using different grid structures
- Wind variables are adjusted to match the corresponding pollutant grids
- Each pollutant therefore has its own aligned meteorological configuration

This ensures spatial consistency between pollutant concentration data and meteorological variables.

---

# File Description

## Pollutant Files

Files containing `Pollutant` in their names store pollutant concentration values extracted from Sentinel-5P datasets.

Examples:

- `CO_Bangkok_Pollutant.txt`
- `NO2_JakartaMetropolitan_Pollutant.txt`

These files contain:

- CO concentration values
- NO₂ concentration values
- Spatial coordinates
- Temporal observations

under their respective pollutant grid resolutions.

---

## Wind Files

Files containing `Wind` in their names store meteorological variables aligned with the pollutant grids.

Examples:

- `CO_Bangkok_Wind.txt`
- `NO2_JakartaMetropolitan_Wind.txt`

These files contain:

- Horizontal wind speed components
- Vertical wind speed components

adjusted according to the corresponding CO or NO₂ spatial grids.

---

# Spatial Configurations

## `WestJava_Banten_Jakarta_SpatialGrid`

Uses spatial grid representations aligned with Sentinel-5P pollutant resolutions.

Both pollutant concentration and wind variables are extracted according to the spatial grid configuration.

---

## `WestJava_Banten_Jakarta_SpatialCentroid`

Uses representative centroid-based spatial configurations for each city/regency.

For this configuration:

- Wind variables are obtained from NASA POWER
- The spatial representation uses a lower-resolution representative grid
- Additional data retrieval is performed through API-based extraction

This configuration was mainly developed for computationally lighter centroid-level experiments and comparative analysis.

---

# Notes

- CO and NO₂ experiments should not be assumed to use identical spatial resolutions.
- Wind variables are always adjusted to match the pollutant grid configuration.
- Some scripts may represent intermediate experimental configurations used during the development stage of the research.
