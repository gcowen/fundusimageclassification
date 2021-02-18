# Prediction of different eye diseases based on fundus photography via deep transfer learning
This repository contains the code and data used in the paper.
## Project Summary
We propose to utilize a lightweight deep learning architecture called MobileNetV2 and transfer learning to distinguish four common eye diseases including Glaucoma, Maculopathy, Pathological Myopia, and Retinitis Pigmentosa from normal controls using a small training data. The inputs to the algorithm are fundus images. This project was implemented using the tensorflow framework. We include code and data here for each reproduction of the results in the paper.  

## Reproduction Guidance
All experiments are performed on Google Research Colab (Many thanks to Google!!).

### Data 
All data can be found in folder "**Dataset**". Download the Data folder then upload the sub-folder "**HIGHMIDCHANCEGLAUMYOPIAmaculopathyRP**" to Google Drive.

For users own data, please follow the structure of the data set folder. You may need to change the script for different number of classes. 

### Codes
All implementation code, including intermediate and final results, can be found in **Codes** folder.

#### file discription
`ModelAndResults.ipynb` the model in this project.

`Fundus5Runs.ipynb` Comparision with other models.

`binarys` Binary classifier for each disease.




#### rerun the code
Upload the nodebook or use the code to Colab then connect it to Google drive.

Rerun the cells for results.

*Note: the confusion matrix cell can be ran either before the fine-tune for after the fine-tune.*

## Main methods
Freeze the convolution layers and train on the fundus image data set.
Unfreeze the last two layers and fine-tune.
### Structure
[MobileNetV2](https://ieeexplore.ieee.org/document/8578572) feature extractor: 

    Initial convolution layer, 
    17 reversed residual blocks,
    1 poinwised convolution layer.
   Implemented  from [keras-tensorflow-applications](https://www.tensorflow.org/api_docs/python/tf/keras/applications/MobileNetV2). Pretrained on ImageNet.

Global average layer

Prediction layer



#### figure of structure
![image](https://github.com/gcowen/fundusimageclassification/blob/master/IMG/Stucture2.jpg)
[Tool](https://github.com/HarisIqbal88/PlotNeuralNet)

## Model Results
Confusion Matrix

![image](https://github.com/gcowen/fundusimageclassification/blob/master/IMG/Picture2.png)

0: Normal, 1: Glaucoma, 2: Pathological Myopia 3: Maculopathy, 4: Retinitis Pigmentosa
## Visulization
visualization using [Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization](https://ieeexplore.ieee.org/document/8237336)
![image](https://github.com/gcowen/fundusimageclassification/blob/master/IMG/Picture1.png)

A: Normal, B: Glaucoma, C: Pathological Myopia D: Maculopathy, F: Retinitis Pigmentosa.
Mis-classified image are marked in red. The first is mis-classified as glaucoma, the second is misclassified as maculopathy.

# Citations
see paper
