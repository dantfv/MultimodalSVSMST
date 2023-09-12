![alt text](http://parsecproject.org/wp-content/uploads/2019/10/cropped-PARSEC_Logo-1.png)

# A NAIVE MULTIMODAL DEEP LEARNING APPROACH FOR ESTIMATING SOCIO-ECONOMIC INDICATORS BY COMBINING AERIAL, SATELLITE AND STREET-LEVEL IMAGERY

This code was used to generate results and images for the submitted article "A NAIVE MULTIMODAL DEEP LEARNING APPROACH FOR ESTIMATING SOCIO-ECONOMIC INDICATORS BY COMBINING AERIAL, SATELLITE AND STREET-LEVEL IMAGERY
". (2023)  VELLENICH, Danton Ferreira; MACHICAO, Jeaneth; PIZZIGATTI CORRÊA Pedro; 

For complete reproducibility and replication, see notes in “Reproducibility and Replication” below.

## Links to related projects

This work was based on the [paper](https://www.nature.com/articles/s41598-019-42036-w) with source code in [github](https://github.com/esrasuel/measuring-inequalities-sview)

## REQUIREMENTS:

### SOFTWARE:
Main software requirements:
Python 3.7
TensorFlow 2.1 and TensorFlow 2.2
For a  complete list of libraries and packages see list in myenv.yml, with conda 4.8.3. 

Tip: Once conda is installed, to set up conda environment run: “conda env create -f myenv.yml”


### HARDWARE:
The experiments were executed on a system with minimum configuration of:
OS: Ubuntu 16.04.6 LTS
CPU: Intel Xeon Silver 4110
GPU: 1x NVIDIA Titan Xp
Memory RAM: 8 GB
Storage: 22 GB



## GUIDE:
The sequence of execution is:
Data set preparation
+ 0. Socioeconomics: Export data from IBGE (Brazilian institute for geography and statistics) for the region in study
	IDHMS/IDHMS.ipynb
+ 2. Images Dataset - Export data from Google Street View for the region in study
			0. Run_crawler.sh
			1. StreetImagesCrawler.ipynb
			2. StreetImagesAnalysisPlots.ipynb
Running the Multimodal approach
+ 4. Multimodal
+ 3. Data Aggregation (1_DataAggregation.ipynb) - Prepare data files for use
+ 4. Image Feature (2_ImageFeatureExtraction.py) - This script uses VGG16 pre-trained network weights to extract vectors from each of the street level images used. 
+ 5. Train (3_Train.py)  - Train convolutional neural network models 
+ 6. Prediction (4_Predict.py) - Generate predictions for other images
+ 7. Plot Predictions (5_Plots.ipynb) - Plot charts with predictions and results from study


## REPRODUCIBILITY AND REPLICATION:
In order to reproduce and replicate this experiment, all data used are available.

All other information needed, such as seeds and flags, should be in codes. 





