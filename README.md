# CRCV_A1
#### Training with CIFAR100

## Introduction
This is my first attempt at machine learning using Keras. I had the model learn from CIFAR100, which is a subset of the Tiny Images dataset and consists of 60000 32x32 color images. The 100 classes in the CIFAR-100 are grouped into 20 super classes. There are 600 images per class. Each image comes with a "fine" label (the class to which it belongs) and a "coarse" label (the superclass to which it belongs). There are 500 training images and 100 testing images per class.
Source: https://www.cs.toronto.edu/~kriz/cifar.html

## Method
Data preprocessing: Normalize pixel values using mean and standard deviation, and split data into training and validation sets.
Model architecture: Convolutional Neural Network (CNN) - sequential convolutional model
Hyperparameters: I used a learning rate scheduler to reduce the learning rate as more epochs were done to help with training. I had a batch size of 128, and for my first run, I did 200 epochs on my laptop overnight.
Training process: I trained the model using data augmentation, early stopping, learning rate decay, and freezing certain layers after obtaining the first set of model weights.
Data augmentation techniques: I had a few set out, but the ones I used were randomly rotating the image, shifting the images horizontally and vertically, and flipping the images horizontally.

## Results
Test loss: 1.90
Test accuracy: 0.50

Confusion Matrix: | True Positives: 69 | True Negatives: 69 | False Negatives: 2 | False Positives: 0 |  

## Analysis/Conclusion
My first model was way heftier than the second. 
The model.fit took longer when I used my data augmentation flow. Getting the colors on the photos to work after normalization was trickier than I had first imagined, as the values were outside RGB.
I had some issues getting Git to work on my first project. I ended up cloning a GitHub repo I made and putting my files there.
Tensorboard was not showing without deleting its temp data.
Overall, I learned a ton about using Keras and how each step is crucial to creating an environment for the model to succeed!

## Sources
iamssr02 / CIFAR-100-Classification-using-Custom-Model
https://github.com/iamssr02/CIFAR-100-Classification-using-Custom-Model/blob/main/CIFAR_100_Classification_NN_Project.ipynb

geifmany / cifar-vgg
https://github.com/geifmany/cifar-vgg

Introduced by Krizhevsky et al. in Learning multiple layers of features from tiny images
https://www.cs.toronto.edu/~kriz/cifar.html
