
# Capstone Project:  Facial Emotion Recognition in Real-Time


Emotion AI is a subset of artificial intelligence (the broad term for machines replicating the way humans think) that measures, understands, simulates, and reacts to human emotions.

One of the technologies available to analyse facial expressions is using Computer Vision. This technology often uses convolutional neural networks in which the models are trained to detect a combination of emotional states based on both facial landmark and muscle movement detection. This analysis can be augmented with body posture and movement analysis.

In this project, we will explore the basics of convolutional neural networks and understand how we can utilise existing models to create one that can possibly be a minimum viable product to detect facial emotions in real-time. 
## Problem Statement


This project aims to create a model that can **accurately distinguish emotions based on facial expressions**.
I conducted transfer learning using existing models: ResNet-50, MobileNetV2, VGG16 and VGGFace. The models are evaluated based on the **test accuracy scores** (the higher, the better).

Subsequently, the best model is deployed using OpenCV, with real-time application on a laptop with integrated webcam. 


## Data

I used the FER2013 dataset, available on [Kaggle](https://www.kaggle.com/datasets/msambare/fer2013).  

* The data consists of 48x48 pixel grayscale images of faces. 
* The faces have been automatically registered so that the face is more or less centred and occupies about the same amount of space in each image.
* The images have been labelled into one of seven emotion categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral). 
* The training set consists of 28,709 images and the test set consists of 3,589 images.

**Note:**
* For this project, I have excluded 'neutral' and 'disgust' emotion classes. 
* There is a severe lack of examples for 'disgust' which will lead to  a class imbalance problem.
* As I am more interested to capture 'active' emotions i.e. positive (happy or surprise) or negative (fear, angry, sad), I find that it is not meaningful to identify 'neutral' emotion. 

As the dataset is huge, I am unable to upload it to this GitHub repository. A copy of the dataset can be downloaded from [this Google Drive folder](https://drive.google.com/drive/folders/1uFzQ4Utxr4xkAP813q-IA2becU13OPmr?usp=sharing).
## Structure

To organise my work better, I have organised this project into two notebooks, across six parts: 

**Notebook 1:** 
* Part 1 : Data Import
* Part 2: Exploratory Data Analysis

**Notebook 2:**
* Part 3: Data Preprocessing
* Part 4: Baseline Model: A CNN model built from scratch
* Part 5: Transfer Learning & Model Evaluation

**Notebook 3:**
* Part 6: Model Deployment

## Summary of Analysis

As shown in the table below, transfer learning on **VGGFace model with finetuning applied across all layers** produced the best test accuracy score:

| Model | Train Accuracy | Val Accuracy | Delta | Test Accuracy | Evaluation|
| :-: | :-: | :-: | :-:|:-:|:-:|
| VGGFace Model (Finetuned all layers) |0.9786| 0.7629|(0.2157)| 0.7494| 1st|
| MobileNetV2 Model (Finetuned all layers) |0.8247| 0.6857|(0.1390)| 0.6823| 2nd|
| VGG16 Model (Finetuned all layers) |0.9971| 0.6930|(0.3041)| 0.6808| 3rd|
| ResNet50 Model (Finetuned all layers) |0.9219| 0.6492|(0.2727)| 0.6530| 4th|
| Baseline - Custom CNN Model | 0.5796| 0.5792|(0.0004)| 0.5817| Baseline|

However, in terms of speed of training, it is observed that **VGGFace model took the longest time** (~ 250s per epoch) as compared to the other models: VGG16 (~ 110s per epoch), MobileNetV2 (~ 140s per epoch) and ResNet50 (~30s per epoch). 

A copy of the finetuned VGGFace model can be downloaded [here](https://drive.google.com/file/d/10BI99L0cYWXMW9niWWdqMLHOgzpieIXW/view?usp=sharing).



   

## Conclusions & Recommendations

While this project has shown the possibilities of using convolutional neural networks to accurately distinguish emotions based on facial expressions, 
the application of it in the law enforcement and public safety context is still at an infancy stage as there are ethical issues that have yet to be addressed. 




**Recommendations**

* To perform transfer learning on other datasets if can be acquired e.g. [AffectNet](http://mohammadmahoor.com/affectnet/), [JAFFE](https://zenodo.org/record/3451524).
* To attempt machine learning techniques on emotion classification by extracting facial landmark features that can distinguish emotions. 
* To explore combining facial emotion recognition with speech emotion recognition since this will be more useful in a real-time interview setting. 