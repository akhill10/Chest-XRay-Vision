# Chest-XRay-Vision

Chest Xray image analysis using Deep Transfer Learning technique for it with Pytorch.
The maxpool-5 Layer pretrained VGGNet-16 CNN model via Finetuning the convnet with SGD optimizer and Batch Normalization for the classification of Normal vs Opacity vs Cardiomegaly. 
Fine Tuning : Instead of random initializaion, we initialize the network with a pretrained network, like the one that is trained on imagenet 1000 dataset. Rest of the training looks as usual.
Also created a an option of Feature Extractor: where we will freeze the weights for all of the network except that of the final fully connected layer.
