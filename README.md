###################################################################
# Rapid Diagnosis of IDC in Mammography Scans using Deep Learning #
###################################################################

The dataset select for the proposal was published on Kaggle:
https://www.kaggle.com/paultimothymooney/breast-histopathology-images

To download it follow the link above and click download (1.53 GB)

########################
### Project contents ###
########################
1) report.pdf - the full projcet report
2) 'Rapid Diagnosis of IDC in Mammography Scans using Deep Learning.ipynb' - an iPython notebook with the project code


######################
### Prerequisites: ###
######################
0) Install python3.6.5 Jupyter notebook server 5.5.0

1) Install the the following python packages (GPU is highly recommended if running on the full dataset...): 
			pip install keras, tf-nightly-gpu, opencv-python

2) Start the Jupyter notebook server (e.g. jupyter notebook --ip=0.0.0.0 --no-browser  --notebook-dir=<<my local dir>>

3) Download the dataset from Kaggle (1.55GB): https://www.kaggle.com/paultimothymooney/breast-histopathology-images

4) Extract the dataset zip file in a directory acceissble by your notebook (--notebook-dir=<<my local dir>>)
################################
### FULL Test Configuration: ###
################################

5) Open the notebook, and Configure the "global settings" cell for your test:
--- Optional: Set a working directory for the test: 'BASE_RUN_DIR = 'trained_models/04-09-2018/' #dd-MM-yyyy

Create empty diretories for train (IDC_regular_ps50_idx5) and unseen test data (UNSEEN_DATA)
--- Set the input training dataset directory (where you extraced the Zip): TRAIN_DATA_DIR = 'IDC_regular_ps50_idx5/'

--- Move (!!!) some of the input images from the TRAIN_DATA_DIR to a new directory and point the TEST_DATA_DIR to it: TEST_DATA_DIR = 'UNSEEN_DATA/'

--- Set the number of images to load: MAX_NUM_IMAGES_TO_LOAD = 90000 for example: 
----- 90000 images ~ 3.5 hours (30 minutes per fold)
----- 250K images ~ 8 hours (60 minutes per fold)


6) Click Cell --> Run All :)
