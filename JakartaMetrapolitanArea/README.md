# JakartaMetropolitanArea

This directory contains the implementation of the CO and NO₂ reconstruction framework for the Jakarta Metropolitan Area (Jabodetabek).

The files mainly represent the end-to-end model implementation pipeline, including:

- Data preprocessing
- Model training
- Reconstruction of missing pollutant observations
- Imputation of incomplete spatial-temporal pollutant grids

The experiments were conducted using both CO and NO₂ atmospheric datasets under multiple urban-event and seasonal scenarios.

---

# CO Experimental Scenarios

The CO reconstruction experiments primarily focus on fire-related urban emission events within the Jakarta Metropolitan Area.

## 1. North Jakarta Pertamina Depot Fire (3 March 2023)

This scenario represents the major fire incident at the Pertamina fuel depot in North Jakarta during the night of 3 March 2023.

The event was analyzed to evaluate pollutant reconstruction performance during a large-scale urban combustion event.

References:
- Kompas — Kronologi Kebakaran di Depo Pertamina Plumpang, Bau Bensin Menyengat Disusul Ledakan Hebat
  https://megapolitan.kompas.com/read/2023/03/04/07494471/kronologi-kebakaran-di-depo-pertamina-plumpang-bau-bensin-menyengat
  
---

## 2. Tambora Residential Fire (11 October 2024)

This scenario represents the large residential fire involving approximately 50 rental housing units in Tambora, West Jakarta, during the daytime of 11 October 2024.

This case was used to analyze localized urban fire emissions and their spatial-temporal reconstruction characteristics.

References:
- Kompas — Kontrakan 50 Pintu di Tambora Ludes Terbakar, Diduga akibat Korsleting  
  https://megapolitan.kompas.com/read/2024/10/11/15225751/kontrakan-50-pintu-di-tambora-ludes-terbakar-diduga-akibat-korsleting
  
---

# NO₂ Experimental Scenarios

The NO₂ reconstruction experiments primarily focus on large-scale mobility and traffic-related emission variations during the Eid al-Fitr holiday periods in 2023-2025.

---

# Notes

- CO and NO₂ implementations may use different spatial resolutions following their respective Sentinel-5P configurations.
- Wind variables are spatially aligned with the corresponding pollutant grids.
- Some implementations may represent exploratory or intermediate experimental configurations evaluated during the development of the final methodology presented in the paper.
