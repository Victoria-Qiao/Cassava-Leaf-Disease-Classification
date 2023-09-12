# Cassava-Leaf-Disease-Classification

This is a three-month project in a course called 'Machine Learning Project'. The theme of the project was from a Kaggle competition - 'Cassava Leaf Disease Classification'. This repository contains Code and report of this project. Two people were involed in this project. I most participated in the Neural Network Development, training and testing code development, and report writing parts.

## 1. Background of the Cassava-Leaf-Disease-Classification project

Cassava, which is a popular kind of crop in Africa. It could be used in many areas and withstand harsh farming conditions. However, there are some types of diseases that make poor harvest. To cope with this problem, we need to identify the type of cassava disease and remedy it. Nowadays, image classification techniques could be applied to help identify cassava disease. Recently, using image classification to detect cassava disease has been attached great importance as a Kaggle competition. 


## 2. Dataset

The dataset we used was the dataset provided by the Kaggle competition [Cassava Leaf Disease Dataset](https://www.kaggle.com/c/cassava-leaf-disease-classification/data)

## 3. Preprocessing of the dataset

We deployed data augmentation techniques to help mitigate overfitting. Some functions provided in the [Albumentations]([https://www.kaggle.com/c/cassava-leaf-disease-classification/data](https://github.com/albumentations-team/albumentations)) library were applied. 

A sequence of data augmentation methods is implemented sequentially for each image. For each input image, a region with a specified size is cropped randomly within the original image. Then for the cropped image, **transpose**, **flip operations**, **rotate**, and **normalize** are implemented to make training images various, which could enhance the generalization ability of a model.


## 4. The design of our classification model

First, we trained several common single-type deep neural networks including **ResNet**, **DenseNet**, **ResNext**, **EfficientNet B3** and **Vision Transformer**. 

Then based on their performance, we did ensembling classification using models with the top three highest validation accuracy. It shows that ensembling model performs much better than single-type models. 

Based on the ensembling model, we also investigated several **generalization and regularization** methods including **Fmix** and **Test time Augmentation**, however, experiment results show that these methods fail to improve the validation performance. Finally, we applied **weighted average** of the predict scores from the top three classifiers as the final outcome.

## 5. What I learned from this project

1) Larned many image pre-processing techniques, to increase the variety of data.
2) Got to know many convolutional neural networks and their structures, as well as ensembling of different models to do classification.
