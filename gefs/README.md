# Initializing Aurora with NCEP GEFS Initial Conditions for PM2.5 Forecasting 

This directory contains the workflow used to initialize Aurora using initial conditions from the Global Ensemble Forecasting System (GEFS). Aurora is a neural-network based foundational model of the Earth system with the downstream capability for air quality prediction (Bondar et al. 2025). For air quality, Aurora was fine-tuned on data from the Copernicus Atmosphere Monitoring Service (CAMS) provided by the European Centre for Medium-range Weather Forecasting (ECMWF). Recent work from NOAA has used initial conditions from the Global Ensemble Forecasting System (GEFS) to successfully drive Aurora for PM2.5 predictions.

## IMPORTANT! 
The full run_Aurora.ipynb requires locally stored data and dedicated GPUs to generate multiple forecasts. The same core code required to pre-process GEFS and run Aurora is included in the scaled back **run_Aurora_demo.ipynb** notebook in the /demo directory. The demo is intended to work on Colab and does not require any local data. The demo can also be run on any day a user is interested in. It is highly recommended to begin with the **run_Aurora_demo.ipynb** script and adapt Aurora as necessary. The **run_Aurora.ipynb** includes more options as far as saving/exporting Aurora and is able to run for multiple initializations. Beyond this, it is identical to the **run_Aurora_demo.ipynb** script. 

## Repository 
```python
https://github.com/ehojeily/aurora_gefs/
```

## Requirements 
Initial conditions must be retrieved from CAMS and stored locally or on Google Drive. It is highly recommended that this is done prior to attempting to run Aurora on multiple initializatioin days as importing data from CAMS takes several minutes and will eat into your computing resources. 

Sample code to retrieve CAMS data is provided in the **/demo/run_Aurora_demo.ipynb** script. Multiple days of data can be retrieved from the script by simpling extended the start and end dates of data retrieval. 

**Google Drive**. All data to support this project was stored on Google Drive. As such, the notebooks mounts to Google Drive to read and export data files. If running locally, you will have to modify these lines to whatever directory you intend on working in. 

**Dependencies**. All required Python libraries are imported within the notebook. 

**Computing resources**. Running Aurora requires a dedicated GPU. The **A100 GPU** is the best option for running Aurora in inference mode. 

## Output files 
Aurora files are saved as netcdf files mirroring the format of GEFS data. The script is also configured to save Aurora files to Google Drive, however, this can be turned off within the code when configuring Aurora. 

## Misc. 
**Model evaluation** of Aurora was completed using [*Melodies-Monet*](https://melodies-monet.readthedocs.io/en/stable/) and custom plotting scripts. 

# References 
* Bodnar, Cristian, Wessel P. Bruinsma, Ana Lucic, et al. “A Foundation Model for the Earth System.” Nature 641, no. 8065 (2025): 1180–87. https://doi.org/10.1038/s41586-025-09005-y.
* Zhang et al., “Development and Evaluation of the Aerosol Forecast Member in the National Center for Environment Prediction (NCEP)’s Global Ensemble Forecast System (GEFS-Aerosols V1). https://10.5194/gmd-15-5337-2022

# Contact
Ellie H. Hojeily (ehojeily@albany.edu). 
