# Anticipating future incremental densification: <br> A parcel-level modelling framework for urban planning
This repository provides the code used to develop a parcel-level modelling framework for anticipating incremental densification within existing urban areas. The workflow predicts both, the probability that densification occurs on a parcel, and the expected increase in floor area where densification takes place (see figure below). The approach is implemented for Munich, Germany, using parcel-level observations of densification between 2013 and 2023, and applied to derive a baseline scenario for future densification between 2023 and 2033.

<img src="https://github.com/user-attachments/assets/ed05724b-d1ae-4816-ab66-fc7f4409e897" width="600">

## Getting started
The repository is intended to provide transparent documentation of data preparation and of the modelling and prediction workflow. Because several input datasets are proprietary or protected, the full workflow cannot be reproduced without access to local municipal data.

### Input data
More information on input data is provided in [data_description.md](https://github.com/urban-structure-and-policy/Anticipating-future-incremental-densification/blob/main/data_description.md).

### Output
The output of the workflow is a parcel-level dataset containing:

- probability of densification for each parcel  
- expected increase in floor area  
- parcel type classification  
- scenario-based selection of likely densified parcels  

The results can be aggregated spatially (e.g. 500 m grid) to analyse spatial patterns of future densification and support strategic urban planning.

### Prerequisites
All parts of the workflow run in [R](https://www.r-project.org/). Further details on all versions and packages used can be found [here](https://github.com/urban-structure-and-policy/Anticipating-future-incremental-densification/blob/main/R_and_R_packages.md). 

### Description of the code
The code is structured in three parts. Each part can be run by executing the run_all scripts, which gives an overview on all processing steps.

* Data preparation 2013 -> [00_run_all_data_prep_2013.Rmd](https://github.com/urban-structure-and-policy/Anticipating-future-incremental-densification/tree/main/code/data_preparation_2013)
* Data preparation 2023 -> [00_run_all_data_prep_2023.Rmd](https://github.com/urban-structure-and-policy/Anticipating-future-incremental-densification/tree/main/code/00_run_all_data_prep_2023.Rmd)
* Models and prediction -> [00_run_all_models_and_predictions.Rmd](https://github.com/urban-structure-and-policy/Anticipating-future-incremental-densification/tree/main/code/00_run_all_models_and_predictions.Rmd)
