# 🌍 Introduction to GIS (Geographic Information Systems)

## 🎯 Objective
Understand the fundamentals of GIS and learn how to work with spatial data through practical examples.

---

# 🧠 What is GIS?

A Geographic Information System (GIS) is a system designed to capture, store, analyze, manage, and visualize geographic (spatial) data.

👉 In simple terms:
GIS allows us to **understand the world through location**.

---

# 🗺️ Why is GIS Important?

GIS helps answer questions like:
- Where is something located?
- What is nearby?
- What has changed over time?
- What is the best location for a project?

---

# ⚙️ Components of GIS

1. **Data**
   - Spatial data (location)
   - Attribute data (information)

2. **Software**
   - ArcGIS
   - QGIS

3. **Hardware**
   - Computers, servers

4. **People**
   - Analysts, planners, decision-makers

---

# 📊 Types of Spatial Data

## 🔹 1. Vector Data

Represents discrete features.

| Type   | Example        |
|--------|---------------|
| Point  | Cities        |
| Line   | Roads         |
| Polygon| Parcels       |

---

## 🔹 2. Raster Data

Represents continuous data.

Examples:
- Satellite imagery
- Elevation (DEM)
- Temperature maps

---

# 🧪 DEMO 1 – Visualizing Vector Data (QGIS / ArcGIS)

## 🎯 Goal
Display a shapefile and explore its attributes.

## 🪜 Steps

1. Open QGIS or ArcGIS
2. Add a shapefile (e.g., administrative boundaries)
3. Right-click → Open Attribute Table
4. Identify fields (name, population, etc.)
5. Change symbology (colors)

## ✅ Expected Result
- Map displayed
- Data visible in table
- Styled layer

---

# 🧪 DEMO 2 – Adding Raster Data (Satellite Image)

## 🎯 Goal
Visualize satellite imagery

## 🪜 Steps

1. Download Sentinel-2 image (or use sample)
2. Add raster layer in GIS software
3. Adjust brightness/contrast
4. Zoom and explore

## ✅ Expected Result
- Satellite image displayed
- Ability to identify land features

---

# 🧪 DEMO 3 – Simple Spatial Analysis

## 🎯 Goal
Find features within a specific area

## 🪜 Steps

1. Load:
   - Cities layer
   - Regions layer
2. Use tool:
   👉 “Select by Location”
3. Select cities inside a region

## ✅ Expected Result
- Selected cities highlighted
- Filtered data

---

# 🧪 DEMO 4 – Python (GeoPandas Example)

## 🎯 Goal
Read and visualize spatial data using Python

## 🧑‍💻 Code

```python
import geopandas as gpd
import matplotlib.pyplot as plt

# Load dataset
gdf = gpd.read_file("data/shapefile.shp")

# Display first rows
print(gdf.head())

# Plot map
gdf.plot()
plt.title("GIS Map Example")
plt.show()
