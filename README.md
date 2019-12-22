# p300-speller
A BCI speller based on P300 detection using a 1D CNN architecture.

The aim of this project is to understand the limits and the potentials of Brain Computer Interfaces (BCI) used to facilitate communication for people with brain injuries. The methodology implemented in this work is based on the development of binary classification models for Evoked Related Potential (ERP) through which we retrieve the information about the character spelled by the patient.

# Experiment procedure:

The dataset of this project comes from the third BCI competition and consists of 50 min of EEG recordings and speller matrix information from 2 subjects (renamed subject A and subject B). The data is acquired during an experiment set up as follows:

1) The speller matrix is displayed on a monitor in front of the subject. Its columns and rows are numbered sequentially from 1 to 12 (left to right and then top to bottom);

2) For every character epoch the subject is asked to focus his view on a sigle character of the speller matrix for the entirety of the epoch duration;

3) In a single character epoch each one of the 12 columns/rows of the matrix lights up in a random order for 100 ms followed by 75 ms in which every columns/rows is turned off;

4) The procedure is repeated 15 times for each character in the dataset, for a total of 12 x 15 = 180 columns/rows flashes during 15 epochs of a single character;

![P300 experiment procedure](https://gualor.github.com/p300-speller/images/p300experiment.png)

# Materials:
All the materials of this project are organized into 3 separate folders:

- **Python_script**: contains all notebook scripts (.ipynb files);

- **Dataset**: contains all training and testing sets for both subjects, EEG channels names and respective coordinates for the topoplot representation (.mat and .csv files);

- **Trained_models**: contains all the trained models (.h5 files);

# Usage information:
- The project has been developed to be used with Google Colab service, thus the file paths mounted refer to a directory in the Google Drive cloud service for a simple use;

- At the top of all scripts, information about the settings are given. Settings may include:
	- Subject's data selection (A or B);
	- Trained model selection (CNN1, CNN2a, CNN2b, CNN2c, CNN3, MCNN1, MCNN2, MCNN3);
	- EEG channels group selection (F, C, P, O, LT, RT);
	
- All settings available can be changed in the first code section of the notebook script;

- By changing settings the path names will be updated automatically;

- Scripts are divided in sub-sections with headers explaining the procedures implemented;
