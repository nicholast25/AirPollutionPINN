# WestJava_Banten_Jakarta_SpatialGrid

This directory contains the spatial-grid implementation of the CO and NO₂ reconstruction framework for the West Java, Banten, and Jakarta.

The implementation uses spatial-grid representations aligned with Sentinel-5P pollutant resolutions and focuses on large-scale regional atmospheric reconstruction experiments.

The files mainly represent the end-to-end model implementation pipeline, including:

- Data preprocessing
- Model training
- Reconstruction of missing pollutant observations
- Imputation of incomplete spatial-temporal pollutant grids

Both CO and NO₂ datasets are implemented under regional-scale mobility and emission-related scenarios.

---

# Experimental Scenarios

The primary scenarios explored in this directory correspond to the Eid al-Fitr holiday periods from 2024–2025. These periods were selected because they represent significant regional-scale mobility changes, transportation activity variations, and emission pattern shifts across the West Java, Banten, and Jakarta regions.

---

# Spatial Configuration

This implementation uses spatial-grid representations rather than centroid-based representations.

The spatial grids are aligned with the corresponding Sentinel-5P pollutant resolutions for both CO and NO₂ datasets.

Wind variables are spatially adjusted to match the pollutant grid configuration.

---

# Notes

- CO and NO₂ implementations may use different spatial resolutions following their respective Sentinel-5P configurations.
- Wind variables are spatially aligned with the corresponding pollutant grids.
- Some implementations may represent exploratory or intermediate experimental configurations evaluated during the development of the final methodology presented in the paper.
