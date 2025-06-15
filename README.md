# 🔥 Wildfire Risk Mapping in Alberta (2025)

This project explores how GIS and spatial analysis can be used to model and map wildfire susceptibility across Alberta using terrain, vegetation, and historical fire data.

🗓️ **Date**: June 14, 2025  
👩‍💻 **Author**: Michelle Alzola  


---

## 📌 Project Overview

The goal of this project is to identify areas in Alberta that are most at risk of wildfires. By combining ecological, terrain, and historical datasets within a GIS framework, I created a weighted overlay model that classifies land into four wildfire risk categories.

---

## 🧭 Data Sources

- **Primary Land and Vegetation Inventory (PLVI)** – Alberta Open Data
- **Digital Elevation Model (25m DEM)** – Altalis
- **Wildfire Perimeters (1931–2024)** – Alberta Wildfire Open Data
- **Municipal Boundaries** – AltaLIS

---

## 🛠️ Methodology Summary

1. **Vegetation Risk Classification** – Custom Python function `classify_fire_risk()` using species, conifer density, and time since last disturbance.
2. **Terrain Analysis** – Slope and aspect derived from 25m DEM; south-facing slopes identified using aspect.
3. **Proximity to Fires** – Buffered wildfire perimeters from 2000–2024 by 2 km to model ignition risk.
4. **Weighted Overlay** – Combined raster layers with the following weights:
   - Vegetation: 30%
   - Slope: 30%
   - South Aspect: 20%
   - Fire Proximity: 20%
5. **Municipality Intersection** – Identified rural districts that overlap with the highest wildfire risk zones.

---

## 📊 Key Results

- **Most Affected Regions**:
  - Regional Municipality of Wood Buffalo
  - Big Lakes County
  - Northern Sunrise County

- **Risk Classification**:
  - Class 1 (Highest Risk): Over 5.8 million pixels
  - Class 4 (Lowest Risk): Fewer than 3,000 pixels

---

## 🧪 Tools Used

- ArcGIS Pro (Raster tools, Spatial Join, Polygon to Raster, Feature to Point)
- Python (Field Calculator, `classify_fire_risk()` function)
- Jupyter Notebook (Validation of classification logic)

---

## 🧭 Next Steps (as recommended in the report)

- Integrate real-time fire monitoring (MODIS/VIIRS)
- Expand analysis to Boreal regions using Alberta Vegetation Inventory (AVI)
- Add anthropogenic risk layers (infrastructure proximity)
- Package into a reusable workflow/toolbox

---

## 📎 License

This repository is for educational and portfolio use. All third-party datasets used are credited to the Government of Alberta and associated public data sources.

---

## 🔗 Report

[📄 Click here to view the full PDF](Wildfire_Risk_Mapping_Report.pdf)
