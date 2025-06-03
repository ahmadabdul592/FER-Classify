# Emotion Recognition using FER Dataset

This repository contains the code for the Arewa Data Science Capstone Project by Group 5, focusing on emotion recognition using ResNet architecture. This deep learning project is developed with PyTorch and aims to contribute to the critical field of affective computing and its many applications.



## Project Overview

In this project, we fine-tune a Resnet18 model on the [FER2013 dataset](https://www.kaggle.com/datasets/msambare/fer2013) on Kaggle to recognize one of seven emotions from static facial images: anger, disgust, fear, happiness, sadness, surprise, and neutral. The goal here is to explore techniques that can increase the accuracy of the model on the troublesome dataset.


## Team Members
- Samuel Gali
- Abdul Ahmed Abdul 
- Muhammad Saleh Ibrahim
- Zeera Baidu


## Dataset
The [FER2013 dataset](https://www.kaggle.com/datasets/msambare/fer2013) consists of two folders containing training and test data respectively. The data consists of 4x48 pixel grayscale images of faces. The faces have been automatically registered so that the face is more or less centered and occupies about the same amount of space in each image. There are 28,709 examples in the train folder and 3589 examples in the test set.

The dataset does not include a validation set that can be used in training, so we create that ourselves, taking care to ensure that the validation set correctly represents the training set by performing a stratified split using a custom function.


## Methodology

The project utilizes a Resnet18 architecture initialized with the default pre-trained weights. The final fully connected layer is replaced with two hidden layers and one output layer to increase variance. The base layers are not frozen to allow for proper fine-tuning given the unfamiliarity of the pre-trained model with classifying emotions.

## Results

The model achieved a final test accuracy of 70%. Training and validation accuracy and losses are documented through graphs on Wandb, showcasing the learning progress and model convergence. The project paper further explains the results.

## Deployment

The model is deployed to Huggingface and is ready for user interaction and testing. You can now take a picture of your or someone else's face, upload to the platform, and have the model classify your expression instantly. Check it out [here](https://huggingface.co/spaces/lazymonster/facial-emotion-recognition). The video demo can be found here.

## Acknowledgements

We extend our gratitude to the Arewa Data Science Academy, most especially our able mentor [Mr Mustapha Abdullahi](https://www.mustaphaabdullahi.com/) and [Dr Shamsuddeen H Muhammad](https://shmuhammadd.github.io/). Special thanks to our mentors and peers for their valuable guidance and feedback.