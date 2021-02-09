# Prediction of different eye diseases based on fundus photography via deep transfer learning --Rrepository
This repository contains the code and data of the paper for research.
## Project Summary
Prediction of different eye diseases is a multi-class problem. The data form is the image of the retinal fundus. With transfer learning on a proper deep convolution network, we can predict from the small data set. This project is implemented by python on tensorflow framework.Check the paper for more details. This approach generates certainly satisfactory results, we present all the results, code, and reproduction guidance together here. 

## Model Structure
MobileNetV2 feature extractor: 

    Initial convolution layer, 
    
    1 depthwise convolution layer, 
    
    1 pointwise convolution layer,
    
    16 reversed residual blocks. 
   Implemented  from keras-tensorflow-applications. Pretrained on ImageNet.

Global average layer

Prediction layer

## Model Results

## Visulization

## Reproduction Guidance
All experiments are performed on Google Colab (Many thanks to Google!!).
# Data (optional)
We provide data in folder "Data". Download the Data 
