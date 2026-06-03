This directory contains the necessary files to run a simple demo of the Aurora-GEFS workflow using the 'Run_Aurora_DEMO.ipynb' on Google Colab. 

To run the demo on Google Colab, simply open the notebook in Colab. All dependencies required by the notebook are installed and configured within the notebook. Any figures or datasets made when running the notebook on Colab are subject to deletion when disconnecting from runtime, so please be mindful to save outputs as necessary. The demo is intended to run on a A100 GPU. In my experience, it can occasionally work on other GPUs but the A100 is the most reliable. 

The demo allows users to configure Aurora using a dictionary which will replace CAMS and GEFS initial conditions, as required, and is flexible to users omitting surface and atmospheric variables. Omitting some variables (i.e., ozone) WILL cause Aurora to become unstable. If this happens, this is OK and should not affect other configurations. 

Finally, when running these notebooks, PLEASE be mindful of your computing resource allocation and usage. The A100 usually costs 7 computing units per hour on Colab. Importing large CAMS datasets will eat into your computing resources, which is why the demo is intended to only import 2 CAMS analysis datasets. If you decide to run Aurora using multiple days of CAMS analysis, I highly recommend downloading the CAMS data prior to running Aurora and saving it locally. This was the approach used in the run_Aurora.ipynb script where the CAMS data were stored on Google Drive. 

If you have any questions or need assistance, please contact Ellie H. Hojeily (ehojeily@albany.edu).
