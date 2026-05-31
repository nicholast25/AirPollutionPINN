# BangkokCity

This directory contains the implementation of the CO and NO₂ reconstruction framework for the Bangkok City.

The files mainly represent the model implementation pipeline, including:

- Data preprocessing
- Model training
- Reconstruction of missing pollutant observations
- Imputation of incomplete spatial-temporal pollutant grids

The experiments were developed using both CO and NO₂ atmospheric datasets under multiple urban-event scenarios.

---

# Experimental Scenarios

Several event-based cases were explored in this implementation, including major fire-related incidents in Bangkok and surrounding metropolitan regions.

## 1. Pathum Thani School Bus Fire (1 October 2024)

This scenario represents the school bus fire incident that occurred along Vibhavadi Rangsit Road in Pathum Thani, located in the northern outskirts of Bangkok.

The event was analyzed to observe potential atmospheric pollutant behavior and reconstruction performance during a sudden high-emission urban fire event.

Reference:

- [The Guardian — School Bus Fire Incident](https://www.theguardian.com/world/2024/oct/01/many-feared-dead-after-fire-on-school-bus)

---

## 2. Bang Sue Wood Processing Factory Fire (18 January 2024)

This scenario represents the fire incident at a wood-processing factory in the Bang Sue district of Bangkok on the morning of 18 January 2024.

The event provides a representative industrial fire case for evaluating pollutant reconstruction and imputation under localized combustion-related emissions.

Reference:

- [Bangkok Post — Wood Processing Factory Fire](https://www.bangkokpost.com/thailand/general/2942362/fire-engulfs-bangkok-wood-processing-factory)

---

# Notes

- CO and NO₂ implementations may use different spatial resolutions following their respective Sentinel-5P configurations.
- Wind variables are spatially aligned with the corresponding pollutant grids.
- Some implementations may represent exploratory or intermediate experimental configurations evaluated during the development of the final methodology presented in the paper.
