# Landslide Susceptibility Mapping Using Machine Learning (MATLAB)

## Aim
The aim of this project is to generate a landslide susceptibility map for a selected region using machine learning techniques in MATLAB.

## Project Overview
This project uses various geographical and environmental factors as input data to predict landslide-prone areas. A cascade feed-forward neural network is trained using historical landslide data and then applied to generate a landslide susceptibility map for the selected region.

## Data Collection
Raster maps are collected from Bhukosh (Geological Survey of India).

### Input Parameters
- Slope  
- Aspect  
- Elevation  
- Rainfall  
- NDVI  
- Soil Type  
- Distance from roads  
- Distance from rivers  
- Distance from faults  

The historical landslide map is used as the target data.

## Data Preprocessing
- Region of Interest (ROI) is selected using MATLAB Image Segmenter
- ROI masking is applied to all parameter maps
- Random pixel samples are extracted from the ROI
- Input and target data are stored in matrix and CSV format

## Model Architecture
- Cascade Feed-Forward Neural Network
- 36 input features
- 24 hidden neurons
- Output represents landslide susceptibility level

## Model Training
Training parameters used:
- Epochs: 40  
- Learning Rate: 0.01  
- Momentum: 0.1  
- Max Validation Checks: 6  

The trained model is saved as a `.mat` file.

## Prediction and Mapping
The trained model is applied to all pixels within the selected ROI to predict landslide susceptibility. The predicted values are then used to generate the final landslide susceptibility map.

## Results
The output map highlights low, medium, and high landslide-risk zones, which can help in disaster management and land-use planning.

## How To Run
1. Provide paths to all raster files in the MATLAB script  
2. Select the ROI using Image Segmenter and export `segmentImage.m`  
3. Set the training parameters  
4. Run `LandslideMapping.m`  

## Key Features
- Fully implemented using MATLAB
- No external GIS software required
- Flexible ROI-based analysis
- Supports multiple raster image formats

## Conclusion
This project demonstrates an effective approach for landslide susceptibility mapping using machine learning techniques in MATLAB.

## License
This project is licensed under the MIT License.
