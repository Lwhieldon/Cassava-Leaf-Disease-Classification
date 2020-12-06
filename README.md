# Cassava Leaf Disease Classification
Using Machine Learning Algorithms to Identify the Type of Disease Present on a Cassava Leaf Image

# Poison Mushroom Alert! 
<p align="center"style="font-size:22px">
 Deadly v. Edible Gilled Mushroom Classification
</p>

<p align="center">
<img src="https://github.com/Lwhieldon/IstheMushroomPoisonous/blob/master/notebooks+data+images/images/edible-vs-poisonous-mushrooms.jpg?raw=true" width="400" height="200" />
</p>

## Overview

Is it possible to tell if a gilled mushroom in North American is poisonous or not just by its physical characteristics?  In this project, I compare different classification algorithms to accurately predict if a gilled mushroom is toxic.

## Goals

This repo is part of the work completed within UMBC's DATA602 Course: Intro to Data Analysis and Machine Learning.

In this project, I attempt to achieve the following:
<ol>
<li><b>Exploration of Gilled Mushroom Features:</b> Examine features of toxic versus edible North American gilled mushrooms.</li>
<li><b>Optimal Classification Model:</b> Compare 3 commonly used classification models for accuracy: Logistic Regression, K Nearest Neighbor (kNN), and Decision Tree Classification.</li>
<li><b>Provide Solid Feedback to Stakeholders:</b> Effectively articulate outcomes of study and next steps to key stakeholders in the mushroom foraging communities (in this fictitious case, Oregan).</li>
</ol>

## Motivation and Background

Mushrooms (a.k.a. Fungi) have a multitude of uses for humankind. From medicine, food, and even for esoteric uses like packaging & biofuel, fungi have the potential to unlock biological material that's considered a 'waste product' in our civilization and convert it into something else entirely useful. Small business communities of mushroom foragers are now more than ever seeing a rise in the interest of fungi throughout the world.

Mushrooms are equally as useful as they are morbid: In a study conducted in Turkey in 2018, it was discovered that environmental foraging of mushrooms can result in serious illness and death, resulting in a 20% mortality rate in adults and 50% in children who consume poisonous mushrooms. It is apparent that the mushroom foraging industry needs quality measures to ensure that these statistics decrease.

In this project, I will pretend that I am a data scientist hired by a business community of local mushroom foragers in Oregon and they need my help to build out a better process to identify if gilled mushrooms are poisonous or edible; they have a bunch of 'young' foragers who need a little help!
<p align="center">
<img src="https://github.com/Lwhieldon/IstheMushroomPoisonous/blob/master/notebooks+data+images/images/587c2ffe1150c.image.jpg?raw=true" height="300" />
</p>

## Data Details

<a href=https://archive.ics.uci.edu/ml/datasets/mushroom>UCI Machine Learning Mushroom Dataset</a>

This dataset contains 8124 entries corresponding to 23 species of gilled mushrooms from North America.

Each species is identified as:
<ul>
<li>Definitely edible (e),</li> 
<li>Definitely poisonous (p), or</li> 
<li>Of unknown edibility and not recommended (also p).</li> 
<li>Each entry is a single mushroom and has 22 features related to its physical characteristics. </li>
</ul>

Mushroom records drawn from <i>The Audubon Society Field Guide to North American Mushrooms (1981)</i>. G. H. Lincoff (Pres.), New York: Alfred A. Knopf
 
## Video Presentation

A virtual presentation has been created to help support this project. Please review the video using think link: https://youtu.be/bL5E18r6EYc

## Table of Contents

This assignment contains 6 areas:

<ol>
  <li><a href=https://github.com/Lwhieldon/IstheMushroomPoisonous/blob/master/Presentation.pdf>Presentation:</a> Powerpoint presentation to support the deliverables.</li>
  <li><a href=https://github.com/Lwhieldon/IstheMushroomPoisonous/blob/master/notebooks%2Bdata%2Bimages/mushrooms.csv>Dataset in Repo</a>. Local copy of the original dataset from the ICU Machine Learning Repository.</li>
  <li><a href=https://github.com/Lwhieldon/IstheMushroomPoisonous/blob/master/notebooks%2Bdata%2Bimages/labels.txt>Dataset Labels</a> A helpful text file explaining each feature label assigned to a mushroom. </li>
  <li><a href=https://github.com/Lwhieldon/IstheMushroomPoisonous/blob/master/notebooks%2Bdata%2Bimages/summaryreport.ipynb>Summary and Report</a>: Jupyter Notebook including a detailed abstract on problems in assignment, code relevant to project, and visualizations supporting the completion of the project. </li>
  <li> <a href=https://github.com/Lwhieldon/IstheMushroomPoisonous/blob/master/notebooks%2Bdata%2Bimages/code.ipynb>Code:</a> Area to perform testing of dataset, functions, and implement models before final project output. </li>
  <li> <a href=https://github.com/Lwhieldon/IstheMushroomPoisonous/blob/master/notebooks%2Bdata%2Bimages/utils.py>utils.py:</a> .py file to store functions I use throughout the project to make notebooks & summary report clean. </li>
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
Assignment Submitted     : October 2020
</pre>

