# City Subway Design

This project provides the functions needed to create an optimized central subway route in any city in the United States for which there is data available representing the total population broken down by census block. The code here completes that process for Columbus, Ohio, Cleveland, Ohio, and Pittsburgh, Pennsylvania. While Cleveland and Pittsburgh already have small rail transit services, the outputs in those cities were used to demonstrate improvements in population accessibility.

### Data

##### Geodata
Geodata for all census blocks was too large of a dataset to load in GitHub - can be found at https://hub.arcgis.com/datasets/fedmaps::u-s-census-blocks-1/about.

The RMD file contains the codeused on the national geodata file to isolate and export state-level data that is easier to work with in the optimization models.

DataReading.ipynb contains the functions to clean all of the downloaded geodata and census block population data.

##### Population Data
The ColumbusCensusBlocksPopulations dataset contains block-by-block populations for the Columbus metropolitan area.
The ClevelandCensusBlocksPopulations dataset contains block-by-block populations for the Cleveland metropolitan area.

### Analysis

SubwayDesign.ipynb contains functions that can be used to read geodata and population data, run the station selection model with mandatory points that have low population densities, produce maps of those points, run the route optimization model, and plot that optimized route.

Testing.ipynb contains the steps to actually run the station selection model and route optimization for both Columbus and Cleveland. It also contains the code that determines the population accessed by the existing rail lines in Cleveland, to compare against the results of the model-designed route.

### Output

The city maps show the optimized subway routes produced by the station selection and route optimization models.
