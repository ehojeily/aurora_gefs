This directory contains the workflow used to initialize Aurora using GEFS initial conditions. The run_Aurora.ipynb contains the neccessary pre-processing of GEFS data required to ensure compatibility with Aurora. 

In order to use the run_Aurora.ipynb script, initial conditions from the CAMS Analysis must be retrieved from ECMWF. Sample code to do so is provided in the /demo/run_Aurora_demo.ipynb notebook. Model evaluation of Aurora was completed using Melodies-Monet (https://melodies-monet.readthedocs.io/en/stable/) and custom plotting scripts. The script is also configured to save Aurora files to Google Drive, however, this option can be turned off within the code. 

The run_Aurora_demo.ipynb notebook uses the same pre-processing and Aurora code as the main run_Aurora.ipynb notebook, however, it is scaled back to allow users to experiment with variables without costing a substantial amount of computing units from Colab by only forecasting for a single initialization time. Both notebooks are compatible with the A100 GPU on Google Colab. 

Author: Ellie H. Hojeily 
Contact: ehojeily@albany.edu
