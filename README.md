# mRNA Subcellular Localization Predictor
UMSLP: Unified mRNA Subcellular Localization Predictor based on Machine Learning Techniques


## Data folder
Contains 2 floders:

* TEST_01: Testset_01: 
         Independent dataset files used for testing only.
* Train: Training Dataset: 
         Contains all five Fasta Sequence Files used to train MSLP models. The fifth one is a combination of all Fastafiles.

## Code Folder:
 
## Docker Guideline:

Use the PREBUILT Docker image available on the public Docker Hub Account**

FROM USER SIDE (User Computer):
1. Install Docker Desktop (Windows, Linux, or MacBook iOS)
	You can download and install Docker Desktop from: https://www.docker.com/products/docker-desktop/ 

2. RUN the following command: Open a terminal session (Windows - command line or cmd, on MacBook it is terminal, on Ubuntu it is console app)
	- Type in the following command:
		docker run -p 7000:8000 smusleh/localization:umslp
	- Open the local browser and type in the address bar the following link:
	  http://127.0.0.1:7000/docs or http://localhost:7000/docs  

Once the container is up and running:

1. Open the local browser and type in the address bar the following link:
	http://127.0.0.1:7000/docs or http://localhost:7000/docs 

2. Expand POST /predict endpoint, then click on "Try it out"
   Click on the "Choose File" button and upload the fasta file, then CLICK on the "Execute" button
   Then all Fasta sequences get processed (all features generated in a "master" file, then
   each sequence in the master file passes through all classifiers, a prediction probability
   get generated, and then the sequence gets assigned to classifiers that have the highest 
   probability. The sequences are then of that classier class.

**Download Prediction Results: To download the predictions in CSV format.**   
   Type in the following link:
   http://localhost:7000/download_prediction_file
   
   To download the features file generated "master.csv" file, open a new tap on the browser and
   type in the following link:
   http://localhost:7000/download_feature_file
   


![image](https://user-images.githubusercontent.com/19537901/211297065-1a82aff3-34b1-4b75-ad8f-78f0a28e685b.png)



