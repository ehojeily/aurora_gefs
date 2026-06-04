# Run Aurora with GEFS initial conditions demo

Aurora is a neural-network based foundational model of the Earth system with the downstream capability for air quality prediction (Bondar et al. 2025). For air quality, Aurora was fine-tuned on data from the Copernicus Atmosphere Monitoring Service (CAMS) provided by the European Centre for Medium-range Weather Forecasting (ECMWF). Recent work from NOAA has used initial conditions from the Global Ensemble Forecasting System (GEFS) to successfully drive Aurora for PM2.5 predictions. This demo allows users to replicate this workflow and run sensitivity tests using Aurora. 

## Repository 
```python
https://github.com/ehojeily/aurora_gefs/
```

## Requirements 
You will need an API key to retrieve CAMS data from the ECWMF Climate Data Store. Aurora requires SO2 data, at minimum, to generate air quality forecasts without an error. Visit [here](https://accounts.ecmwf.int/auth/realms/ecmwf/protocol/openid-connect/auth?client_id=cds&scope=openid%20email&response_type=code&redirect_uri=https%3A%2F%2Fcds.climate.copernicus.eu%2Fapi%2Fauth%2Fcallback%2Fkeycloak&state=TNQu0RtsUNmp_BjUwqsvTZmnTLCnUKCW-8J-2oqXl34&code_challenge=U-NaEWhoFdMDgZFhegjCs4Hs84nuLCkaS1-3HaOBmQc&code_challenge_method=S256)  to generate an API key. The **run_Aurora_demo.ipynb** notebook indicates where this API key should be copy and pasted.  

## Running the demo script on Google Colab *(recommended)*

In Google Colab, select **File** --> **Open notebook** --> **Github** --> **Enter a Github URL or search by organization or user**

Then, copy and paste the following link into the search bar: 
```python
https://colab.research.google.com/github/ehojeily/aurora_gefs/blob/main/gefs/demo/run_Aurora_demo.ipynb
```
This will load the notebook in Colab. 

### Specifying computing resources in Colab

The default resource allocation is insufficient for running Aurora. In Colab, you must upgrade your computing resources to, at minimum, a GPU. The **A100 GPU** is the best option for running Aurora in inference mode. 

To do this, in the top left menu, select the **downward arrow** next to the RAM and disk usage. 
Then, select **Change runtime type** --> **A100 GPU** (*recommended*)

## Run the notebook to generate Aurora forecasts! 

All required dependencies are installed within the **run_Aurora_demo.ipynb**. 

## Output files
**IMPORTANT!** Notebooks run on Colab are temporary allocated space. Disconnecting the the GPU will cause the Notebook and all output files to disappear. Save any files you deem necessary *locally* before disconnecting from Colab! 

Running the notebook will produce copies of the CAMS initial conditions in the /demo directory and figures of the Aurora forecasts. 

# References 
* Bodnar, Cristian, Wessel P. Bruinsma, Ana Lucic, et al. “A Foundation Model for the Earth System.” Nature 641, no. 8065 (2025): 1180–87. https://doi.org/10.1038/s41586-025-09005-y.
* Zhang et al., “Development and Evaluation of the Aerosol Forecast Member in the National Center for Environment Prediction (NCEP)’s Global Ensemble Forecast System (GEFS-Aerosols V1). https://10.5194/gmd-15-5337-2022

**More Aurora demos can be found [here](https://microsoft.github.io/aurora/intro.html) in the Aurora documentation** 

# Contact 
Ellie Hojeily (ehojeily@albany.edu)
