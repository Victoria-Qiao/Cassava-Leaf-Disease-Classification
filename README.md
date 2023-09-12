# Cassava-Leaf-Disease-Classification

This is a three-month project in a course called 'Machine Learning Project'. The theme of the project was from a Kaggle competition - 'Cassava Leaf Disease Classification'. This repository contains Code and report of this project. Two people were involed in this project. I most participated in the Neural Network Development, training and testing in the code development part, and report writing part.

## Background of the Cassava project：
Cassava, which is a popular kind of crop in Africa. It could be used in many areas and withstand harsh farming conditions. However, there are some types of diseases that make poor harvest. To cope with this problem, we need to identify the type of cassava disease and remedy it. Nowadays, image classification techniques could be applied to help identify cassava disease. Recently, using image classification to detect cassava disease has been attached great importance as a Kaggle competition. 

We selected this topic as our project, in which, firstly we tried several common single-type deep neural networks including ResNet, DenseNet, ResNext, EfficientNet B3 and Vision Transformer. Then based on their performance, we did ensembling classification using models with the top three highest validation accuracy. It shows that ensembling model performs much better than single-type models. Based on the ensembling model, we also investigated several generalization and regularization methods in- cluding Fmix, however, experiment results show that these methods fail to improve the validation performance.
