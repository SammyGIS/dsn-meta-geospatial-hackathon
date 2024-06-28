# Zamfara State Health Care Facilities Accessibility and Assessment
This project aims to assess and improve health care facilities' accessibility in Zamfara State, Nigeria, using both spatial and non-spatial data. The analysis involves determining population coverage within a 500m radius of existing facilities, identifying suitable areas for new health facilities, and pinpointing areas with low access to health care.

## Project Aims
1. Determine the population within a 500m radius of existing health care facilities.
2. Identify the most suitable areas to site new health facilities.
3. Identify areas with low access to health facilities.
4. Determine the optimal locations for new health facilities based on population needs.

## Methodology

### Data Analysis and Visualization
1. **Count of Health Care Facilities:** Determine the total number of health care facilities in different wards across the state.
2. **Categories of Health Facilities:** Count the categories of health facilities.
3. **Population Analysis:** Use raster data to estimate the population within Zamfara State and analyze population distribution within 500m of health facilities.
4. **Mobility Data Analysis:** Use Facebook mobility data to analyze human movement patterns within the state.

### Geospatial Analysis
1. **Facebook Mobility Data:** Use Facebook movement data to understand human mobility within the state.
2. **Validation:** Validate the health facility data and eliminate points that do not exist.
3. **Buffer Creation:** Create a 500m buffer around health facilities to determine how many people within the buffered area have access to the health facilities.
4. **Constraints Identification:** Identify constraints such as distance to waterways, water bodies, and existing health facilities. Merge these constraints into a single vector file.
5. **Factors Identification:** Identify important factors such as distance to road networks and residential areas. Residential areas within 100m of a road network are considered suitable for siting a health facility.
6. **Low Access Areas:** Identify areas with low access to health facilities by erasing residential polygons with the constraint vector. Use the remaining polygons to determine the population with low access to health care.
7. **Overlay Analysis:** Use the overlay function in geopandas to erase the factors polygon using the merged constraint layer. The remaining areas are suitable for siting new health facilities.
8. **Optimal Location:** Population is a critical factor, as health centers are built for people. Determine the optimal location based on population needs.
9. **Suitability Analysis:** Perform suitability analysis to identify optimal locations for new health facilities based on population need.

## Results
1. **Health Facilities Population Coverage:** Determine the population within 500m of each health facility.
2. **Suitable Areas:** Identify suitable areas for new health facilities.
3. **Low Access Areas:** Identify areas with low access to health facilities and determine the population in these areas.
4. **Optimal Locations:** Determine optimal locations for new health facilities based on population needs.
5. **Geosptial Web App:** Use ArcGIS Online Web App Builder to create a geospatial web map that visualizes the results.

## Workflow
![work flow](workflow.png)


## Web APP Link
![WEB MAP](https://africageoportal.maps.arcgis.com/apps/webappviewer/index.html?id=129ec4eac15c42e9878df1361ff55d25)

## Conclusion
This project provides a comprehensive assessment of health care facilities' accessibility in Zamfara State and offers insights into suitable locations for new facilities. By integrating data analysis and geospatial techniques, we can improve health care accessibility and address the needs of the population effectively.

## File Structure
- `data/`: Folder containing all datasets used in the analysis.
- `notebooks/`: Jupyter notebooks containing the data analysis and geospatial analysis code.
- `outputs/`: Folder containing the results, including maps and visualizations.
- `README.md`: This readme file.

## Usage
1. Clone the repository.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Run the Jupyter notebooks in the `notebooks/` folder to reproduce the analysis.
4. View the results in the `outputs/` folder.

## Dependencies
- ArcGIS Python API
- Python 3.x
- Geopandas
- Pandas
- Numpy
- Rasterio
- Matplotlib
- Seaborn
- Fiona


## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments
This project was conducted by Team Space X. We acknowledge the use of Facebook mobility data and other datasets for this analysis.