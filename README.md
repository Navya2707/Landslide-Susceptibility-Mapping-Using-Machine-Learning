Landslide Susceptibility Mapping Using Machine Learning (MATLAB)
#Aim

The aim of this project is to generate a landslide susceptibility map for a selected region using machine learning techniques in MATLAB.

#ProjectOverview

This project uses various geographical and environmental factors as input data to predict landslide-prone areas. A cascade feed-forward neural network is trained using historical landslide data and then applied to generate a susceptibility map for the region of interest.

#DataCollection

Raster maps collected from Bhukosh (GSI)

Input parameters include:

Slope

Aspect

Elevation

Rainfall

NDVI

Soil Type

Distance from roads, rivers, and faults

Historical landslide map used as target data

Image formats: JPG, PNG, etc.

#DataPreprocessing

Region of Interest (ROI) selected using MATLAB Image Segmenter

ROI masking applied to all parameter maps

Random pixel samples extracted from ROI

Input and target data stored in matrix and CSV format

#ModelArchitecture

Cascade Feed Forward Neural Network

36 input features (RGB values of 12 parameters)

24 hidden neurons

Output represents landslide susceptibility level

#ModelTraining

Training parameters used:

Epochs: 40

Learning Rate: 0.01

Momentum: 0.1

Max Validation Checks: 6

Trained model saved as .mat file.

#PredictionAndMapping

Model applied to all pixels within ROI

Susceptibility values predicted

Final landslide susceptibility map generated

Color scheme matches historical landslide data

#Results

The output map highlights low, medium, and high landslide risk zones, helping in hazard assessment and planning.

#HowToRun

Add paths to raster files in the MATLAB script

Select ROI and export segmentImage.m

Set training parameters

Run LandslideMapping.m

Update ROI file if required

#KeyFeatures

Fully implemented in MATLAB

No external GIS software required

Flexible ROI-based analysis

Supports multiple raster image formats

Easy to adapt for different regions

#Conclusion

This project demonstrates an effective approach for landslide susceptibility mapping using machine learning in MATLAB, useful for disaster risk analysis and land-use planning.
