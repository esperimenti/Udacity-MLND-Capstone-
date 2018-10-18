The dataset select for the proposal was published on Kaggla:
https://www.kaggle.com/paultimothymooney/breast-histopathology-images

To download it follow the link above and click download (1.53 GB)

########################
### Project contents ###
########################
1) report.pdf - the full projcet report
2) proposal.pdf - the proposal for the project
3) 'Rapid Diagnosis of IDC in Mammography Scans using Deep Learning.ipynb' - an iPython notebook with the project code
4) results directory - some sample HTML reports of the iPython notebook experiments
5) sample_simulation_on_tiny_dataset directory - a copy of the notebook setup for running quickly on tiny data (if you dont want to run on the full dataset)


######################
### Prerequisites: ###
######################
0) Install python3.6.5 Jupyter nodtebook server 5.5.0

1) Install the the following python packages: 
			pip install keras, tf-nightly-gpu, opencv-python

2) Start the Jupyter notebook server (e.g. jupyter notebook --ip=0.0.0.0 --no-browser  --notebook-dir=<<my local dir>>

3) Download the dataset from Kaggle (1.55GB): https://www.kaggle.com/paultimothymooney/breast-histopathology-images

4) Extract the dataset zip file in a directory acceissble by you notebook (--notebook-dir=<<my local dir>>)
################################
### FULL Test Configuration: ###
################################

Important noteE: if you just want to see the notebook running quickly on a tiny dataset skip to "Simulation on a tiny dataset"

5) Open the notebook, and Configure the "global settings" cell for your test:
--- Optional: Set a working directory for the test: 'BASE_RUN_DIR = 'trained_models/04-09-2018/' #dd-MM-yyyy

--- Set the input training dataset directory (where you extraced the Zip): TRAIN_DATA_DIR = 'IDC_regular_ps50_idx5/'

--- Move (!!!) some of the input images from the TRAIN_DATA_DIR to a new directory and point the TEST_DATA_DIR to it: TEST_DATA_DIR = 'UNSEEN_DATA/'

--- Set the number of images to load: MAX_NUM_IMAGES_TO_LOAD = 90000 for example: 
----- 90000 images ~ 3.5 hours (30 minutes per fold)
----- 250K images ~ 8 hours (60 minutes per fold)


6) Click Cell --> Run All


#####################################
### Simulation on a tiny dataset: ###
#####################################

The sub-directory "sample_simulation_on_tiny_dataset" contains a copy of the notebook,
 and it is configured to work on tiny local datasets (validation is done with a pretrained full CNN model).
Open the notebook in Jupyter and just 'Run All' :)