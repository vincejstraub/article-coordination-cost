# Replication materials for: The cost of coordination can exceed the benefit of collaboration in performing complex tasks

## Table of Contents
* [General info](general-info)
* [Data](#data)
* [Analysis](#code)
* [Requirements](requirements)

## General info
This repository contains the code and (anonymized) data necessary for reproducing the main findings of [Straub, V. J., Tsvetkova, M., & Yasseri, T. (*arXiv* 2020)](https://arxiv.org/pdf/2009.11038.pdf). A more extensive collection of materials including figures found in the supplementary material can be found on the Open Science Framework [project page](https://osf.io/6rcgx/?view_only=7d72c5c914e14f6a9f6c56d313a0c08b). The text below provides a summary of each file and it's function, with further comments provided throughout the code. Once all data and code are downloaded, open a notebook (see below) and use the `paths.py` file in the `lib` folder to point to the right path. The code will automatically access the relevant data files. The notebook should already contain the expected output. Execute cells one by one. 

## Data
* `Raw/`: contains a json of the (anonymized) participant classification data `classsifications.json` and timestamp jsons `standardize_training_starttimes` and `standardize_testing_starttimes` that contain datetime data points to standardize the classifications made by participants during the training stage and testing stage (i.e. update all times to start at 12:00:00) for sliding window analysis. `training_ids.txt` and `testing_ids.txt` contain a list of ids randomly allocated to participants for both stages of the experiment. `multispecies_image_ids.json` contains  ids of Zooniverse images with multiple species entries (i.e. correct answers; see S2.1 in [supplementary material](https://arxiv.org/pdf/2009.11038.pdf) for details).
* `Processed/`: contains a json of the 'ground truth' classifications `wildcam_gorongosa_answers.json`; aggregated citizen scientist-provided labels for each image downloaded from The Zooniverse.

## Analysis
* `01-data-preparation.ipynb`: this is the main data preparation notebook that takes in the raw data and performs data cleaning and formatting, preprocessing, and descriptive statistics; it should be run first. 
* `02-plot-figure-2.ipynb`: contains code for reproducing individual panels depicted in Figure 2 of the main text, where the code will save each plot. 
* `03-plot-figure-3.ipynb`: contains code for reproducing individual panels depicted in Figure 3 of the main text, where the code will save each plot. 
* `04-plot-figure-4.ipynb`: contains code for reproducing individual panels depicted in Figure 4 of the main text, where the code will save each plot. 
* `05-plot-si-figures.ipynb`: contains code for reproducing individual panels depicted in the supplementary information.
* `06-statistical-tests.ipynb`: contains code for performing analysis of variance and post-hoc tests, where the output is automatically converted to a set number of significant digits for consistency. 
* `evaluating_classifications.py`: contains data preprocessing functions for both stages of the experiment, helper functions and various operations that are used in the `01-data_preparation.ipynb` notebook. 
* `sliding_window.py`: contains data analysis functions for conducting a sliding window analysis of each experimental group's performance for both stages of the experiment across each task. The script is called in `01-data-preparation.ipynb` to generate processed DataFrames ready for plotting and statistical testing. 


## Requirements
- Python 3.7.7
- Pandas, Matplotlib, Seaborn, Pingouin 
- Jupyter

Please follow the online instructions to install the required libraries, depending on your operating system and machine specifications. 

This code is being released with a permissive open-source license. You should feel free to use or adapt the code as long as you follow the terms of the license. If you make use of the code, we would appreciate that you cite the paper. 
