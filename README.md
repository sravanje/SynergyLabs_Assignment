# SynergyLabs_Assignment

## Problem:    

Transfer learning:  
Deep Learning is awesome, it has given wings to computer vision and object
detection/classification. However you need a lot of data to train a good detection model
which may not be readily available. Show use the use of transfer learning to train a model on
less data (<1000 images) and still getting good results (>80% accuracy) to demonstrate use
of transfer learning. You are free to pick a model of your choice and dataset of your choice.
(just don’t pick dataset which is already used in initial training)

What to submit:
a. Source code of your python script (either in email or link to your github repo)
b. List of websites/articles which you found helpful while doing your search
c. A small writeup

## Solution:  

### Choosen network for Transfer Learning:  
VGG16

### Choosen dataset:  
[Intel Image Classification][https://www.kaggle.com/puneet6060/intel-image-classification]  
This dataset contains images of Natural Scenes around the world and is contains the following classes:  
buildings, forest, glacier, mountain, sea, street  

I chose to work on binary classification with the classes glacier and mountain for the following reasons:  
1. Since the problem statement asked to use about 1000 images, multi-class classfication with 6 classes would be difficult.
2. Out of all these classes, the classes glacier and mountain seemed to contain the most similar images. If the model still performs well, it would make the capabalities of transfer learning apparent.  

### Some examples of images from this dataset:  

#### Glacier  
![alt text](https://github.com/sravanje/SynergyLabs_Assignment/blob/Datasets/main/glacier/20111.jpg?raw=true "Glacier Example")
![alt text](https://github.com/sravanje/SynergyLabs_Assignment/blob/Datasets/main/glacier/20059.jpg?raw=true "Glacier Example")
![alt text](https://github.com/sravanje/SynergyLabs_Assignment/blob/Datasets/main/glacier/20164.jpg?raw=true "Glacier Example")  

#### Mountain
![alt text](https://github.com/sravanje/SynergyLabs_Assignment/blob/Datasets/main/mountain/20107.jpg?raw=true "Mountain Example")
![alt text](https://github.com/sravanje/SynergyLabs_Assignment/blob/Datasets/main/mountain/20181.jpg?raw=true "Mountain Example")
![alt text](https://github.com/sravanje/SynergyLabs_Assignment/blob/Datasets/main/mountain/20144.jpg?raw=true "Mountain Example")  

### Results of the model trained:  
The model was trained with the crossentropy loss, adam optimiser and for 5 epochs.  
Here are the accuracy and loss plots for the same:  

#### Accuracy:  
Final training accuracy: 91.59%  
Final validation accuracy: 80.30%  
![alt text](https://github.com/sravanje/SynergyLabs_Assignment/blob/acc.png?raw=true "Accuracies")

#### Loss:  
Final training loss: 0.1983  
Final validation loss: 0.8131
![alt text](https://github.com/sravanje/SynergyLabs_Assignment/blob/loss.png?raw=true "Losses")


We see here that the model performs pretty well with just 5 epochs. The performance could be much better with more number of epochs and fine tuning.
