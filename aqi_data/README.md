# AQI Data Folder

## Overview

This folder contains all of the air quality data under consideration in our project. The data was collected from the EPA website[https://www.epa.gov/outdoor-air-quality-data/download-daily-data]. Each of the csv files contains all of the site locations in CA for the csv's respective year. These readings are eventually matched to the image data downloaded in the img_data/ folder.

After downloading the desired EPA data, use `epa_data_manipulation.ipynb` to clean the data into the form usable by the modeling process.

## File structure
### Current directory
- `epa_data_manipulation.ipynb` : code for cleaning the EPA data
- `all_sites_particleName_year.csv`: data downloaded from the EPA website containing all AQI readings for the particle and year.

### final_data subfolder
- `all_sites_data.csv` : cleaned file of max AQI for the desired sites and dates
- `label_file.csv`: the final label file used for training; maps the images to the above AQI data.

