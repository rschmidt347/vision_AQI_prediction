# Image Data Folder

## Overview
This folder contains notebooks to download and manipulate the satellite imagery into a form usable for modeling. The process can be broken down into the following steps.

### 1. Identify site locations
Follow the instructions in the `SearchAPI.ipynb` notebook to find the geographic locations for the desired sites.

### 2. Download the images
Move to `OrderAPI.ipynb` to order the desired imagery from Planet.com.

### 3. Create a final file-to-site mapping
Use `create_mapping_csv.ipynb` to create a final .csv file of file-to-site mappings from the numerous file-to-site mappings downloaded in the process of acquiring the images (these will end up in the `fileToSite` folder).

### 4. Comb through the imagery to create the final dataset
Move through the interactive `move_images_to_folders.ipynb` to create the final label file, assign train/valid/test sets, and convert the images to a final form usable by the model.

## Structure
### Notebooks
1. `SearchAPI.ipynb`
2. `OrderAPI.ipynb`
3. `create_mapping_csv.ipynb`
4. `move_images_to_folders.ipynb`

### Files
- `file2siteWClouds.txt` : file-to-site mapping that specifically identifies very cloudy images
- `fileToSite.txt` : the master list of images and corresponding sites

### Sub-directories
- `county_site` : the main image repository
- `fileToSite` : location for the file-to-site mappings at the yearly level
- `pred_grid`, `prediction_clipped`, and `prediction_strips`: imagery for the unsupervised task
- `rotation_fixed` : repository for fixed images that were rotated unintentionally during the image download process
