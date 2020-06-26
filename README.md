# Image Processing of Plant Pathology - DSI7 Capstone Project


## Table of Contents

* [Introduction](#introduction)
* [ Competition Specific Objectives](#competition-specific-objectives)
* [Data Description](#data-description)
* [Modeling](#modeling)


## Introduction 

For our capstone project we choose Kaggle competition for Plant Pathology to Identify the category of foliar diseases in apple trees. The challenge In this competition is to diagnose plant diseases based on leaf images. 
Solving this problem is very important because diagnosing plant diseases early can save a lot of agricultural products every year. This will benefit the farmers by ensuring they get the harvest they deserve.

competition link : [Plant Pathology!](https://www.kaggle.com/c/plant-pathology-2020-fgvc7/data)

## Competition Specific Objectives

Train a model using images of training dataset to classify a given image from testing dataset into different diseased category or a healthy leaf.

## Data Description

Data include **1821** train images and **1821** test images, in jpg format, with high resolution.
train data has 4 classes :

* healthy : 28.3%
* rust : 34.2%
* scab : 32.5%
* multiple_diseases : 5%

We notice that data contain unbalance classes where Rust was the most frequent class with **622** images, and multiple diseases was the least frequent class with only **91** images. 
Since 91 images is small to train a model, we decide to do over sampling using ImageDataGenerator to increase train data by image augmentation for random selected images for each class to increase the dataset. in result we had **2489** images in total and **622** images for each class.

## Modeling

For modeling, we build CNN model and DenseNet model.
Both models gave us close scores on Kaggle but different in running time. 
For first model the CNN model, it give us an accuracy of 0.80 in 6h. Second model we work on is DenesNet and it give us a 0.82 accuracy. 
Submissions on kaggle are evaluated by ROC AUC.

Model | Kaggle score | run time
------------ | ------------- | -------------
CNN model | 0.803 | 6 hours to run
DenseNet model | 0.819 | 7.5 hours to run

Team members: Hanin Almarshad - Reem Alghamdi - Ahmad Fatani 
