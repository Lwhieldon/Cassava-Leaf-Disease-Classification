# Cassava Leaf Disease Classification
Using Machine Learning Algorithms to Identify the Type of Disease Present on a Cassava Leaf Image

<p align="center">
<img src="https://github.com/Lwhieldon/Cassava-Leaf-Disease-Classification/blob/master/images/220px-Manihot_esculenta_-_K%C3%B6hler%E2%80%93s_Medizinal-Pflanzen-090.jpg?raw=true" width="200" height="200" />
</p>

## Abstract

Cassava plants are a key food security crop grown by local farmers in Africa due to the plant's ability to withstand harsh outdoor elements. When Cassava plants incur disease, it can devastate a local farmer's crops and income that drastically affects their source of food and quality of life. As a data scientist, I have been tasked with helping to identify 4 different types of viral diseases from healthy plants on plant images in an attempt to expedite disease identification and mitigate local African farmer's poor crop yields.

In this project, I have ~20k images that I will train a disease classification model using a convultional neural network with an accuracy score higher than ~61%. By applying transfer learning using EfficientNetB architecture, I yield an accuracy score of 85% in our model to detect different types of disease or healthy plants.

For future work, I would like to enhance the CNN by applying Test Time Augmentation; I would also like to see how well the model performs on larger image files, increase the resolution up to 448x448x3.
## Goals

This repo is part of the work completed within UMBC's DATA602 Course: Intro to Data Analysis and Machine Learning.

In this project, I attempt to achieve the following:
<ol>
<li><b>Exploration of Cassava Disease Images:</b> Examine the images tagged to each Cassava Leaf Disease Type </li>
<li><b>Image Preprocessing of Cassava Leaf Images: </b>Apply image preprocessing to augment the images in our dataset, as this will help us create a solid model. Additionally, will break out dataset into training & validation groups.</li>
<li><b>Train Convolutional Neural Network:</b> Applying transfer learning, using EfficientNetB architecture </li>
<li><b>Loss & Accuracy Analysis on CNN:</b> Analysis of both training & validation loss and accuracy. </li>
<li><b>Recommendations and Future Work:</b> Provide initial conclusions on project and recommend future work to enhance the model </li>
</ol>

## Overview and Background

Cassava plants are a key food security crop grown by local farmers in Africa due to the plant's ability to withstand harsh outdoor elements. As the second-largest provider of carbohydrates in Africa and at least 80% of household farms in Sub-Saharan Africa grow this starchy root, I (as a data scientist) have been tasked with helping to identify viral diseases on the plants as this is a major reason of poor crop yields.

As it stands today, if farmers require help to detect disease within their crops, they must go through an arduous task of soliciting the help of government-funded agricultural experts, leading to delays in assessing crop damage and risk of destroying their entire crop base due to the spread of disease. As an added challenge, any image detection solution must perform well under low quality images, since African farmers may only have access to mobile-quality cameras with low-bandwidth.

I am now tasked to classify each cassava image into four disease categories or a fifth category indicating a healthy leaf. With my help, farmers may be able to quickly identify diseased plants, potentially saving their crops before they inflict irreparable damage.

In this project, we will train a convultional neural network that must have an accuracy score higher than ~61%. We demonstrate that by utilizing transfer learning, applying an EfficientNetB architecture, we yield an accuracy score of 85% in our model.

<p align="center">
<img src="https://github.com/Lwhieldon/Cassava-Leaf-Disease-Classification/blob/master/images/cassavafarmer.jpg?raw=true" height="200" />
</p>

## Data Details

<a href=https://www.kaggle.com/c/cassava-leaf-disease-classification>Kaggle Cassava Leaf Disease Detection Competition</a>

The dataset is part of an active competition as of December 2020; note the competition will end February 2021. The competition introduces a dataset of 21,367 labeled images collected during a regular survey in Uganda. Most images were crowdsourced from farmers taking photos of their gardens, and annotated by experts at the National Crops Resources Research Institute (NaCRRI) in collaboration with the AI lab at Makerere University, Kampala. The image format and documentation within the competition most realistically represents what farmers would need to diagnose in real life.

