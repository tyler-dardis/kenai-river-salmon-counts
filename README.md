# Kenai River Salmon Count Forecasting Pipeline
Machine learning project to forecast fish counts (late-run sockeye salmon) in the Kenai River.

My goal for this project is to develop a machine learning pipeline that utilizes historical fish count data, as well as environmental data, to forecast daily fish counts during the sockeye salmon run in the Kenai River (Kenai Peninsula, Alaska).

**Timeline:** My goal is to have the model ready to deploy before the 2024 salmon run (July).

## Next steps:
- Write scripts to pull data from external sources
  - **MIGRATE THIS TASK LIST TO ISSUES/PROJECTS**
  - (DONE) Fish counts - Working scripts in notebook; need to finalize in .py file
  - (DONE) Water metrics - Working scripts in notebook; need to finalize in .py file
  - Water levels/tidal data - Working on scripts to pull from NOAA API. (reference links in notebooks)
  - Weather data (need to identify which NWS sites should be included)
  - Consolidate data ingestion scripts into a .py file for production

## Repository Structure
(This is more of the _planned_ structure, since many of these components have not yet been added):
- **data/** - Contains all data pulled by data_ingestion.py scripts
  - **raw_data/** - Raw, unprocessed data files
  - **processed_data/** - Processed data, prepared for modeling
- **notebooks**/ - Contains all notebooks used for prototyping
  - **data_ingestion.ipynb** - Data ingestion notebook, fetching data from external sources and saving unprocessed data in .../data/raw_data/
  - **EDA.ipynb** - Exploratory data analysis notebook
  - **data_processing.ipynb** - Data cleaning/processing and feature engineering notebook
  - **model_evaluation.ipynb** - Model training and evaluation notebook
- **src/** - Contains all scripts for each pipeline step
  - **\_\_init\_\_.py**
  - **data_ingestion.py** - Scripts to pull in data
  - **preprocess.py** - Scripts for cleaning/processing data and feature engineering
  - **model_training.py** - Scripts for training models
  - **predict.py** - Scripts for generating fish count forecasts
- **models/** - Contains trained models
- **tests/** - Contains scripts to test pipeline component scripts
  - **test_data_ingestion.py** - Unit tests for data ingestion
  - **test_process.py** - Unit tests for data processing
  - **test_model_training.py** - Unit tests for model training
- **scripts/** - Scripts for deploying the pipeline
  - **run_pipeline.sh** - Script to run entire pipeline
  - **train_model.py** - Command-line interface to train model
  - **predict.py** - Command-line interface for predicitons
- **requirements.txt** - List of all dependencies

## Data for training model:
|Data Description|Source|Link|Frequency|
|----|------|----|---------|
|Fish counts (sockeye salmon)|Alaska Department of Fish and Game|https://www.adfg.alaska.gov/sf/FishCounts/index.cfm?ADFG=main.displayResults&COUNTLOCATIONID=40&SpeciesID=420|Daily|
|Water temperature, air temperature, water level, discharge/flow rates|USGS|https://waterdata.usgs.gov/monitoring-location/15266300/#dataTypeId=continuous-00065-0&period=P7D&showMedian=false| Daily(?)|
|Trolling records|?|?|?|
|Historical fishing restrictions|Alaska Department of Fish and Game|?|?|

## Further reading/research:
|Description|Link|
|-----------|----|
|USGS Water Science School|https://www.usgs.gov/special-topics/water-science-school|
