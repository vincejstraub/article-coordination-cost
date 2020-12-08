# Replication materials for: The cost of coordination can exceed the benefit of collaboration in performing complex tasks

## Table of Contents
* [General info](general-info)
* [Data](#data)
* [Analysis](#code)

## General info
This repository contains the code and (anonymized) data necessary for reproducing the main findings of [Straub, V. J., Tsvetkova, M., & Yasseri, T. (*arXiv* 2020)](https://arxiv.org/pdf/2009.11038.pdf). A more extensive collection of materials including figures found in the supplementary material can be found on the Open Science Framework [project page](https://osf.io/6rcgx/?view_only=7d72c5c914e14f6a9f6c56d313a0c08b). The text below provides a summary of each file and it's function, with further comments provided throughout the code. Once all data and code are downloaded, open a notebook (see below) and use the `paths.py` file in the `lib` folder to point to the right path. The code will automatically access the relevant data files. The notebook should already contain the expected output. Execute cells one by one. 

## Data
* `exp1/` contains a csv of the (anonymized) experiment data `experiment1Full.csv` and `graphs.json` defines the graph structures used in experiment 1

## Analysis
* `01-data_preparation.ipynb`: this is the main data preparation notebook that takes in the raw data and performs data cleaning and formatting, preprocessing, and descriptive statistics; it should be run first. 
* `02-plot_figure_2.ipynb`: contains code for reproducing individual panels depicted in Figure 2 of the main text, where the code will save each plot. 
* `03-plot_figure_3.ipynb`: contains code for reproducing individual panels depicted in Figure 3 of the main text, where the code will save each plot. 
* `04-plot_figure_4.ipynb`: contains code for reproducing individual panels depicted in Figure 4 of the main text, where the code will save each plot. 
* `05-statistical_tests.ipynb`: contains code for performing analysis of variance and post-hoc tests, where the output is automatically converted to a set number of significant digits for consistency. 
* `evaluating_classifications.py`: contains data preprocessing functions for both stages of the experiment, helper functions and various operations that are used in the `01-data_preparation.ipynb` notebook. 
* `sliding_window.py`: contains data analysis functions for conducting a sliding window analysis of each experimental group's performance for both stages of the experiment across each task. The script is called in `01-data_preparation.ipynb` to generate processed DataFrames ready for plotting and statistical testing. 

## Requirements
- Python 3.7.7
- Pandas, Matplotlib, Seaborn, Pingouin 
- Jupyter

Please follow the online instructions to install the required libraries, depending on your operating system and machine specifications. 

This code is being released with a permissive open-source license. You should feel free to use or adapt the code as long as you follow the terms of the license. If you make use of the code, we would appreciate that you cite the paper. 
