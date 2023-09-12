# Cassava-Leaf-Disease-Classification

This is a three-month project in a course called 'Machine Learning Project'. The theme of the project was from a Kaggle competition - 'Cassava Leaf Disease Classification'. This repository contains Code and report of this project. Two people were involed in this project. I most participated in the Neural Network Development, training and testing in the code development part, and report writing part.

## Background of the Cassava-Leaf-Disease-Classification project

Cassava, which is a popular kind of crop in Africa. It could be used in many areas and withstand harsh farming conditions. However, there are some types of diseases that make poor harvest. To cope with this problem, we need to identify the type of cassava disease and remedy it. Nowadays, image classification techniques could be applied to help identify cassava disease. Recently, using image classification to detect cassava disease has been attached great importance as a Kaggle competition. 


## Dataset

The dataset we used was the dataset provided by the Kaggle competition [Cassava Leaf Disease Dataset](https://www.kaggle.com/c/cassava-leaf-disease-classification/data)

## Preprocessing of the dataset

We deployed data augmentation techniques to help mitigate overfitting. Some functions provided in the **Albumentations** library were applied. 

Asequence of data augmentation methods is implemented sequentially for each image. For each input image, a region with a specified size is cropped randomly within the original image. Then for the cropped image, **transpose**, **flip operations**, **rotate**, and **normalize** are implemented to make training images various, which could enhance the generalization ability of a model.


## The design of our classification model

First, we trained several common single-type deep neural networks including **ResNet**, **DenseNet**, **ResNext**, **EfficientNet B3** and **Vision Transformer**. 

Then based on their performance, we did ensembling classification using models with the top three highest validation accuracy. It shows that ensembling model performs much better than single-type models. 

Based on the ensembling model, we also investigated several **generalization and regularization** methods including **Fmix**, however, experiment results show that these methods fail to improve the validation performance.
