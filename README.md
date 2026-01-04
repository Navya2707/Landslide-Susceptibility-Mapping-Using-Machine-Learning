# Landslide Susceptibility Mapping Using Machine Learning (MATLAB)

## Aim
The aim of this project is to generate a landslide susceptibility map for a selected region using machine learning techniques in MATLAB.

## Project Overview
This project uses various geographical and environmental factors as input data to predict landslide-prone areas. A cascade feed-forward neural network is trained using historical landslide data and then applied to generate a susceptibility map for the region of interest.

## Data Collection
Raster maps are collected from **Bhukosh (GSI)**.

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
- Region of Interest (ROI) selected using MATLAB Image Segmenter
- ROI masking applied to all parameter maps
- Random pixel samples extracted from the ROI
- Input and target data stored in matrix and CSV format

## Model Architecture
- Cascade Feed-Forward Neural Network
- 36 input features
- 24 hidden neurons
- Output represents landslide susceptibility class

## Model Training
Training parameters used:
- Epochs: 40  
- Learning Rate: 0.01  
- Momentum: 0.1  
- Max Validation Checks: 6  

The trained model is saved as a `.mat` file.

## Prediction and Mapping
The trained model is applied to all pixels within the ROI to predict landslide susceptibility. The predicted values are used to generate the final susceptibility map.

## Results
The output map highlights **low, medium, and high landslide-risk zones**, which can assist in disaster management and land-use planning.

## How To Run
1. Provide paths to all raster files in the MATLAB script  
2. Select the ROI using Image Segmenter and export `segmentImage.m`  
3. Set the training parameters  
4. Run `LandslideMapping.m`  

## Key Features
- Implemented entirely in MATLAB
- No external GIS software required
- Flexible ROI-based analysis
- Supports multiple raster image formats

## Conclusion
This project demonstrates an effective and simple approach for landslide susceptibility mapping using machine learning in MATLAB.

## License
MIT License
