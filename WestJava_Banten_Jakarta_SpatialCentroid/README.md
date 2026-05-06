# WestJava_Banten_Jakarta_SpatialCentroid

This directory contains the centroid-based spatial implementation of the pollutant reconstruction framework for the West Java, Banten, and Jakarta regions.

Unlike the spatial-grid implementation, this configuration uses representative centroid locations to approximate regional atmospheric behavior.

The implementation includes:
- Data preprocessing
- Model training
- Reconstruction of pollutant observations
  
The centroid-based approach was mainly developed as a comparative baseline against the full spatial-grid representation.

---

# Objective

This implementation was designed to evaluate whether centroid-based representations are sufficient for reconstructing atmospheric pollutant dynamics across large regional domains.

The experiments include:
- Diffusion PDE reconstruction
- Advection-Diffusion PDE reconstruction
- Inverse PDE coefficient estimation

for both CO and NO₂ datasets.

---

# Key Findings

The centroid-based spatial representation showed significant limitations in capturing localized spatial relationships within the atmospheric pollutant distributions.

Several experiments produced:

- Extremely small reconstructed spatial interaction magnitudes (approximately `~1e-5`)
- Unstable inverse PDE coefficient predictions
- Weak representation of localized transport dynamics
- Reduced sensitivity to spatial variability across regions

These issues were observed in both:
- Diffusion PDE models
- Advection-Diffusion PDE models

---

# Interpretation

The results suggest that centroid-only spatial representations are insufficient for modeling complex regional atmospheric transport behavior.

In particular, the centroid approach struggles to:
- Capture localized pollutant propagation
- Preserve fine-grained spatial dependencies
- Represent heterogeneous regional transport patterns
- Maintain stable inverse PDE parameter estimation

These findings support the use of spatial-grid representations and localized spatial modeling approaches for atmospheric pollutant reconstruction tasks.

---

# Notes

- This implementation mainly serves as a comparative and exploratory baseline.
- The centroid representation uses lower-resolution representative spatial points compared to the spatial-grid implementation.
- Wind variables for this configuration were obtained using representative-grid approaches from NASA POWER and API-based extraction pipelines.
- Some implementations may represent exploratory or intermediate experimental configurations evaluated during the development of the final methodology presented in the paper.
