# GeoAnomaly Detection

## Overview
This project applies geospatial data analysis and machine learning to detect geological anomalies using spectral reflectance properties. The workflow reconstructs spectral bands using Random Forest regression, computes residual error maps, performs PCA-based dimensionality reduction, and visualizes anomaly intensity in geospatial form.

## Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (Random Forest, PCA)
- SciPy
- GeoPandas / Shapely (optional for geospatial output)

## Project Tasks
### 1. Data Loading & Preprocessing
- Imported remote sensing data (spectral bands or geological features).
- Handled missing values and standardized numeric fields.

### 2. Spectral Band Reconstruction
- Trained a Random Forest model to reconstruct a selected band using remaining features.
- Model residuals used as anomaly indicators.

### 3. Residual Analysis
- Computed absolute residuals and normalized them.
- Created residual intensity maps to highlight anomalous locations.

### 4. PCA & Feature Reduction
- Performed PCA to compress feature space.
- Derived key principal components contributing to anomaly variability.

### 5. Anomaly Mapping
- Generated anomaly heatmaps and scatter plots.
- Identified spatial clusters of high residual error — potential geological anomalies.

### 6. Exporting Results
- Exported anomaly scores as:
  - CSV tables
  - Optional GeoJSON for GIS-based visualization

## Summary of Findings
- Identified multiple high-residual regions indicating unusual spectral signatures.
- PCA confirmed variance patterns consistent with localized anomalies.
- Random Forest residuals proved effective in highlighting non-linear spectral deviations.

## Challenges & Improvements
- Spectral noise sensitivity in lower-reflectance regions.
- Model selection trade-offs between interpretability and accuracy.
- Potential improvements:
  - Larger training dataset
  - Inclusion of elevation / soil composition layers
  - Use of gradient boosting or deep autoencoders

## Conclusion
GeoAnomaly Detection demonstrates how machine learning can enhance geoscientific exploration by uncovering subtle spectral anomalies. The reproducible workflow provides analytical transparency and generates interpretable outputs suitable for further geospatial investigation.