Each Cassave leaf image is identified as:
<ul>
<li>Cassava Bacterial Blight (CBB)</li>
<li>Cassava Brown Streak Disease (CBSD)</li> 
<li>Cassava Green Mottle (CGM)</li> 
<li>Cassava Mosaic Disease (CMD)</li>
<li>Healthy</li>
</ul>

Below are examples of each image class as a reference:

<style>
.cassava{
 max-width: 100%;
 max-height: 200%
}
</style>
<img src="https://github.com/Lwhieldon/Cassava-Leaf-Disease-Classification/blob/master/images/sample_images.png?raw=true" class="cassava" alt="Cassava Leave Examples">


Since the dataset is too large to import into a Github repo, we will not be uploading images to this project. We will be referencing local copies of the files provided by Kaggle competition, including the following:

<ul>
<li><b>test_images:</b> A single sample image used to validate the model's prediction accuracy. Since this is an open competition, Kaggle has not provided us a full test image dataset, so we will use this single image to test the accuracy of our model.</li>
<li><b>train_images:</b> ~20k training images to help train the CNN</li> 
<li><b>label_num_to_disease_map.json</b>: Provides a key value pair to tie the label to the appropriate disease/healthy classification tag.</li> 
<li><b>train.csv:</b> tabular file associating training images to disease/healthy classification label</li>
</ul>

## Outcomes and Conclusions of this Study

We preprocessed our training images using ImageDataGenerator and performed a validation split where 20% of our images test the model; 80% of images train our model. We also augment our images by horizontal flips, vertical flips, shifts in ranges, and rotations. 

After our images are preprocessed, we then create a CNN by first applying transfer learning, importing the EfficientNetB4 architecture, and then adding a GlobalAveragePooling2D() and Dense layers to denote the 5 image classifications. Note our batch size is 16, 10 epochs, and the target size of the images is 299x299x3. Our steps per epoch & validation are separated like our training & testing images (20-80 split) and the CNN takes approximately ~50 minutes to run.

We also apply callbacks to make sure our model can stop and reduce learning speed when the model does not improve its validation loss. We also tell our model in a call to save the model when the model validation loss improves so we have the best model available for future fine tuning.

After completing 10 epochs, the models finishes with a validation loss of 39.9% and a validation accuracy of 85%. I used Tensorboard to provide a visual representation on the accuracy and loss per each epoch. Below are line graphs representing the test & validation accuracy and loss at each epoch:


<p align="center">
<b>Train & Validation Loss</b>
<img src="https://github.com/Lwhieldon/Cassava-Leaf-Disease-Classification/blob/master/images/epoch_loss.jpg?raw=true"/>
*Note: Train line = Orange; Validation line = Blue
</p>

<p align="center">
<b>Train & Validation Accuracy</b>
<img src="https://github.com/Lwhieldon/Cassava-Leaf-Disease-Classification/blob/master/images/epoch_acc.jpg?raw=true"/>
*Note: Train line = Orange; Validation line = Blue
</p>

## Table of Contents

This assignment contains the following areas:

<ol>
  <li><a href=>Summary and Report</a>: Jupyter Notebook including a detailed abstract on problems in assignment, code relevant to project, and visualizations supporting the completion of the project. </li>
  <li> <a href=>Code:</a> Area to perform testing of dataset, functions, and implement models before final project output. </li>
</ol>

<br>
<pre>
Contributors : <a href=https://github.com/Lwhieldon>Lee Whieldon</a>
</pre>

<pre>
Languages    : Python
Tools/IDE    : Anaconda
Libraries    : pandas, numpy, matplotlib, seaborn, sklearn
</pre>

<pre>
Assignment Submitted     : December 2020
</pre>

