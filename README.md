# Computer-Artifact
This repository contains the computer artifact for my comprehensive exam. 
I have already integrated the datasets within the code of the files
It pretty simple to run the files yourself , but beware that it might take some training time when the model retrains itself.
The computer artifacts are based on the CNN-RNN and DeepLabV3 models which are used in the paper " Automatic Detection of Congestive Heart Failure Based on a Hybrid Deep Learning Algorithm in the Internet of Medical Things " and " High-Throughput Precision Phenotyping of Left Ventricular Hypertrophy
With Cardiovascular Deep Learning " respectively. These Models were used and modified a bit so that it works with the PneumoniaMNIST and BreastMNIST dataset. DeepLabv3 was adapted for classification tasks, using segmentation features to improve performance. CNN-RNN hybrid model was used in both datasets, despite their lack of temporal data.

# Medical Image Classification with CNN-RNN and DeepLabv3 Models

This repository contains code for training and evaluating two deep learning models—**CNN-RNN Hybrid** and **Modified DeepLabv3**—on medical imaging datasets. The models are tested on two datasets, **PneumoniaMNIST** and **BreastMNIST**, to classify medical images and demonstrate model performance.

## Table of Contents
- [Overview](#overview)
- [Datasets](#datasets)
- [Models](#models)
  - [CNN-RNN Hybrid Model](#cnn-rnn-hybrid-model)
  - [Modified DeepLabv3 Model](#modified-deeplabv3-model)
- [Installation](#installation)
- [Usage](#usage)
  - [Training and Evaluation](#training-and-evaluation)
- [Results](#results)
- [Acknowledgments](#acknowledgments)

## Overview
This project explores the use of hybrid deep learning architectures for medical image classification. The CNN-RNN model leverages convolutional layers for feature extraction and an LSTM for sequential processing, while the DeepLabv3 model has been modified with a ResNet-based encoder to perform image classification.

## Datasets
The models are tested on two datasets:
1. **PneumoniaMNIST**: A dataset of chest X-ray images to classify pneumonia cases.
2. **BreastMNIST**: A dataset of breast ultrasound images for classifying benign or malignant cases.

Both datasets are part of the **MedMNIST** collection and can be installed and accessed via the `medmnist` Python library.

## Models

### CNN-RNN Hybrid Model
The CNN-RNN model combines convolutional layers for spatial feature extraction and an LSTM layer to capture sequential dependencies within the feature maps. It is used for binary classification with the following architecture:
- Convolutional layers with ReLU activation and max pooling
- LSTM layer for sequential feature processing
- Fully connected output layer

### Modified DeepLabv3 Model
This model utilizes a ResNet-based encoder without ASPP (Atrous Spatial Pyramid Pooling), adapted for classification instead of segmentation. Key components:
- ResNet encoder with convolutional and bottleneck layers
- Global average pooling to capture feature representation
- Fully connected layer for classification

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/medical-image-classification.git
   cd medical-image-classification  

## Results
Model performance on each dataset is evaluated using metrics such as accuracy, F1-score, recall, precision, and confusion matrix.

## Acknowledgments
1. MedMNIST for providing accessible medical image datasets for research.
2. PyTorch for deep learning frameworks.
