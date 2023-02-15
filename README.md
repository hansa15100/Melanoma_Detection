# Melanoma Detection

## Table of Contents
* [Problem Statement](#problem-statement)
* [General Information](#general-information)
* [Steps Performed](#steps-performed)
* [Result and Findings](#result-and-findings)
* [Conclusions](#conclusions)


## Problem Statement

To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

## General Information
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:
Actinic keratosis Basal cell carcinoma Dermatofibroma Melanoma Nevus Pigmented benign keratosis Seborrheic keratosis Squamous cell carcinoma Vascular lesion.

<img width="638" alt="Screenshot 2023-02-15 at 10 26 37 PM" src="https://user-images.githubusercontent.com/35450500/219108694-aa3f5a5f-377e-431b-83ce-4c1e22d5d94e.png">

## Steps performed 
1. Understanding the data.
2. Create train & validation datasetwith batch size of 32 with resizing images to 180*180.
3. Perform Data Visualization
4. Build model while scaling image to normalize pixel value between (0,1).
5. Choose loss function and optimizer for model training and train it for 20 epochs.
6. check whether the model underfit or overfit.


## Result and Findings
 - Initial Basic Model with 4 layers, No Dropout(Only after dense layer) with original data.
 <img width="538" alt="Screenshot 2023-02-15 at 10 35 38 PM" src="https://user-images.githubusercontent.com/35450500/219104982-e854ed29-22d2-4010-9f0d-4740cd8b2b11.png">
 
 - Model metrics after applying tf.image augmentation layers.
 
 
 <img width="538" alt="Screenshot 2023-02-15 at 10 41 37 PM" src="https://user-images.githubusercontent.com/35450500/219105217-604e13d4-a2aa-46f2-ba59-0e01982cacb1.png">
 

 - Data Imbalance:
 
1. seborrheic keratosis has the least number of samples.
2. igmented benign keratosis and melanoma dominate the data in terms of proportion.


  - Model metrics after using Augmentor Library.
  
  <img width="563" alt="Screenshot 2023-02-15 at 11 33 00 PM" src="https://user-images.githubusercontent.com/35450500/219115250-3b9d82fc-2424-4a63-a202-945a30b50737.png">


## Conclusions
- Intial Model with original dataset seems to be Overfitting with training accuracy 85%(could go upto 95 after removing dropout after dense layer and validation accuracy 58%.
- Next model with same complexity just with augmented data looks like underfitting case with train accuracy:60% and validation accuracy 53%
- Last model after treating model with data imbalance and using Augmentor library looks fine with training accuracy 83% and validation accuracy 79%.




<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
