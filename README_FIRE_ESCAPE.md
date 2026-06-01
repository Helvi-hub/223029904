# FIRE_ESCAPE — Wildfire Risk Visualization & Evacuation Analysis Tool
**Module:** GIS Programming  
**Author:** Helvi Kainekelwa Iita · 223029904  
**Institution:** Namibia University of Science and Technology  
**Study Area:** Namibia (focus: Etosha National Park & surrounding regions)

---

A Python-based interactive Web GIS application for wildfire risk classification, fire density analysis, and safe evacuation route identification across Namibia.

## ⬇️ Download
### [👉 Click here to download FIRE_ESCAPE (source code + datasets + HTML map)](https://drive.google.com/file/d/10q5rwr26A_hxWT_U1OM7b945wBCC5zoo/view?usp=sharing)

No GIS software required — download, unzip, and open `Wildfire_Map.html` in any browser. A ZIP export with all shapefiles and outputs is included.

---

**Risk Classes:** High · Medium · Low  
**Layers:** Fire Points · Vegetation · Rainfall · Temperature · Roads · Towns · Regional Boundaries  
**Data Sources:** MODIS/AFIS Fire Data · OpenStreetMap · Namibia Shapefiles

---

## Features

- Wildfire risk classification with colour-coded map layers (High / Medium / Low)
- Fire density heatmap generated with NumPy & Matplotlib — highlights concentration hotspots
- Buffer analysis (~15 km around fire points) to identify high-risk zones
- Safe road identification — erases road segments intersecting fire buffers
- Live analysis engine with progress tracking and summary statistics
- Geolocation tool (LocateControl) — shows user's position relative to fire risk
- Layer toggle control for all environmental layers
- Multiple basemap options: OpenStreetMap, Satellite, Terrain
- ZIP download with full HTML map, heatmap image, and all shapefiles

## Tech Stack

| Library | Purpose |
|---------|---------|
| GeoPandas | Spatial data loading and processing |
| Folium | Interactive web map generation |
| NumPy | Heatmap computation |
| Matplotlib | Fire density heatmap visualisation |
| Shapely | Buffer and geometric analysis |

## How It Works

1. Load all shapefiles (fire points, vegetation, rainfall, temperature, roads, towns, regions)
2. Standardise all layers to WGS84 (EPSG:4326)
3. Classify fire incidents into risk categories and style layers accordingly
4. Build interactive Folium map with all environmental layers and tooltips
5. Generate fire density heatmap and embed as interactive panel
6. Run buffer analysis — identify safe roads outside high-risk fire zones
7. Export complete interactive map as `Wildfire_Map.html`
