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

#### figure of structure
![image](https://github.com/gcowen/fundusimageclassification/blob/master/IMG/Stucture2.jpg)

## Model Results
Confusion Matrix

![image](https://github.com/gcowen/fundusimageclassification/blob/master/IMG/Picture2.png)

0: Normal, 1: Glaucoma, 2: Pathological Myopia 3: Maculopathy, 4: Retinitis Pigmentosa
## Visulization
![image](https://github.com/gcowen/fundusimageclassification/blob/master/IMG/Picture1.png)

A: Normal, B: Glaucoma, C: Pathological Myopia D: Maculopathy, F: Retinitis Pigmentosa
Mis-classified image are marked in red. The first is mis-classified as glaucoma, the second is misclassified as maculopathy.
## Reproduction Guidance
All experiments are performed on Google Colab (Many thanks to Google!!).
### Data 
We provide data in folder "**Data**". Download the Data folder then upload the sub-folder "**HIGHMIDCHANCEGLAUMYOPIAmaculopathyRP**" to Google Drive.

For customized data, please follow the structure of the data set folder, you may need to change the script for different number of class. 
### Codes
All the raw results are avillable in **Codes** folder.
#### file discription
`ModelAndResults.ipynb` the model in this project.

`Fundus5Runs.ipynb` Comparision with other models.

`binarys` Binary classifier for each disease.




#### rerun the code
Upload the nodebook or use the code to Colab then connect it to Google drive.

Rerun the cells for results.

*Note: the confusion matrix cell can be ran either before the fine-tune for after the fine-tune.*
