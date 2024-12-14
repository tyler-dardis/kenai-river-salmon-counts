# Kenai River Salmon Count Forecasting
Machine learning project to forecast fish counts (late-run sockeye salmon) in the Kenai River.

My goal for this project is to develop a machine learning pipeline that utilizes historical fish count data, as well as environmental data, to forecast daily fish counts during the sockeye salmon run in the Kenai River (Kenai Peninsula, Alaska).

**Timeline:** My goal is to have the model ready to deploy before the 2024 salmon run (July).

### Data for training model:
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
