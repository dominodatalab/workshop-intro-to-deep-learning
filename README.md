## Project Contents:
* `download-data-supplement` folder - contains the code and files for downloading the images and processing the annotations
* `1-Data-Prep.ipynb` notebook - code for cleaning data
* `2-Load-Data-PyTorch.ipynb` notebook - code for loading and visualizing data in PyTorch
* `3-Build-Model.ipynb` - build and train model
* `4-Improve-Performance.ipynb` - improve training speed
* `5-Hyperparameters-Tuning.ipynb` -improve training accuracy


## Project Resources:
* Data location - https://www.zooniverse.org/projects/zooniverse/snapshot-serengeti
* Article - https://www.pnas.org/content/115/25/E5716
* Article code - https://github.com/Evolving-AI-Lab/deep_learning_for_camera_trap_images


## Summary:

This tutorial is a chance to get hands-on with PyTorch and GPU Deep Learning (DL). It is specifically targeted toward attendees who may be familiar with the concepts of DL, but want practical experience. Familiarity with Python and typical ML packages (e.g. pandas, numpy, sklearn) is expected.

At the end of this session, you will understand how to:
* Build some common DL architectures in PyTorch
* Evaluate and improve the performance of DL models
* Take advantage of more compute (and when you should do so)

This will set you up to take advantage of interesting developments in the field and maybe even contribute your own!


## Tutorial Outline:

Introduction and Data Preparation 
* Real-world examples
* When to use Deep Learning
* PyTorch overview
* Forward and back propagation
* Weights and biases
* Types of networks - CNN, RNN, and more

Activity: Load and prep data, Explore transforms

Deep Learning in Practice  
* Input, output, and hidden layers
* CNN hidden layers - convolutional layers, ReLU layers, pooling layers, fully connected layers
* Cost functions
* Cross entropy

Activity: Build CNN architecture and train model

Optimizing Models 
* Parameters - epochs, learning rate, etc
* Overview of different optimizers
* Image augmentation
* Hyperparameter tuning

Activity: Speed up Model Training, Explore hyperparameter tuning

 
