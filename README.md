# Chest-XRay-Vision

Chest Xray image analysis using **Deep Transfer Learning technique** with **Pytorch**.

The maxpool-5 Layer pretrained **VGGNet-16 CNN model** via **Finetuning** the convnet with SGD optimizer and Batch Normalization for the classification of **Normal vs Opacity vs Cardiomegaly** 

**Fine Tuning** : Instead of random initializaion, we initialize the network with a pretrained network, like the one that is trained on imagenet 1000 dataset. Rest of the training looks as usual.

**Feature Extractor**(Option Field Created): where we will freeze the weights for all of the network except that of the final fully connected layer,which can be done setting up `feature_extract=True` in `set_require_grad` function .


## Data Set

[openi.nlm.nih.gov](openi.nlm.nih.gov) has a large base of Xray,MRI, CT scan images publically available.Specifically Chest Xray Images have been scraped, Normal and Nodule labbeled images are futher extrated for this task.


## Steps to follow
1.Go to import data folder – Download Data using this command in your CLI.

`python scraper.py <path/to/folder/to/save/images>`

This downloads the images and saves corresponding disease label in json format.

2.Now ,  the following  `Importdata/Making dataset-For three labels.ipynb` notebook for Data processing and generate 

* All images for training will be stored in Train Folder

* All images for testing will be stored in Test Folder 
   with  3 cateogries of each .

3.Finally , `Run the Vision_Transfer_Learning.ipynb`

**Accuracy : 71.4221%**
