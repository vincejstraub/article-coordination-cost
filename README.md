# Replication materials for: The cost of coordination can exceed the benefit of collaboration in performing complex tasks

## Table of Contents
* [General info](general-info)
* [Data](#data)
* [Code](#code)
* [Figures](#figures)

## General info
This repository contains the code and (anonymized) data necessary for reproducing the main findings of [Straub, V. J., Tsvetkova, M., & Yasseri, T. (*arXiv* 2020)](https://arxiv.org/pdf/2009.11038.pdf). A more extensive collection of materials including figures found in the supplementary material can be found on the Open Science Framework [project page](https://osf.io/6rcgx/?view_only=7d72c5c914e14f6a9f6c56d313a0c08b). The following text provides a summary of each file and it's function, with further comments provided throughout the code. 


## Data
* `exp1/` contains a csv of the (anonymized) experiment data `experiment1Full.csv` and `graphs.json` defines the graph structures used in experiment 1



## Code
* `modelResults/` contains the individual cross-validated maximum likelihood estimates from Exp 1 (`Exp1/`) and Exp 2 (`networkBandit/`). It also contains `modelFit.csv` and `paramEstimates.csv` as the compiled dataframes describing the model results in Exp 2 for convenience.  In addition, `Exp1diffevidence.csv` and `Exp2diffevidence.csv` contain the log loss of each model for computing the protected exceedence probabilities, which is then saved as `Exp1PXP.csv` and `Exp2PXP.csv`. Lastly, the model-based analyses of the bonus from from Exp 2 are here for covenience as `BanditBonusRoundmodelDF.Rds`
* `plots/` contains plots for the paper, where the code will save each plot
* `utilities.R` contains data preprocessing functions for each experiment and various vector operations that are used across multiple scripts
* `statisticalTests.R` contains code for performing t-tests and correlations, where the output is formatted for Latex and automatically converted to a set number of significant digits for consistency. Contains code from van Doorn et al., (2018) for computing the Bayes factor for Kendall's rank correlation [paper](https://amstat.tandfonline.com/doi/full/10.1080/00031305.2016.1264998)

### Training Stage: 

* `Exp1Behavior.R` contains all the behavioral analyses
* `Exp1ModelCV.R` contains code for model fitting 
* `Exp1ModelingResults.R` contains code for all model-based analyses

### Testing Stage: 

* `Exp1ModelingResults.R` contains code for all model-based analyses


## Figures
* Contains the main figures reproduced by the above code. 


This code is being released with a permissive open-source license. You should feel free to use or adapt the code as long as you follow the terms of the license. If you make use of the code, we would appreciate that you cite the paper. 
