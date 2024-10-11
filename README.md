# 🌍 Land Cover Classification with Google Earth Engine (GEE) and geemap 🌍

This project uses **Google Earth Engine (GEE)** and **geemap** to perform land cover classification for the Mumbai region. The classification is done using **Landsat 8** satellite data, calculating **NDVI** and **MNDWI** indices, and applying a **Random Forest Classifier** to classify the land cover types. The project also utilizes the **ESRI Global Landcover** dataset for training the model.

## Features
- 🛰️ **Landsat 8 Data**: Satellite imagery is collected and processed from the **LANDSAT/LC08/C02/T1_L2** dataset.
- 🌱 **Vegetation & Water Index Calculations**: Calculate the **Normalized Difference Vegetation Index (NDVI)** and **Modified Normalized Difference Water Index (MNDWI)** to analyze land cover.
- 🎨 **Land Cover Classification**: Classify the land cover using a **Random Forest Classifier** trained on **ESRI Global Landcover** data.
- 🗺️ **Visualizations**: Display satellite imagery with custom visualizations using NIR, Red, and Green bands.
- 🌏 **Real-time Map Display**: Visualize classified land cover data in an interactive map centered on Mumbai.

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/landcover-classification.git
cd landcover-classification
```
### 2. Set up a virtual environment
```bash
python3 -m venv venv
source venv/bin/activate  # For Linux/MacOS
venv\Scripts\activate  # For Windows
```
### 3. Install dependencies
```bash
pip install -r requirements.txt
```
### 4. Authenticate Google Earth Engine
```bash
import ee
import geemap
ee.Authenticate()  # Authenticate your GEE account
ee.Initialize(project='your-project-id')  # Initialize GEE with your project ID
```

### Usage
    1. Define the Region of Interest (ROI): The project focuses on the geographical coordinates of Mumbai.
    2. Process Landsat Data: Apply scale factors and calculate indices like NDVI and MNDWI.
    3. Land Cover Classification: Classify the land cover using a Random Forest Classifier trained on the ESRI Global Landcover Dataset.
    4. Visualize Results: Display the classified land cover and ESRI data on an interactive map.
### Running the Script
Once the environment is set up, run the Python script to visualize and classify the land cover:
```bash
python main.py
```

### Land Cover Classes
The model classifies land into the following categories:

Water
Trees
Flooded Vegetation
Crops
Built Area
Bare Ground
Snow/Ice
Clouds
Rangeland
These classes are color-coded in the visualization.

### Dataset
Landsat 8: Data from the LANDSAT/LC08/C02/T1_L2 collection.
ESRI Global Landcover: The land cover training data comes from ESRI_Global-LULC_10m_TS.

### Visualizations
NDVI & MNDWI Calculation: The project calculates and visualizes the NDVI and MNDWI indices to help in distinguishing vegetation and water bodies.
Classified Land Cover: The results of the classification are shown on an interactive map using color palettes to represent different land cover types.

### Future Improvements
🌍 Expand the analysis to include more regions and higher-resolution datasets.
🧪 Implement more advanced classification techniques like deep learning models for better accuracy.
📈 Explore time-series analysis for land cover changes over multiple years.

### License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). See the LICENSE file for details.

### Images:

### ROI Selection
![ROI Selection](https://github.com/user-attachments/assets/ed1e239c-48f6-41e6-b905-1a269e5a3a54)


### RGB Visualization
![RGB Visualization](https://github.com/user-attachments/assets/68409579-a106-4fe3-a168-19814b715f96)

