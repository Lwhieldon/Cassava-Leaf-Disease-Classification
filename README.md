# Cassava Leaf Disease Classification
Using Machine Learning Algorithms to Identify the Type of Disease Present on a Cassava Leaf Image

<p align="center">
<img src="https://github.com/Lwhieldon/Cassava-Leaf-Disease-Classification/blob/master/images/220px-Manihot_esculenta_-_K%C3%B6hler%E2%80%93s_Medizinal-Pflanzen-090.jpg?raw=true" width="200" height="200" />
</p>

## Overview

Cassava plants are a key food security crop grown by local farmers in Africa due to the plant's ability to withstand harsh outdoor elements. When Cassava plants incur disease, it can devastate a local farmer's crops and income that drastically affects their source of food and quality of life. As a data scientist, I have been tasked with helping to identify 4 different types of viral diseases on plant images in an attempt to expedite disease identification and mitigate local African farmer's poor crop yields.

In this project, I have ~20k images that I will train a disease classification model using a convultional neural network with an accuracy score higher than ~61%. By applying transfer learning using EfficientNetB architecture, I yield an accuracy score of 85% in our model to detect different types of disease or healthy plants.
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

## Motivation and Background

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

