REQUIREMENTS
- Python 3.7.7
- Pandas, Matplotlib, Seaborn, Pingouin 
- Jupyter

N.B. When finished, this file should contain information that will help your forgetful future self, newcomers, and collaborators figure out why this project exists, how things are organized, conventions used in the project, and where they can go to find more information.

INSTALLATION GUIDE
Please follow the online instructions to install the required libraries, depending on your operating system and machine specifications. 

DEMO
Once all data and code are downloaded, open a notebook (see below) and use the `paths.py` file in the `lib` folder to point to the right path. The code will automatically access the relevant data files. The notebook should already contain the expected output. Execute cells one by one. 

FILES 
* `01-data_preparation.ipynb`: this is the main data preparation notebook that takes in the raw data and performs data cleaning and formatting, preprocessing, and descriptive statistics; it should be run first. 
* `02-plot_figure_2.ipynb`: contains code for reproducing individual panels depicted in Figure 2 of the main text, where the code will save each plot. 
* `03-plot_figure_3.ipynb`: contains code for reproducing individual panels depicted in Figure 3 of the main text, where the code will save each plot. 
* `04-plot_figure_4.ipynb`: contains code for reproducing individual panels depicted in Figure 4 of the main text, where the code will save each plot. 
* `05-statistical_tests.ipynb`: contains code for performing analysis of variance and post-hoc tests, where the output is automatically converted to a set number of significant digits for consistency. 
* `evaluating_classifications.py`: contains data preprocessing functions for both stages of the experiment, helper functions and various operations that are used in the `01-data_preparation.ipynb` notebook. 
* `sliding_window.py`: contains data analysis functions for conducting a sliding window analysis of each experimental group's performance for both stages of the experiment across each task. The script is called in `01-data_preparation.ipynb` to generate processed DataFrames ready for plotting and statistical testing. 
